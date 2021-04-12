---
title: Acessando os métodos, as propriedades e os eventos dos controles
description: Acessando os métodos, as propriedades e os eventos dos controles
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363931"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a><span data-ttu-id="a6e06-103">Acessando os métodos, as propriedades e os eventos dos controles</span><span class="sxs-lookup"><span data-stu-id="a6e06-103">Accessing the Controls Methods, Properties, and Events</span></span>

<span data-ttu-id="a6e06-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a6e06-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a6e06-105">Usar o controle do Microsoft Agent com o Visual Basic é muito semelhante ao uso do controle com o VBScript, exceto pelo fato de que os eventos em Visual Basic devem incluir o tipo de dados dos parâmetros passados.</span><span class="sxs-lookup"><span data-stu-id="a6e06-105">Using Microsoft Agent's control with Visual Basic is very similar to using the control with VBScript, except that events in Visual Basic must include the data type of passed parameters.</span></span> <span data-ttu-id="a6e06-106">Adicionar o controle do Microsoft Agent a um formulário incluirá automaticamente os eventos do Microsoft Agent com seus parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="a6e06-106">Adding the Microsoft Agent control to a form will automatically include Microsoft Agent's events with their appropriate parameters.</span></span> <span data-ttu-id="a6e06-107">Ele também criará automaticamente uma conexão com o servidor do agente quando o aplicativo for executado.</span><span class="sxs-lookup"><span data-stu-id="a6e06-107">It will also automatically create a connection to the Agent server when the application runs.</span></span>

