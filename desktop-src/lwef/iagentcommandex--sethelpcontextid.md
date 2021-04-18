---
title: IAgentCommandEx setidentificaçãodocontextodaajuda
description: IAgentCommandEx setidentificaçãodocontextodaajuda
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105781194"
---
# <a name="iagentcommandexsethelpcontextid"></a><span data-ttu-id="6463b-103">IAgentCommandEx:: setidentificaçãodocontextodaajuda</span><span class="sxs-lookup"><span data-stu-id="6463b-103">IAgentCommandEx::SetHelpContextID</span></span>

<span data-ttu-id="6463b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6463b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

<span data-ttu-id="6463b-105">Define o [**HelpContextId**](helpcontextid-property-com.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="6463b-105">Sets the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="6463b-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6463b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6463b-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span><span class="sxs-lookup"><span data-stu-id="6463b-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span></span>
</dt> <dd>

<span data-ttu-id="6463b-108">O número de contexto do tópico da ajuda associado ao objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; usado para fornecer ajuda contextual para o comando.</span><span class="sxs-lookup"><span data-stu-id="6463b-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="6463b-109">Se você criou um arquivo de ajuda do Windows para seu aplicativo e o definiu na propriedade [**HelpFile**](helpfile-property.md) do caractere.</span><span class="sxs-lookup"><span data-stu-id="6463b-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="6463b-110">O Microsoft Agent chama automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) é definido como **true** e o usuário seleciona o comando.</span><span class="sxs-lookup"><span data-stu-id="6463b-110">Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="6463b-111">Se houver um número de contexto em [**HelpContextId**](helpcontextid-property-com.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual.</span><span class="sxs-lookup"><span data-stu-id="6463b-111">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="6463b-112">O número de contexto atual é o valor de **HelpContextId** para o comando.</span><span class="sxs-lookup"><span data-stu-id="6463b-112">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="6463b-113">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6463b-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6463b-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6463b-114">See Also</span></span>

<span data-ttu-id="6463b-115">[**IAgentCommandEx:: getidentificaçãodocontextodaajuda**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="6463b-115">[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 