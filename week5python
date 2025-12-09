class Hero:
    def __init__(self, name, alias, powers, health=100, stamina=100):
        self.name = name  # Real name of the superhero
        self.alias = alias  # Alias or superhero name (e.g., 'Spiderman')
        self.powers = powers  # List of powers the superhero possesses
        self.health = health  # Health points
        self.stamina = stamina  # Stamina points

    def __str__(self):
        return f"{self.alias} (Real Name: {self.name})"

    def display_powers(self):
        return ', '.join(self.powers)

    def attack(self):
        if self.stamina > 0:
            self.stamina -= 10
            return f"{self.alias} attacks using {self.powers[0]}!"
        else:
            return f"{self.alias} is too tired to attack!"

    def rest(self):
        self.stamina = 100
        return f"{self.alias} is resting and has regained stamina."

# A subclass for a specific type of hero (e.g., a Tech Hero)
class TechHero(Hero):
    def __init__(self, name, alias, powers, tech_gadgets, health=100, stamina=100):
        super().__init__(name, alias, powers, health, stamina)
        self.tech_gadgets = tech_gadgets  # Gadgets the hero uses in battle

    def display_gadgets(self):
        return ', '.join(self.tech_gadgets)

    def attack(self):
        if self.stamina > 0:
            self.stamina -= 15
            return f"{self.alias} attacks with gadgets: {', '.join(self.tech_gadgets)}!"
        else:
            return f"{self.alias} is too tired to attack!"

# Another subclass for a magical hero
class MagicHero(Hero):
    def __init__(self, name, alias, powers, spells, health=100, stamina=100):
        super().__init__(name, alias, powers, health, stamina)
        self.spells = spells  # List of magical spells the hero can cast

    def display_spells(self):
        return ', '.join(self.spells)

    def attack(self):
        if self.stamina > 0:
            self.stamina -= 20
            return f"{self.alias} casts a spell: {self.spells[0]}!"
        else:
            return f"{self.alias} is too tired to attack!"

# Create a few superhero objects
iron_man = TechHero(name="Tony Stark", alias="Iron Man", powers=["Super Strength", "Flying"], tech_gadgets=["Repulsor", "Hulkbuster", "AI suit"])
doctor_strange = MagicHero(name="Stephen Strange", alias="Doctor Strange", powers=["Super Strength", "Intelligence"], spells=["Time Manipulation", "Portal Creation"])

# Interact with the objects
print(iron_man)
print("Powers:", iron_man.display_powers())
print("Gadgets:", iron_man.display_gadgets())
print(iron_man.attack())  # Attack with gadgets
print(iron_man.rest())
