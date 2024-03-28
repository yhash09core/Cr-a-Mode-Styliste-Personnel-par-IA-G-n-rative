# Cr-a-Mode-Styliste-Personnel-par-IA-G-n-rative
Créa-Mode utilise l'IA générative pour créer des designs de mode uniques et personnalisés en fonction du style, des mensurations et des préférences de couleurs et de textures des utilisateurs.
import random

class FashionDesignGenerator:
    def __init__(self, user_preferences):
        """
        Initializes the fashion design generator with user preferences.
        :param user_preferences: A dict containing style, measurements, color preferences, and textures.
        """
        self.style = user_preferences['style']
        self.measurements = user_preferences['measurements']
        self.color_preferences = user_preferences['color_preferences']
        self.textures = user_preferences['textures']
    
    def generate_design(self):
        """
        Generates a fashion design based on user preferences.
        :return: A dict representing the generated fashion design.
        """
        # Simulating generative AI fashion design process
        design = {
            'sketch': self._generate_sketch(),
            'fabric': self._select_fabric(),
            'colors': self._select_colors(),
            'measurements': self.measurements,
        }
        return design
    
    def _generate_sketch(self):
        """
        Simulates the sketch generation process.
        :return: A string representing the sketch URL or ID.
        """
        # Placeholder for a generative model to create a sketch
        return "sketch_{}".format(random.randint(1, 100))
    
    def _select_fabric(self):
        """
        Selects fabric based on user's texture preferences.
        :return: A string representing the selected fabric.
        """
        # This could be enhanced by using AI to match textures to available fabrics
        return random.choice(self.textures)
    
    def _select_colors(self):
        """
        Selects colors based on user's color preferences.
        :return: A list of colors that will be used in the design.
        """
        # This could be enhanced by using AI to create a pleasing color palette
        return random.sample(self.color_preferences, min(len(self.color_preferences), 3))

# Example usage
user_preferences = {
    'style': 'casual',
    'measurements': {'chest': 38, 'waist': 32, 'hip': 37},
    'color_preferences': ['red', 'blue', 'green'],
    'textures': ['cotton', 'silk', 'denim'],
}

design_generator = FashionDesignGenerator(user_preferences)
generated_design = design_generator.generate_design()

print("Generated Fashion Design:", generated_design)
