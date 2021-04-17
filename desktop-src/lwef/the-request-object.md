---
title: O objeto de solicitação
description: O objeto de solicitação
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105763044"
---
# <a name="the-request-object"></a><span data-ttu-id="4d459-103">O objeto de solicitação</span><span class="sxs-lookup"><span data-stu-id="4d459-103">The Request Object</span></span>

<span data-ttu-id="4d459-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d459-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4d459-105">O servidor processa alguns métodos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4d459-105">The server processes some methods asynchronously.</span></span> <span data-ttu-id="4d459-106">Isso permite que o código do aplicativo continue enquanto o método está sendo concluído.</span><span class="sxs-lookup"><span data-stu-id="4d459-106">This enables your application code to continue while the method is completing.</span></span> <span data-ttu-id="4d459-107">Quando um aplicativo cliente chama um desses métodos, o controle cria e retorna um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4d459-107">When a client application calls one of these methods, the control creates and returns a [**Request**](/windows/desktop/lwef/the-request-object) object for the request.</span></span> <span data-ttu-id="4d459-108">Você pode usar o objeto de **solicitação** para acompanhar o status do método atribuindo uma variável de objeto ao método.</span><span class="sxs-lookup"><span data-stu-id="4d459-108">You can use the **Request** object to track the status of the method by assigning an object variable to the method.</span></span> <span data-ttu-id="4d459-109">Em Visual Basic, primeiro declare uma variável de objeto:</span><span class="sxs-lookup"><span data-stu-id="4d459-109">In Visual Basic, first declare an object variable:</span></span>


```
   Dim MyRequest as Object
```



<span data-ttu-id="4d459-110">No VBScript, você não inclui o tipo de variável em sua declaração:</span><span class="sxs-lookup"><span data-stu-id="4d459-110">In VBScript, you don't include the variable type in your declaration:</span></span>


```
   Dim MyRequest
```



<span data-ttu-id="4d459-111">E use a instrução SET do Visual Basic para atribuir a variável à chamada do método:</span><span class="sxs-lookup"><span data-stu-id="4d459-111">And use Visual Basic's Set statement to assign the variable to the method call:</span></span>


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



<span data-ttu-id="4d459-112">Isso adiciona uma referência ao objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="4d459-112">This adds a reference to the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="4d459-113">O objeto de **solicitação** será destruído quando não houver mais referências a ele.</span><span class="sxs-lookup"><span data-stu-id="4d459-113">The **Request** object will be destroyed when there are no more references to it.</span></span> <span data-ttu-id="4d459-114">Onde você declara o objeto de **solicitação** e como usá-lo determina seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="4d459-114">Where you declare the **Request** object and how you use it determines its lifetime.</span></span> <span data-ttu-id="4d459-115">Se o objeto for declarado local para uma sub-rotina ou função, ele será destruído quando sair do escopo; ou seja, quando a sub-rotina ou a função termina.</span><span class="sxs-lookup"><span data-stu-id="4d459-115">If the object is declared local to a subroutine or function, it will be destroyed when it goes out of scope; that is, when the subroutine or function ends.</span></span> <span data-ttu-id="4d459-116">Se o objeto for declarado globalmente, ele não será destruído até que o programa seja encerrado ou um novo valor (ou um valor definido como "Empty") seja atribuído ao objeto.</span><span class="sxs-lookup"><span data-stu-id="4d459-116">If the object is declared globally, it will not be destroyed until either the program terminates or a new value (or a value set to "empty") is assigned to the object.</span></span>

<span data-ttu-id="4d459-117">O objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) fornece várias propriedades que você pode consultar.</span><span class="sxs-lookup"><span data-stu-id="4d459-117">The [**Request**](/windows/desktop/lwef/the-request-object) object provides several properties you can query.</span></span> <span data-ttu-id="4d459-118">Por exemplo, a propriedade [**status**](status-property.md) retorna o status atual da solicitação.</span><span class="sxs-lookup"><span data-stu-id="4d459-118">For example, the [**Status**](status-property.md) property returns the current status of the request.</span></span> <span data-ttu-id="4d459-119">Você pode usar essa propriedade para verificar o status da sua solicitação:</span><span class="sxs-lookup"><span data-stu-id="4d459-119">You can use this property to check the status of your request:</span></span>


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



<span data-ttu-id="4d459-120">A propriedade [**status**](status-property.md) retorna o status de um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) como um valor inteiro longo.</span><span class="sxs-lookup"><span data-stu-id="4d459-120">The [**Status**](status-property.md) property returns the status of a [**Request**](/windows/desktop/lwef/the-request-object) object as a Long integer value.</span></span>



