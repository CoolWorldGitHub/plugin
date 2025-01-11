``` xml title="submerged.xml" linenums="4"

<Calculator name="FLL Submerged 24/25" version="1">
    <UserInterface>
        <Header>Equipment Inspection</Header>
        <CheckboxMission noMaterial="true" description="The robot and all the equipment fits in one launch area under a height limit of 30.5cm." score="20" default="true" id="equipment.inspection.main"/>
        <Header>Coral Nursery</Header>
        <CheckboxMission noMaterial="true" description="The coral tree is hanging on the support." score="20" id="coral-nursery.tree.main"/>
        <CheckboxMission noMaterial="true" description="The bottom of the coral tree is in its holder." score="10" bonusFor="coral-nursery.tree.main" id="coral-nursery.tree.bonus"/>
        <CheckboxMission noMaterial="true" description="The coral are flipped up." score="20" id="coral-nursery.buds.main"/>
        <Header>Shark</Header>
        <CheckboxMission description="The shark is no longer touching the cave." score="20" id="shark.cave.main"/>
        <CheckboxMission description="The shark is touching the mat and is at least partly in the habitat." score="10" id="shark.habitat.main"/>
        <Header>Coral Reef</Header>
        <CheckboxMission noMaterial="true" description="The coral reef is flipped up and not touching the mat." score="20" id="coral-reef.flip.main"/>
        <CounterMission noMaterial="true" description="The reef segments are standing upright, outside of home and touch the mat." scoreEach="5" max="3" id="coral-reef.segments.main"/>
        <Header>Scuba Diver</Header>
        <CheckboxMission description="The scuba diver is no longer touching the coral nursery." score="20" id="scuba-diver.nursery.main"/>
        <CheckboxMission description="The scuba diver is hanging on the coral reef support." score="20" id="scuba-diver.reef.main"/>
        <Header>Angler Fish</Header>
        <CheckboxMission description="The angler fish is latched within the shipwreck." score="30" id="angler-fish.shipwreck.main"/>
        <Header>Raise the Mast</Header>
        <CheckboxMission noMaterial="true" description="The mast of the shipwreck is completely raised." score="30" id="ship-wreck.mast.main"/>
        <Header>Kraken's Treasure</Header>
        <CheckboxMission noMaterial="true" description="The treasure chest is completely outside the nest of the kraken." score="20" id="kraken-nest.treasure.main"/>
        <Header>Artificial Habitat</Header>
        <CounterMission noMaterial="true" description="A artificial habitat stack segment is completely flat and upright." scoreEach="10" max="4" id="artificial-habitat.segments.main"/>
        <Header>Unexpected Encounter</Header>
        <CheckboxMission description="The unknown creature is released." score="20" id="unexpected-encounter.creature.release"/>
        <CheckboxMission description="The unknown creature is at least partially in the cold seep." score="10" id="unexpected-encounter.creature.delivery"/>
        <Header>Send over the Submersible</Header>
        <CheckboxMission noMaterial="true" description="The yellow flag on your side is down." score="30" id="team-task.flag.main"/>
        <CheckboxMission description="The submersible is clearly closer to the opposing field." score="10" id="team-task.submersible.main"/>
        <Header>Sonar Discovery</Header>
        <CheckboxMission description="At least one whale is revealed." score="20" id="sonar.whale.single"/>
        <CheckboxMission description="Both whales are revealed." score="10" id="sonar.whale.both" bonusFor="sonar.whale.single"/>
        <Header>Feed the Whale</Header>
        <CounterMission noMaterial="true" description="A krill is at least partly in the mouth of the whale." scoreEach="10" max="5" id="whale.krill.main"/>
        <Header>Shipping Lanes</Header>
        <CheckboxMission description="The ship is flipped over and touches the mat." score="20" id="shipping-lanes.ship.main"/>
        <Header>Sample Collection</Header>
        <CheckboxMission description="The water sample is completely outside the water sample area." score="5" id="sample-collection.water.removed"/>
        <CheckboxMission description="The seabed sample is no longer touching the seabed." score="10" id="sample-collection.seabed.removed"/>
        <CheckboxMission description="The plankton sample is no longer touching the kelp forest." score="10" id="sample-collection.plankton.removed"/>
        <CheckboxMission description="A piece of the trident is no longer touching the shipwreck." score="20" id="sample-collection.trident-removal.single"/>
        <CheckboxMission description="Both pieces of the trident are no longer touching the shipwreck." score="10" bonusFor="sample-collection.trident-removal.single" id="sample-collection.trident-removal.both"/>
        <Header>Research Vessel</Header>
        <CounterMission noMaterial="true" description="A sample is in the research vessel." scoreEach="5" max="3" id="research-vessel.sample-collection.main">
            <CounterBudget>
                <Requirement budget="1" requirement="sample-collection.water.removed"/>
                <Requirement budget="1" requirement="sample-collection.seabed.removed"/>
                <Requirement budget="1" requirement="sample-collection.plankton.removed"/>
            </CounterBudget>
        </CounterMission>
        <CounterMission noMaterial="true" description="A trident part is in the research vessel." scoreEach="5" max="2" id="research-vessel.trident.main">
            <CounterBudget>
                <Requirement budget="1" requirement="sample-collection.trident-removal.single"/>
                <Requirement budget="1" requirement="sample-collection.trident-removal.both"/>
            </CounterBudget>
        </CounterMission>
        <CheckboxMission noMaterial="true" description="The treasure chest is in the research vessel." score="20" id="research-vessel.chest.main"/>
        <CheckboxMission noMaterial="true" description="The port latch holds at least partly onto the research vessel." score="20" id="research-vessel.port.main"/>
        <Header>Precision Tokens</Header>
        <CounterMission description="Remaining Precision Tokens" max="6" default="6" id="referee.precision-tokens.main">
            <ScoringCurve>
                <Score count="6" score="50"/>
                <Score count="5" score="50"/>
                <Score count="4" score="35"/>
                <Score count="3" score="25"/>
                <Score count="2" score="15"/>
                <Score count="1" score="10"/>
                <Score count="0" score="0"/>
            </ScoringCurve>
        </CounterMission>
    </UserInterface>
</Calculator>
```