# Schedulo

Schedulo is a job scheduler that enables users to:

* Schedule multiple cron-based jobs.

* Track jobs across system restarts.

* Ensure exactly-once execution.

* Handle simultaneous job execution.

* Provide job status, logs, and searching capabilities of a particular job.

* Support instant job execution, job removal, and running jobs scheduled for future timeframes.


Usage

```Bash
#Schedule a job 
schedulo add "*/10 * * * *" <path to the file>

#Instant execution of a job 
schedulo run <job_id>

# Remove of a job
schedulo remove <job_id>

# Run a future job
schedulo run --date 01/03/25

# List out all the jobs
schedulo list

# Display the next N execution times
schedulo next <job_id> --count 3 

# Status the jobs
schedulo status <job_id>

# History of a given job
schedulo logs <job_id>

# Remove a job from schedule
schedulo purge <job_id>

# Remove all jobs
schedulo reset 
```

Future Enhancements to lookout for:
- Support scheduling HTTP calls natively.
- Job dependency runner (run job B after job A completes).
- Distributed execution using a message queue (e.g., RabbitMQ, Kafka).
- Time zone support for scheduling.
