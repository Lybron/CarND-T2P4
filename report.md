# Report: CarND PID Controller

- Student describes the effect of the `P`, `I`, `D` component of the PID algorithm in their implementation. Is it what you expected?

The final values for the PID controller are:
- `P: -0.1`
- `I: 0`
-` D: -8.0`

The proportional term, `P`, affects how aggressively the car attempts to make corrections to return to the correct position, and is negative in order to steer opposite to the cross-track error. The final `P` value, `-0.1`, provides a good threshold to make unaggressive track corrections.

The integral term, `I`, affects the car's ability to compensate for accumulative errors, such as misalignment of the wheels. These errors were negligible in attempting to navigate the track, so the integral term is set to `0`.

The derivative term, `D`, affects the affects how quickly the car converges to the neutral position (i.e. cross-track error = 0). The final `D` value, `-8.0`, means the car will quickly dampen cross-track errors.

[PID Controller Demo](https://youtu.be/0rV-bd-4_xs)

- Student discusses how they chose the final hyperparameters (P, I, D coefficients). This could be have been done through manual tuning, twiddle, SGD, or something else, or a combination!

I tuned the hyperparameters manually, observing the effects of each change by running the simulator.