<span data-ttu-id="a6e06-108">Você também pode usar a sintaxe de criação de object's da linguagem de programação para criar uma instância do controle em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a6e06-108">You may also be able to use your programming language's object's creation syntax to create an instance of the control at runtime.</span></span> <span data-ttu-id="a6e06-109">Por exemplo, no Visual Basic (5,0 ou posterior), se você incluir o controle do Microsoft Agent 2,0 nas referências do seu projeto, poderá usar um [**com eventos**](https://www.bing.com/search?q=**With+Events**).. [**Nova**](https://www.bing.com/search?q=**New**) declaração.</span><span class="sxs-lookup"><span data-stu-id="a6e06-109">For example, in Visual Basic (5.0 or later), if you include the Microsoft Agent 2.0 Control in your project's references, you can use a [**With Events**](https://www.bing.com/search?q=**With+Events**)..[**New**](https://www.bing.com/search?q=**New**) declaration.</span></span> <span data-ttu-id="a6e06-110">Se você não incluir a referência, o VB gerará um erro indicando que o Microsoft Agent não pôde ser iniciado (código de erro 80042502).</span><span class="sxs-lookup"><span data-stu-id="a6e06-110">If you do not include the reference, VB raises an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

<span data-ttu-id="a6e06-111">Para versões do VB anteriores a 5,0, você pode usar a palavra-chave [**New**](https://www.bing.com/search?q=**New**) do VB sem declaração [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) ou a função do VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) , mas essas convenções não expõem os eventos do controle do agente.</span><span class="sxs-lookup"><span data-stu-id="a6e06-111">For versions of VB prior to 5.0, you can use the VB [**New**](https://www.bing.com/search?q=**New**) keyword without [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) declaration or the VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) function, but these conventions will not expose the Agent control's events.</span></span> <span data-ttu-id="a6e06-112">Você também precisa usar a propriedade [**Connected**](https://www.bing.com/search?q=**Connected**) antes de fazer referência a qualquer método ou Propriedade do agente.</span><span class="sxs-lookup"><span data-stu-id="a6e06-112">You also need to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property before you reference any Agent methods or properties.</span></span> <span data-ttu-id="a6e06-113">Se isso não for feito, o VB gerará um erro indicando que o Microsoft Agent não pôde ser iniciado (código de erro 80042502).</span><span class="sxs-lookup"><span data-stu-id="a6e06-113">If this is not done, VB will raise an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

<span data-ttu-id="a6e06-114">Da mesma forma, para outras linguagens de programação, você pode precisar usar a propriedade [**Connected**](https://www.bing.com/search?q=**Connected**) para estabelecer uma conexão com o servidor de Component Object Model de agente (com) antes que seu código possa chamar qualquer um dos métodos ou propriedades do controle Agent.</span><span class="sxs-lookup"><span data-stu-id="a6e06-114">Similarly for other programming languages, you may have to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property to establish a connection to the Agent Component Object Model (COM) server before your code can call any of the Agent control's methods or properties.</span></span> <span data-ttu-id="a6e06-115">Além disso, para algumas linguagens de programação, os métodos e as propriedades do agente podem não ser expostos diretamente, a menos que você declare o controle de agente usando seu tipo.</span><span class="sxs-lookup"><span data-stu-id="a6e06-115">In addition, for some programming languages, Agent's methods and properties may not be directly exposed unless you declare the Agent control using its type.</span></span> <span data-ttu-id="a6e06-116">Por exemplo, no Microsoft Access 97, você precisará declarar o objeto como agente de tipo para ver os métodos e as propriedades exibidos na caixa suspensa Listar Membros automaticamente ao digitar.</span><span class="sxs-lookup"><span data-stu-id="a6e06-116">For example, in Microsoft Access 97, you will need to declare the object as type Agent to see the methods and properties display in the Auto List Members drop-down box when you type.</span></span>

<span data-ttu-id="a6e06-117">A maioria das linguagens de programação que dão suporte a controles ActiveX segue convenções semelhantes a Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a6e06-117">Most programming languages that support ActiveX controls follow conventions similar to Visual Basic.</span></span> <span data-ttu-id="a6e06-118">Para linguagens de programação que não dão suporte a coleções de objetos, você pode usar o método de [**caractere**](https://www.bing.com/search?q=**Character**) e o método de [**comando**](https://www.bing.com/search?q=**Command**) para acessar métodos e propriedades de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="a6e06-118">For programming languages that do not support object collections, you can use the [**Character**](https://www.bing.com/search?q=**Character**) method and [**Command**](https://www.bing.com/search?q=**Command**) method to access methods and properties of items in the collection.</span></span>

<span data-ttu-id="a6e06-119">Linguagens de programação como Visual Basic, que fornecem acesso aos tipos de objeto expostos pelo controle Agent, permitem que você as use em suas declarações de objeto.</span><span class="sxs-lookup"><span data-stu-id="a6e06-119">Programming languages like Visual Basic, that provide access to the object types exposed by the Agent control, enable you to use these in your object declarations.</span></span> <span data-ttu-id="a6e06-120">Por exemplo, em vez de declarar um objeto como um tipo genérico:</span><span class="sxs-lookup"><span data-stu-id="a6e06-120">For example, instead of declaring an object as a generic type:</span></span>

``` syntax
   Dim Genie as Object
```

<span data-ttu-id="a6e06-121">Você pode declarar um objeto como um tipo específico:</span><span class="sxs-lookup"><span data-stu-id="a6e06-121">You can declare an object as a specific type:</span></span>

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

<span data-ttu-id="a6e06-122">Isso pode melhorar o desempenho geral do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6e06-122">This may improve the overall performance of your application.</span></span>

<span data-ttu-id="a6e06-123">Para alguns tipos de objeto, você pode encontrar dois tipos que são iguais, exceto o sufixo "ex".</span><span class="sxs-lookup"><span data-stu-id="a6e06-123">For some object types, you may find two types that are the same except for the "Ex" suffix.</span></span> <span data-ttu-id="a6e06-124">Onde ambos existem, use o tipo "ex" porque isso fornece a funcionalidade completa do Agent.</span><span class="sxs-lookup"><span data-stu-id="a6e06-124">Where both exist, use the "Ex" type because this provides the full functionality of Agent.</span></span> <span data-ttu-id="a6e06-125">As contrapartes não "ex" são incluídas apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a6e06-125">The non-"Ex" counterparts are included only for backward compatibility.</span></span>

 

 




