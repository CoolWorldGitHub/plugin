# Calculator Definition Files

!!! info "File"

    Calculator definition files are XML files.

## General Structure
The following is the general, minimal structure:

``` xml
<?xml version="1.0" encoding="UTF-8" ?>
<Calculator name="<insert name of calculator>" version="1">
    <UserInterface>
        ...
    </UserInterface>
</Calculator>
```

!!! danger "Version"

    Don't change this value if you don't know what you are doing!

The magic happens in the `<UserInterface>` section.

### UserInterface
The `<UserInterface>` section contains elements that describe the calculator UI.

!!! warning "Important"

    Some elements require an ID. Each ID must be unique.

### Header

``` xml
<Header>Title</Header>
```

### Checkbox Missions

A switch that can give points:

``` xml
<CheckboxMission description="When should points be awarded for this mission?" score="20" id="my.id"/>
```
***
Bonus missions that can only be scored if another mission already has been solved:

``` xml
<CheckboxMission description="When should points be awarded for this mission?" score="20" id="my.id" bonusFor="other.id"/>
```
***
When the noMaterial flag is set to true, the no-material-at-the-end-of-the-match icon is displayed:

``` xml
<CheckboxMission noMaterial="true" description="When should points be awarded for this mission?" score="20" id="my.id"/>
```
***
When the default flag is set to true, the no-material-at-the-end-of-the-match icon is displayed:

``` xml
<CheckboxMission noMaterial="true" description="When should points be awarded for this mission?" score="20" id="my.id"/>
```

### Counter Mission
Displays a basic counter:

``` xml
<CounterMission description="When should points be awarded for this mission?" scoreEach="10" max="10" id="my.id"/>
```
***
When the noMaterial flag is set, the no-material-at-the-end-of-the-match icon is displayed:
``` xml
<CounterMission noMaterial="true" description="When should points be awarded for this mission?" scoreEach="10" max="10" id="my.id"/>
```
***
With the optional min argument, a minimum can be set:
``` xml
<CounterMission description="When should points be awarded for this mission?" scoreEach="10" max="10" min="1" id="my.id"/>
```
***
Make the max dependent on other tasks:
``` xml
<CounterMission description="A trident part is in the research vessel." scoreEach="5" max="2" id="research-vessel.trident.main">
    <CounterBudget>
        <Requirement budget="1" requirement="sample-collection.trident-removal.single"/>
        <Requirement budget="1" requirement="sample-collection.trident-removal.both"/>
    </CounterBudget>
</CounterMission>
Use a nonlinear curve for scores:

<CounterMission description="Remaining Precision Tokens" max="6" default="6">
    <ScoringCurve>
        <Score count="6" score="50" />
        <Score count="5" score="50" />
        <Score count="4" score="35" />
        <Score count="3" score="25" />
        <Score count="2" score="15" />
        <Score count="1" score="10" />
        <Score count="0" score="0" />
    </ScoringCurve>
</CounterMission>
```
***
A combination of CounterBudget and ScoringCurve is valid.

A CounterMission considers itself completed if the achieved score is greater than 0

!!! success "Example"

    Here is a [Example](/plugin/RoboScore/template-submerged/)