1. Esiteks seadistasin kasutaja ja ühendasin siinse tegevuse GitHub-ga

   git config --global user.name "Ken Elken"
   git config --global user.email "ken.elken@vikk.ee"

2. Seejärel tegin Repo  GitHubis

Repo nimi: MinuRepo

Lisasin sinna README.md

Kloonisin repo arvutisse

3. Lisasin esimese faili ja tegin commit-i

echo "# Tere, GitHub!" > README.md
git add README.md
git commit -m "Lisa esmane README"
git status

4. Push GitHubi

git push origin main

5. Tegin veebis muudatuse ja tõmbasin selle siis arvutisse

git pull origin main

6. Lõin uue haru ja uus pull request ka

git checkout -b feature/tervitus
echo "Uus rida feature-harus" >> README.md
git add README.md
git commit -m "Lisa tervituse rida"
git push -u origin feature/tervitus

Selle peale tuli GitHubi veebilehel pull request ja merge main harule

7. Hitignore tegin ka

echo ".DS_Store" >> .gitignore
echo ".idea/" >> .gitignore
echo "node_modules/" >> .gitignore
git add .gitignore
git commit -m "Lisa .gitignore"
git push origin main