---
title: Gravando código de evento
description: Gravando código de evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Capas do Windows Media Player, escrevendo código
- capas, escrevendo código
- eventos, escrevendo código
- escrevendo código para capas, sobre
- Capas, eventos do Windows Media Player
- capas, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006125"
---
# <a name="writing-event-code"></a><span data-ttu-id="fbd26-109">Gravando código de evento</span><span class="sxs-lookup"><span data-stu-id="fbd26-109">Writing Event Code</span></span>

<span data-ttu-id="fbd26-110">Os eventos são tratados de forma semelhante aos atributos.</span><span class="sxs-lookup"><span data-stu-id="fbd26-110">Events are treated similarly to attributes.</span></span> <span data-ttu-id="fbd26-111">Você deve dar um valor ao evento e o valor é o código que você deseja executar quando o evento acontece.</span><span class="sxs-lookup"><span data-stu-id="fbd26-111">You must give the event a value, and the value is the code you want to run when the event happens.</span></span> <span data-ttu-id="fbd26-112">A palavra "on" é adicionada à frente do nome do evento; por exemplo, o evento de clique ficará **onclick**.</span><span class="sxs-lookup"><span data-stu-id="fbd26-112">The word "on" is added to the front of the event name; for example, the click event will become **onclick**.</span></span>

<span data-ttu-id="fbd26-113">O valor do evento está entre aspas duplas e começa com a palavra JScript seguida por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="fbd26-113">The event value is in double quotes and starts with the word JScript followed by a colon.</span></span> <span data-ttu-id="fbd26-114">O código que você deseja executar vem em seguida, seguido por um ponto e vírgula e as aspas duplas de fechamento.</span><span class="sxs-lookup"><span data-stu-id="fbd26-114">The code you want to run comes next, followed by a semicolon and the closing double quotes.</span></span> <span data-ttu-id="fbd26-115">Por exemplo, para interromper a reprodução quando o usuário clica em um botão, digite o seguinte como um atributo no código do elemento **Button** :</span><span class="sxs-lookup"><span data-stu-id="fbd26-115">For example, to stop playing when the user clicks on a button, type the following as an attribute in your **BUTTON** element code:</span></span>


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



<span data-ttu-id="fbd26-116">Se você tiver um código que requer aspas, use aspas simples.</span><span class="sxs-lookup"><span data-stu-id="fbd26-116">If you have a code that requires quotes, use single quotes.</span></span> <span data-ttu-id="fbd26-117">É necessário tomar cuidado ao usar aspas para que elas sejam balanceadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="fbd26-117">Care must be taken when using quotation marks so that they are balanced properly.</span></span> <span data-ttu-id="fbd26-118">Veja um exemplo de como usar os dois tipos:</span><span class="sxs-lookup"><span data-stu-id="fbd26-118">Here is an example of using both types:</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



<span data-ttu-id="fbd26-119">Você também pode alterar os atributos da sua aparência ao manipular um evento externo.</span><span class="sxs-lookup"><span data-stu-id="fbd26-119">You can also change attributes of your skin when handling an external event.</span></span> <span data-ttu-id="fbd26-120">Por exemplo, para fechar um modo de exibição chamado MyView, você poderia digitar:</span><span class="sxs-lookup"><span data-stu-id="fbd26-120">For example, to close a view named myView, you could type:</span></span>


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a><span data-ttu-id="fbd26-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fbd26-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbd26-122">**Manipulando eventos**</span><span class="sxs-lookup"><span data-stu-id="fbd26-122">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




