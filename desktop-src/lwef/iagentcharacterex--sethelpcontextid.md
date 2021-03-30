---
title: IAgentCharacterEx setidentificaçãodocontextodaajuda
description: IAgentCharacterEx setidentificaçãodocontextodaajuda
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635389"
---
# <a name="iagentcharacterexsethelpcontextid"></a><span data-ttu-id="78e60-103">IAgentCharacterEx:: setidentificaçãodocontextodaajuda</span><span class="sxs-lookup"><span data-stu-id="78e60-103">IAgentCharacterEx::SetHelpContextID</span></span>

<span data-ttu-id="78e60-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="78e60-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="78e60-105">Define o [**HelpContextId**](helpcontextid-property.md) para o caractere.</span><span class="sxs-lookup"><span data-stu-id="78e60-105">Sets the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="78e60-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="78e60-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="78e60-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="78e60-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="78e60-108">O número de contexto do tópico da ajuda para associado a um caractere; usado para fornecer ajuda contextual para o caractere.</span><span class="sxs-lookup"><span data-stu-id="78e60-108">The context number of the help topic for associated with a character; used to provide context-sensitive Help for the character.</span></span>

</dd> </dl>

<span data-ttu-id="78e60-109">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e defini-lo na propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário selecionar o caractere.</span><span class="sxs-lookup"><span data-stu-id="78e60-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="78e60-110">Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual.</span><span class="sxs-lookup"><span data-stu-id="78e60-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="78e60-111">O número de contexto atual é o valor de **HelpContextId** para o caractere.</span><span class="sxs-lookup"><span data-stu-id="78e60-111">The current context number is the value of **HelpContextID** for the character.</span></span> <span data-ttu-id="78e60-112">Se houver um número de contexto na propriedade **HelpContextId** , a ajuda exibirá um tópico correspondente ao contexto de ajuda atual; caso contrário, ele exibirá "nenhum tópico da ajuda associado a este item".</span><span class="sxs-lookup"><span data-stu-id="78e60-112">If there is a context number in the **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="78e60-113">Essa configuração se aplica somente quando o aplicativo cliente é o cliente ativo do caractere superior.</span><span class="sxs-lookup"><span data-stu-id="78e60-113">This setting applies only when your client application is the active client of the topmost character.</span></span> <span data-ttu-id="78e60-114">Ele não afeta outros clientes do caractere ou outros caracteres que seu aplicativo cliente está usando.</span><span class="sxs-lookup"><span data-stu-id="78e60-114">It does not affect other clients of the character or other characters that your client application is using.</span></span>

> [!Note]  
> <span data-ttu-id="78e60-115">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="78e60-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="78e60-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="78e60-116">See Also</span></span>

<span data-ttu-id="78e60-117">[**IAgentCharacterEx:: getidentificaçãodocontextodaajuda**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="78e60-117">[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




