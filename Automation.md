
This is the transcript,

"This is the automation setup of the rail. As you can see it is driving the rotation of the focus knob on the focussing block."

Say over it "On the left is the Arduino, in the center is the BigEasyDriver board and on the right is the stepper motor."

[Cut here to the cogs close-up]

"The stepper motor drives the focus knob via some cogs,"

[Cut to micron side]

"and on the other side the distance travelled by the camera platform is marked in microns."

[cut to overview]

"Returning to the overview of the setup, we will now look at the wiring of each of the parts in turn. To see the sources of all of these parts please see the urls listed at the end of this video."

[Cut to bigeasydriver]

Say: "First we are going to look at the BigEasyDriver because it has connections to all of the other parts.

"The BigEasyDriver was bought from Sparkfun and a tutorial by the manufacturer can be seen at the url on screen."

Show https://learn.sparkfun.com/tutorials/big-easy-driver-hookup-guide on screen.

"We use the BigEasyDriver because it gives much finer control over the rotation of the stepper motor. "

Now we will look at the wiring of the BigEasyDriver.

[cut to bigeasydriver pointing shot]

On the bottom left we have the connectors for the 5V power cable that drives the stepper motor.

To the right of this we have the connectors for the wires of the stepper motor. The wires can be seen below and are connected in pairs to the "B" connections on the left and the "A" connections on the right. The colour of the wires that are connected in pairs depends on the wiring of the motor and we will come back to that later.

[add a "C" marker pointing to the potentiometer on the screen. About 1:18 to 1:32]

Near the centre of the BigEasyDriver, is a potentiometer marked "C" here and this may need to be adjusted using a small screwdriver. This adjusts the current reaching the motor, and turning the potentiometer gently until the sweet spot is found will cause the motor to turn smoothly.

Now we change focus from the front of the BigEasyDriver to the back.

At the top left we can see the DIR connetor, the STEP connector and the Ground connector and these are connected respectively to Digital 3, Digital 2, and the ground connector of the Arduino, which we will look at in a minute.

The Step pin is a logic input. Any transition on the step pin from Low to High triggers the motor to step forward one step. The direction and size of the step is controlled in this setup by the DIR pin.

The DIR pin is also a logic input. The pin determines the direction of the motor rotation. Changes in state only take effect when the Step pin changes state.

These are all the pins that we need to use in the bigeasydriver.

We now return to the overview before taking a look at the Arduino wiring.

This is the Arduino computer, which runs the computer programme to control the stepper motor via the BigEasyDriver.

The wires from the BigEasyDriver are inserted into the slots at the back and at the front shown here.


Looking in more detail, we can see the Step and Dir wires coming into the Digital 2 and digital 3 sockets respectively.

Moving focus to the front of the Arduino, we can see the ground wire from the BigEasydriver coming into the ground slot.

We now return to the BigEasyDriver for a quick look at the stepper motor wires, before going on to find out which stepper motor wires go into which of the A and B slots.

The Sparkfun documentation on this says "For a 4-wire motor, take one wire and check its resistance against each of the three remaining wires. Whichever wire shows the lowest resistance against the first wire is the pair mate. The remaining two wires should show similar resistance between the two of them."

The Ohm meter shows the kind of response that you can expect when testing the resistance.

Having found the correct pairings, one pair are connected to the A connections, and the other two to the B connections.

For a 6 wire motor, please refer to the sparkfun documentation listed previously.

We now return to the overview, before taking a look at the wiring for the infra red camera remote control. The remote control allows the camera shutter to be triggered automatically between movements of the focus rail. It is also programmed from the arduino and so we will look at the wiring for this setup now. In order for this mechanism to work, the camera must be put on the setting usually used with the manufacturer's own infra red remote control.


We now see the wiring to the Arduino, where the two wires are connected into the Digital 13 and ground sockets shown here on the left.


In order to make the remote control for this setup, we bought a 3rd party infra red remote control, and stipped off the outer casing.

At one end is the bulb and then here we can see the purple wire leading from the Digital 13 socket, and the white wire leading form the Ground socket. They were fixed on using a hot glue gun.


We have now covered all of the details of the autmation setup for the focus rail, so we will just look again at the overview the cogs and the micron marking on the focus block knobs as they are working.

For more details and for the code to drive the setup please see the pdfs associated with this video at the url listed on the final screen, or the writeup on hackster or GitHub. The sources of the parts that we used are also listed at the end of this video.

Print all urls on final sheet.
