---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641034"
---
# <a name="iagentcommandsremoveall"></a><span data-ttu-id="53d6c-103">IAgentCommands:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="53d6c-103">IAgentCommands::RemoveAll</span></span>

<span data-ttu-id="53d6c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53d6c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove();
```

<span data-ttu-id="53d6c-105">Remove todos os [**comandos**](/windows/desktop/lwef/the-command-object) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="53d6c-105">Removes all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="53d6c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="53d6c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="53d6c-107">A remoção de todos os [**comandos**](/windows/desktop/lwef/the-command-object) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) também os remove do menu pop-up e da **janela de comandos de voz** quando seu aplicativo está em entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="53d6c-107">Removing all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes them from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span> <span data-ttu-id="53d6c-108">**RemoveAll** não remove as entradas do servidor ou do outro cliente.</span><span class="sxs-lookup"><span data-stu-id="53d6c-108">**RemoveAll** does not remove server or other client's entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="53d6c-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="53d6c-109">See Also</span></span>

<span data-ttu-id="53d6c-110">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="53d6c-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 