| <span data-ttu-id="4d459-121">Status</span><span class="sxs-lookup"><span data-stu-id="4d459-121">Status</span></span> | <span data-ttu-id="4d459-122">Definição</span><span class="sxs-lookup"><span data-stu-id="4d459-122">Definition</span></span>                                        |
|--------|---------------------------------------------------|
| <span data-ttu-id="4d459-123">0</span><span class="sxs-lookup"><span data-stu-id="4d459-123">0</span></span>      | <span data-ttu-id="4d459-124">Solicitação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="4d459-124">Request successfully completed.</span></span>                   |
| <span data-ttu-id="4d459-125">1</span><span class="sxs-lookup"><span data-stu-id="4d459-125">1</span></span>      | <span data-ttu-id="4d459-126">Falha na solicitação.</span><span class="sxs-lookup"><span data-stu-id="4d459-126">Request failed.</span></span>                                   |
| <span data-ttu-id="4d459-127">2</span><span class="sxs-lookup"><span data-stu-id="4d459-127">2</span></span>      | <span data-ttu-id="4d459-128">Solicitação pendente (na fila, mas não concluída).</span><span class="sxs-lookup"><span data-stu-id="4d459-128">Request pending (in the queue, but not complete).</span></span> |
| <span data-ttu-id="4d459-129">3</span><span class="sxs-lookup"><span data-stu-id="4d459-129">3</span></span>      | <span data-ttu-id="4d459-130">Solicitação interrompida.</span><span class="sxs-lookup"><span data-stu-id="4d459-130">Request interrupted.</span></span>                              |
| <span data-ttu-id="4d459-131">4</span><span class="sxs-lookup"><span data-stu-id="4d459-131">4</span></span>      | <span data-ttu-id="4d459-132">Solicitação em andamento.</span><span class="sxs-lookup"><span data-stu-id="4d459-132">Request in progress.</span></span>                              |



 

<span data-ttu-id="4d459-133">O objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) também inclui um valor inteiro longo na propriedade [**Number**](https://www.bing.com/search?q=**Number**) que retorna o erro ou a causa do código de [**status**](status-property.md) .</span><span class="sxs-lookup"><span data-stu-id="4d459-133">The [**Request**](/windows/desktop/lwef/the-request-object) object also includes a Long integer value in the [**Number**](https://www.bing.com/search?q=**Number**) property that returns the error or cause of the [**Status**](status-property.md) code.</span></span> <span data-ttu-id="4d459-134">Se nenhum, esse valor será zero (0).</span><span class="sxs-lookup"><span data-stu-id="4d459-134">If none, this value is zero (0).</span></span> <span data-ttu-id="4d459-135">A propriedade [**Description**](description-property.md) contém um valor de cadeia de caracteres que corresponde ao número do erro.</span><span class="sxs-lookup"><span data-stu-id="4d459-135">The [**Description**](description-property.md) property contains a string value that corresponds to the error number.</span></span> <span data-ttu-id="4d459-136">Se a cadeia de caracteres não existir, a **Descrição** conterá "erro definido pelo aplicativo ou definido pelo objeto".</span><span class="sxs-lookup"><span data-stu-id="4d459-136">If the string doesn't exist, **Description** contains "Application-defined or object-defined error".</span></span>

<span data-ttu-id="4d459-137">Para obter os valores e o significado retornados pela propriedade [**Number**](https://www.bing.com/search?q=**Number**) , consulte [códigos de erro](microsoft-agent-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4d459-137">For the values and meaning returned by the [**Number**](https://www.bing.com/search?q=**Number**) property, see [Error Codes](microsoft-agent-error-codes.md).</span></span>

<span data-ttu-id="4d459-138">O servidor coloca as solicitações de animação na fila do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="4d459-138">The server places animation requests in the specified character's queue.</span></span> <span data-ttu-id="4d459-139">Isso permite que o servidor reproduza a animação em um thread separado, e o código do aplicativo pode continuar enquanto as animações são reproduzidas.</span><span class="sxs-lookup"><span data-stu-id="4d459-139">This enables the server to play the animation on a separate thread, and your application's code can continue while animations play.</span></span> <span data-ttu-id="4d459-140">Se você criar uma referência de objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) , o servidor o notificará automaticamente quando uma solicitação de animação for iniciada ou concluída por meio dos eventos [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) e [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) .</span><span class="sxs-lookup"><span data-stu-id="4d459-140">If you create a [**Request**](/windows/desktop/lwef/the-request-object) object reference, the server automatically notifies you when an animation request has started or completed through the [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) and [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) events.</span></span> <span data-ttu-id="4d459-141">Como os métodos que retornam objetos de **solicitação** são assíncronos e podem não ser concluídos durante o escopo da função de chamada, declare sua referência ao objeto de **solicitação** globalmente.</span><span class="sxs-lookup"><span data-stu-id="4d459-141">Because methods that return **Request** objects are asynchronous and may not complete during the scope of the calling function, declare your reference to the **Request** object globally.</span></span>

<span data-ttu-id="4d459-142">Os métodos a seguir podem ser usados para retornar um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) : [**GestureAt**](gestureat-method.md), [**obter**](get-method.md), [**ocultar**](hide-method.md), [**interromper**](interrupt-method.md), [**carregar**](load-method.md), [**MoveTo**](moveto-method.md), [**reproduzir**](play-method.md), [**Mostrar**](show-method.md), [**falar**](speak-method.md)e [**aguardar**](https://www.bing.com/search?q=**Wait**).</span><span class="sxs-lookup"><span data-stu-id="4d459-142">The following methods can be used to return a [**Request**](/windows/desktop/lwef/the-request-object) object: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md), and [**Wait**](https://www.bing.com/search?q=**Wait**).</span></span>

 

 