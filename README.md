## Minimal Example of Distributed Tracing

### Setup
Set up a python virtualenv and install requirements
```
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Running 
Start the distributed child server first
```
python3 distributed_child.py
```

Then run the distributed parent call
```
python3 distributed_parent.py
```

You should see a trace populate the "distributed-parent" project in LangSmith. If you don't have this project, it will be created for you.

This trace will include your child call, as well as telemetry on LLM Stats.