---
layout: project
type: project
image: img/
title: "Determining the Age of NGC 6791 Through BVI Data"
date: 2022-2023
published: true
labels:
  - Fortran
summary: "Utilizing MESA Star 1D modeling (modeling with graphs) to study the age of NGC 6791"
---

<div class="text-center p-4">
  <img width="200px" src="../img/" class="img-thumbnail" >
</div>

Paragraph here

```cpp
class Player : public MovingObject {
protected:
// etc. variables
	struct Scalar { //dictates what proportion of the player's acceleration goes into x and y components of velocity
		double x; //proportion of acceleration in x direction (-1 to 1)
		double y; //proportion of acceleration in y direaction (-1 to 1)
	};
	Scalar s;
	sf::Sprite* playerSprite;
	sf::Texture* playerTexture;

// etc. functions
// etc. functions

	//calculates what proportion of thrust should go into x and y components
	void calculateScalar() {
		s.x = cos(rotation);
		s.y = sin(rotation);
	}

	//rotates object left, affected by rotateSpeed
	void rotateLeft() {
		rotation += rotateSpeed;
		if (rotation > (2 * PI)) rotation -= (2 * PI);
		calculateScalar();
	}

	//rotates object right, affected by rotateSpeed
	void rotateRight() {
		rotation -= rotateSpeed;
		if (rotation < 0) rotation = 2 * PI + rotation;
		calculateScalar();
	}

	//accelerates forward by moveSpeed, limit is maxVelocity
	void accelerateForward() {
		if (fuel > 0) {
			//FOR X
			//velocity adjustment will not be applied if velocity is over max
			if (abs(v.x) < maxVelocity) {
				v.x += moveSpeed * s.x;
			}
			//unless the adjustment decreases the velocity
			else if (abs(v.x + (moveSpeed * s.x)) < maxVelocity) {
				v.x += moveSpeed * s.x;
			}
			//FOR Y
			//velocity adjustment will not be applied if velocity is over max
			if (abs(v.y) < maxVelocity) {
				v.y += moveSpeed * s.y;
			}
			//unless the adjustment decreases the velocity
			else if (abs(v.y + (moveSpeed * s.y)) < maxVelocity) {
				v.y += moveSpeed * s.y;
			}
			fuel -= fuelConsumptionRate;
		}
	}

	//accelerates reverse by moveSpeed, limit is maxVelocity
	void accelerateReverse() {
		if (fuel > 0) {
			//FOR X
		//velocity adjustment will not be applied if velocity is over max
			if (abs(v.x) < maxVelocity) {
				v.x -= moveSpeed * s.x;
			}
			//unless the adjustment decreases the velocity
			else if (abs(v.x - (moveSpeed * s.x)) < maxVelocity) {
				v.x -= moveSpeed * s.x;
			}

			//FOR Y
			//velocity adjustment will not be applied if velocity is over max
			if (abs(v.y) < maxVelocity) {
				v.y -= moveSpeed * s.y;
			}
			//unless the adjustment decreases the velocity
			else if (abs(v.y - (moveSpeed * s.y)) < maxVelocity) {
				v.y -= moveSpeed * s.y;
			}
			fuel -= fuelConsumptionRate;
		}
	}

};

```



https://github.com/AndrewGBalaschak/PA9


