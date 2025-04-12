# Best Practices

* Use the command-based programming paradigm.
* Create motor objects in the `RobotContainer` constructor and pass them to the subsystems that need them.
    * If multiple motors will always run in unison, use the *lead-follow* feature. Then, only pass the lead motor to the relevant subsystem.
* Prefer to use motor subsystem-provided closed-loop functionality over the WPILib-provided `PIDSubsystem`/`PIDCommand`.
* If a command requires a single subsystem, create that command within the subsystem via a method.
* It is usually not necessary to write custom `Command` classes. Most behavior can be modeled using the preexisting command suite provided by WPILib.
* Prefer `DeferredCommand` over `ProxyCommand`.
