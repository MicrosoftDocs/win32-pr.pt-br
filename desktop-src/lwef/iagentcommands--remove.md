---
title: IAgentCommands remover
description: IAgentCommands remover
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162001"
---
# <a name="iagentcommandsremove"></a><span data-ttu-id="b2fe2-103">IAgentCommands:: Remove</span><span class="sxs-lookup"><span data-stu-id="b2fe2-103">IAgentCommands::Remove</span></span>

<span data-ttu-id="b2fe2-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2fe2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

<span data-ttu-id="b2fe2-105">Remove o [**comando**](/windows/desktop/lwef/the-command-object) especificado de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="b2fe2-105">Removes the specified [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="b2fe2-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b2fe2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b2fe2-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="b2fe2-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="b2fe2-108">A ID de um [**comando**](/windows/desktop/lwef/the-command-object) a ser removido da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="b2fe2-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) to remove from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="b2fe2-109">A remoção de um [**comando**](/windows/desktop/lwef/the-command-object) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) também o Remove do menu pop-up e da **janela de comandos de voz** quando seu aplicativo está em entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="b2fe2-109">Removing a [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes it from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2fe2-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b2fe2-110">See Also</span></span>

<span data-ttu-id="b2fe2-111">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="b2fe2-111">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 