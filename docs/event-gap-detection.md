# Event checkpoint gaps

The listener should compare each checkpoint with the preceding checkpoint and
record a gap when the sequence is not contiguous. A gap emits a structured log
and metric with both checkpoint values, then schedules bounded backfill before
normal polling resumes.
