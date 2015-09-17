PBFALCON_TC_RUNNERS:= \
	pbfalcon.tasks.scatter0_run_daligner_jobs \
	pbfalcon.tasks.scatter1_run_daligner_jobs \
	pbfalcon.tasks.gather0_run_daligner_jobs \
	pbfalcon.tasks.gather1_run_daligner_jobs \

update:
	\rm -f *.json
	${MAKE} all
	#${MAKE} canon
canon:
	../canonicalize.py .
all: modules runners
modules:
	python -m pbfalcon.tasks.basic emit-tool-contracts
runners: ${PBFALCON_TC_RUNNERS}

# This applies only to pbcommand-runners, not plain modules.
%:
	python -m $@ --emit-tool-contract >| $@_tool_contract.json

.PHONY: all modules runners update
