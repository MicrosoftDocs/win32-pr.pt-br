---
title: IAgentCommandsEx getidentificaçãodocontextodaajuda
description: IAgentCommandsEx getidentificaçãodocontextodaajuda
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007466"
---
# <a name="iagentcommandsexgethelpcontextid"></a><span data-ttu-id="ae153-103">IAgentCommandsEx:: getidentificaçãodocontextodaajuda</span><span class="sxs-lookup"><span data-stu-id="ae153-103">IAgentCommandsEx::GetHelpContextID</span></span>

<span data-ttu-id="ae153-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae153-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

<span data-ttu-id="ae153-105">Recupera o [**HelpContextId**](helpcontextid-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="ae153-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="ae153-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ae153-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ae153-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span><span class="sxs-lookup"><span data-stu-id="ae153-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="ae153-108">Endereço de uma variável que recebe o número de contexto do tópico da ajuda para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="ae153-108">Address of a variable that receives the context number of the help topic for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="ae153-109">Se você criou um arquivo de ajuda do Windows para seu aplicativo e definiu a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chama automaticamente Help quando [**HelpModeOn**](helpmodeon-property.md) está definido como **true** e o usuário seleciona o objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="ae153-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects your [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="ae153-110">Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual.</span><span class="sxs-lookup"><span data-stu-id="ae153-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="ae153-111">O número de contexto atual é o valor de **HelpContextId** para o objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="ae153-111">The current context number is the value of **HelpContextID** for the **Command** object.</span></span>

<span data-ttu-id="ae153-112">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="ae153-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="ae153-113">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ae153-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ae153-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ae153-114">See Also</span></span>

<span data-ttu-id="ae153-115">[**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="ae153-115">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 