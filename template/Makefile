combined.py: main.py tools
	python3.13 -m atcoder main.py -o combined.py

tools:
	ln -f -s /workspaces/proconenv/lib_py/tools $@

.PHONY: test
test: combined.py
	oj test -c 'python3.13 combined.py'
#	oj test -c 'python3.13 combined.py' -e 1e-6

.PHONY: submit
submit: combined.py
	acc submit --skip-filename -- --language 5055 --wait 0 --no-open --yes

.PHONY: clean
clean:
	rm -f *~ combined.py

.PHONY: force
force:
	$(MAKE) clean
	$(MAKE)
