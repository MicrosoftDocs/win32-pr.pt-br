---
title: IAgentCharacterEx getidentificaçãodocontextodaajuda
description: IAgentCharacterEx getidentificaçãodocontextodaajuda
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636795"
---
# <a name="iagentcharacterexgethelpcontextid"></a><span data-ttu-id="03cec-103">IAgentCharacterEx:: getidentificaçãodocontextodaajuda</span><span class="sxs-lookup"><span data-stu-id="03cec-103">IAgentCharacterEx::GetHelpContextID</span></span>

<span data-ttu-id="03cec-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03cec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

<span data-ttu-id="03cec-105">Recupera o [**HelpContextId**](helpcontextid-property.md) para o caractere.</span><span class="sxs-lookup"><span data-stu-id="03cec-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="03cec-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="03cec-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="03cec-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span><span class="sxs-lookup"><span data-stu-id="03cec-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="03cec-108">Endereço de uma variável que recebe o número de contexto do tópico da ajuda para o caractere.</span><span class="sxs-lookup"><span data-stu-id="03cec-108">Address of a variable that receives the context number of the help topic for the character.</span></span>

</dd> </dl>

<span data-ttu-id="03cec-109">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário selecionar o caractere.</span><span class="sxs-lookup"><span data-stu-id="03cec-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="03cec-110">Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual.</span><span class="sxs-lookup"><span data-stu-id="03cec-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="03cec-111">O número de contexto atual é o valor de **HelpContextId** para o caractere.</span><span class="sxs-lookup"><span data-stu-id="03cec-111">The current context number is the value of **HelpContextID** for the character.</span></span>

<span data-ttu-id="03cec-112">**IAgentCharacterEx:: getidentificaçãodocontextodaajuda** retorna o [**HelpContextId**](helpcontextid-property.md) definido para o caractere.</span><span class="sxs-lookup"><span data-stu-id="03cec-112">**IAgentCharacterEx::GetHelpContextID** returns the [**HelpContextID**](helpcontextid-property.md) you set for the character.</span></span> <span data-ttu-id="03cec-113">Ele não retorna o **HelpContextId** definido por outros clientes.</span><span class="sxs-lookup"><span data-stu-id="03cec-113">It does not return the **HelpContextID** set by other clients.</span></span>

> [!Note]  
> <span data-ttu-id="03cec-114">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="03cec-114">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="03cec-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="03cec-115">See Also</span></span>

<span data-ttu-id="03cec-116">[**IAgentCharacterEx:: setidentificaçãodocontextodaajuda**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="03cec-116">[**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




