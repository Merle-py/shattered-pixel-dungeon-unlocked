# Shattered Pixel Dungeon Unlocked

Este projeto é um fork de [Shattered Pixel Dungeon](https://github.com/00-Evan/shattered-pixel-dungeon), criado por Evan Debenham, baseado no Pixel Dungeon original de Watabou.

A proposta deste fork é simples: deixar o conteúdo que normalmente depende de progressão global disponível desde a primeira execução, sem marcar badges/conquistas como obtidos automaticamente.

## O que está desbloqueado

- Warrior
- Mage
- Rogue
- Huntress
- Duelist
- Cleric
- Challenges
- Custom Seed
- Daily Run
- Randomização completa de herói/desafios
- Informações de talentos
- Informações de subclasses
- Informações de Armor Abilities

A progressão dentro de uma run continua funcionando normalmente. Subclasses, talentos de tiers superiores e Armor Abilities ainda são adquiridos durante a partida nos momentos normais do jogo. O mod apenas remove os bloqueios de conteúdo ligados à progressão global da conta.

Badges não são concedidos automaticamente. Eles continuam sendo registrados conforme você realmente os conquista.

## Android: como baixar o APK pelo GitHub

Este repositório possui um GitHub Actions que compila automaticamente um APK instalável.

1. Abra a aba **Actions** deste repositório.
2. Abra a execução mais recente chamada **Build Android APK**.
3. Na parte inferior da execução, procure **Artifacts**.
4. Baixe o arquivo `shattered-pixel-dungeon-unlocked-debug`.
5. Extraia o ZIP baixado.
6. Transfira o APK para seu celular Android.
7. Abra o APK e autorize a instalação de apps desconhecidos caso o Android solicite.
8. Instale normalmente.

O mod usa o package `com.merlepy.shatteredpixeldungeonunlocked`, então ele pode ficar instalado ao mesmo tempo que o Shattered Pixel Dungeon oficial.

## Como entrar no jogo

Depois de instalar:

1. Abra **Shattered Pixel Dungeon Unlocked** no celular.
2. Passe pela tela inicial de apresentação.
3. Toque em **Entrar/Enter**.
4. Na tela de seleção, escolha qualquer uma das seis classes.
5. Toque no botão com o nome da classe para iniciar a run.

Para acessar Challenges, Daily Run, Custom Seed e randomização, entre na tela de seleção de herói e abra o botão de opções ao lado do botão de iniciar.

## Compilar localmente no Android

O projeto usa Gradle Wrapper. Com Java/JDK configurado e Android SDK instalado:

```bash
./gradlew android:assembleDebug
```

No Windows:

```bat
gradlew.bat android:assembleDebug
```

O APK será criado em:

```text
android/build/outputs/apk/debug/
```

Também é possível abrir o projeto no Android Studio e executar o módulo `android` diretamente em um aparelho ou emulador.

## Versão

Base atual do fork: **Shattered Pixel Dungeon 3.3.8**.

Versão do mod: **3.3.8-unlocked.1**.

## Alterações principais do fork

- `HeroClass.isUnlocked()` libera todas as classes.
- Os gates que o Shattered usa para builds de desenvolvimento são mantidos ativos neste fork para expor Challenges, Custom Seed, Daily Run e informações avançadas sem editar o arquivo de badges.
- O package do Android foi alterado para evitar conflito com o aplicativo oficial.
- O verificador de atualizações oficial foi desativado na build Android do mod para impedir que uma versão oficial substitua esta variante.

## Créditos e licença

Shattered Pixel Dungeon é desenvolvido por [Evan Debenham / Shattered Pixel](https://shatteredpixel.com/) e é baseado no [Pixel Dungeon](https://github.com/00-Evan/pixel-dungeon-gradle), de Watabou.

Este fork mantém a licença **GNU General Public License v3.0 (GPL-3.0)** do projeto original. Consulte o arquivo [LICENSE](LICENSE.txt) e os créditos existentes no jogo/projeto.

Este projeto não é uma versão oficial de Shattered Pixel Dungeon e não é afiliado ao desenvolvedor original.

## Documentação original

Os guias do projeto original continuam disponíveis em `/docs`:

- [Compilando para Android](docs/getting-started-android.md)
- [Compilando para desktop](docs/getting-started-desktop.md)
- [Compilando para iOS](docs/getting-started-ios.md)
- [Alterações recomendadas para forks](docs/recommended-changes.md)
