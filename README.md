# Week 5:class Hero:
    def __init__(self, name, alias, powers, health=100, stamina=100):
        self.name = name  # Real name of the superhero
        self.alias = alias  # Alias or superhero name (e.g., 'Spiderman')
        self.powers = powers  # List of powers the superhero possesses
        self.health = health  # Health points
        self.stamina = stamina  # Stamina points

# A subclass for a specific type of hero (e.g., a Tech Hero)
class TechHero(Hero):
    def __init__(self, name, alias, powers, tech_gadgets, health=100, stamina=100):
        super().__init__(name, alias, powers, health, stamina)
        self.tech_gadgets = tech_gadgets  # Gadgets the hero uses in battle


# Another subclass for a magical hero
class MagicHero(Hero):
    def __init__(self, name, alias, powers, spells, health=100, stamina=100):
        super().__init__(name, alias, powers, health, stamina)
        self.spells = spells  # List of magical spells the hero can cast


# Create a few superhero objects
iron_man = TechHero(name="Tony Stark", alias="Iron Man", powers=["Super Strength","Flying"], tech_gadgets=["Repulsor", "Hulkbuster", "AI suit"])


# Interact with the objects
print(iron_man)
print("Powers:", iron_man.display_powers())
print("Gadgets:", iron_man.display_gadgets())
print(iron_man.attack())  # Attack with gadgets
print(iron_man.rest())
