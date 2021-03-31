---
title: Métodos de objeto de caractere
description: Métodos de objeto de caractere
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917169"
---
# <a name="character-object-methods"></a>Métodos de objeto de caractere

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor também expõe métodos para cada caractere em uma coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) . Os métodos a seguir têm suporte:

-   [**Activate**](activate-method.md)
-   [**GestureAt**](gestureat-method.md)
-   [**Obter**](get-method.md)
-   [**Ocultar**](hide-method.md)
-   [**Atividades**](interrupt-method.md)
-   [**Escutar**](listen-method.md)
-   [**Mover**](moveto-method.md)
-   [**Reproduzir**](play-method.md)
-   [**programa**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Stop**](stop-method.md)
-   [**Do opAll**](stopall-method.md)
-   [**Pensar**](think-method.md)
-   [**Aguarde**](wait-method.md)

Para usar um método, referencie o caractere na coleção. No VBScript e Visual Basic, você faz isso especificando a ID de um caractere:


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



Para simplificar a sintaxe do seu código, você pode definir uma variável de objeto e defini-la para fazer referência a um objeto de caractere na coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) ; em seguida, você pode usar a variável para referenciar métodos ou propriedades do caractere. O exemplo a seguir demonstra como você pode fazer isso usando a instrução Visual Basic set:


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



No Visual Basic 5,0, você também pode criar sua referência declarando sua variável como um objeto de [**caractere**](/windows/desktop/lwef/the-characters-object):


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



Declarar o objeto do tipo IAgentCtlCharacterEx habilita a ligação antecipada no objeto, o que resulta em um melhor desempenho.

No VBScript, você não pode declarar uma referência como um tipo específico. No entanto, você pode simplesmente declarar a referência de variável:


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



Algumas linguagens de programação não dão suporte a coleções. No entanto, você pode acessar os métodos de um objeto [**Character**](/windows/desktop/lwef/the-characters-object) com o método [**Character**](character-method.md) :


```
   agent.Characters.Character("CharacterID").method
```



Além disso, você também pode criar uma referência ao objeto [**Character**](/windows/desktop/lwef/the-characters-object) para tornar o código de script mais fácil de seguir:


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 