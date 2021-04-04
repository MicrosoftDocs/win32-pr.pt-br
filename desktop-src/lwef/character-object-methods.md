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
# <a name="character-object-methods"></a><span data-ttu-id="72249-103">Métodos de objeto de caractere</span><span class="sxs-lookup"><span data-stu-id="72249-103">Character Object Methods</span></span>

<span data-ttu-id="72249-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72249-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="72249-105">O servidor também expõe métodos para cada caractere em uma coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="72249-105">The server also exposes methods for each character in a [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span> <span data-ttu-id="72249-106">Os métodos a seguir têm suporte:</span><span class="sxs-lookup"><span data-stu-id="72249-106">The following methods are supported:</span></span>

-   [<span data-ttu-id="72249-107">**Activate**</span><span class="sxs-lookup"><span data-stu-id="72249-107">**Activate**</span></span>](activate-method.md)
-   [<span data-ttu-id="72249-108">**GestureAt**</span><span class="sxs-lookup"><span data-stu-id="72249-108">**GestureAt**</span></span>](gestureat-method.md)
-   [<span data-ttu-id="72249-109">**Obter**</span><span class="sxs-lookup"><span data-stu-id="72249-109">**Get**</span></span>](get-method.md)
-   [<span data-ttu-id="72249-110">**Ocultar**</span><span class="sxs-lookup"><span data-stu-id="72249-110">**Hide**</span></span>](hide-method.md)
-   [<span data-ttu-id="72249-111">**Atividades**</span><span class="sxs-lookup"><span data-stu-id="72249-111">**Interrupt**</span></span>](interrupt-method.md)
-   [<span data-ttu-id="72249-112">**Escutar**</span><span class="sxs-lookup"><span data-stu-id="72249-112">**Listen**</span></span>](listen-method.md)
-   [<span data-ttu-id="72249-113">**Mover**</span><span class="sxs-lookup"><span data-stu-id="72249-113">**MoveTo**</span></span>](moveto-method.md)
-   [<span data-ttu-id="72249-114">**Reproduzir**</span><span class="sxs-lookup"><span data-stu-id="72249-114">**Play**</span></span>](play-method.md)
-   [<span data-ttu-id="72249-115">**programa**</span><span class="sxs-lookup"><span data-stu-id="72249-115">**Show**</span></span>](show-method.md)
-   [<span data-ttu-id="72249-116">**ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="72249-116">**ShowPopupMenu**</span></span>](showpopupmenu-method.md)
-   [<span data-ttu-id="72249-117">**Speak**</span><span class="sxs-lookup"><span data-stu-id="72249-117">**Speak**</span></span>](speak-method.md)
-   [<span data-ttu-id="72249-118">**Stop**</span><span class="sxs-lookup"><span data-stu-id="72249-118">**Stop**</span></span>](stop-method.md)
-   [<span data-ttu-id="72249-119">**Do opAll**</span><span class="sxs-lookup"><span data-stu-id="72249-119">**StopAll**</span></span>](stopall-method.md)
-   [<span data-ttu-id="72249-120">**Pensar**</span><span class="sxs-lookup"><span data-stu-id="72249-120">**Think**</span></span>](think-method.md)
-   [<span data-ttu-id="72249-121">**Aguarde**</span><span class="sxs-lookup"><span data-stu-id="72249-121">**Wait**</span></span>](wait-method.md)

<span data-ttu-id="72249-122">Para usar um método, referencie o caractere na coleção.</span><span class="sxs-lookup"><span data-stu-id="72249-122">To use a method, reference the character in the collection.</span></span> <span data-ttu-id="72249-123">No VBScript e Visual Basic, você faz isso especificando a ID de um caractere:</span><span class="sxs-lookup"><span data-stu-id="72249-123">In VBScript and Visual Basic, you do this by specifying the ID for a character:</span></span>


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



<span data-ttu-id="72249-124">Para simplificar a sintaxe do seu código, você pode definir uma variável de objeto e defini-la para fazer referência a um objeto de caractere na coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) ; em seguida, você pode usar a variável para referenciar métodos ou propriedades do caractere.</span><span class="sxs-lookup"><span data-stu-id="72249-124">To simplify the syntax of your code, you can define an object variable and set it to reference a character object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection; then you can use your variable to reference methods or properties of the character.</span></span> <span data-ttu-id="72249-125">O exemplo a seguir demonstra como você pode fazer isso usando a instrução Visual Basic set:</span><span class="sxs-lookup"><span data-stu-id="72249-125">The following example demonstrates how you can do this using the Visual Basic Set statement:</span></span>


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



<span data-ttu-id="72249-126">No Visual Basic 5,0, você também pode criar sua referência declarando sua variável como um objeto de [**caractere**](/windows/desktop/lwef/the-characters-object):</span><span class="sxs-lookup"><span data-stu-id="72249-126">In Visual Basic 5.0, you can also create your reference by declaring your variable as a [**Character**](/windows/desktop/lwef/the-characters-object)object:</span></span>


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



<span data-ttu-id="72249-127">Declarar o objeto do tipo IAgentCtlCharacterEx habilita a ligação antecipada no objeto, o que resulta em um melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="72249-127">Declaring your object of type IAgentCtlCharacterEx enables early binding on the object, which results in better performance.</span></span>

<span data-ttu-id="72249-128">No VBScript, você não pode declarar uma referência como um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="72249-128">In VBScript, you cannot declare a reference as a particular type.</span></span> <span data-ttu-id="72249-129">No entanto, você pode simplesmente declarar a referência de variável:</span><span class="sxs-lookup"><span data-stu-id="72249-129">However, you can simply declare the variable reference:</span></span>


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



<span data-ttu-id="72249-130">Algumas linguagens de programação não dão suporte a coleções.</span><span class="sxs-lookup"><span data-stu-id="72249-130">Some programming languages do not support collections.</span></span> <span data-ttu-id="72249-131">No entanto, você pode acessar os métodos de um objeto [**Character**](/windows/desktop/lwef/the-characters-object) com o método [**Character**](character-method.md) :</span><span class="sxs-lookup"><span data-stu-id="72249-131">However, you can access a [**Character**](/windows/desktop/lwef/the-characters-object) object's methods with the [**Character**](character-method.md) method:</span></span>


```
   agent.Characters.Character("CharacterID").method
```



<span data-ttu-id="72249-132">Além disso, você também pode criar uma referência ao objeto [**Character**](/windows/desktop/lwef/the-characters-object) para tornar o código de script mais fácil de seguir:</span><span class="sxs-lookup"><span data-stu-id="72249-132">In addition, you can also create a reference to the [**Character**](/windows/desktop/lwef/the-characters-object) object to make your script code easier to follow:</span></span>


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



 

 