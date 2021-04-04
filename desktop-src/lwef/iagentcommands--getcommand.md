---
title: IAgentCommands GetCommand
description: IAgentCommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e81043bb8dbe8a6d050f226d09f03b396d0f8f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007539"
---
# <a name="iagentcommandsgetcommand"></a><span data-ttu-id="e6f30-103">IAgentCommands:: GetCommand</span><span class="sxs-lookup"><span data-stu-id="e6f30-103">IAgentCommands::GetCommand</span></span>

<span data-ttu-id="e6f30-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6f30-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

<span data-ttu-id="e6f30-105">Recupera um objeto de [**comando**](/windows/desktop/lwef/the-command-object) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e6f30-105">Retrieves a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="e6f30-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e6f30-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e6f30-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="e6f30-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="e6f30-108">A ID de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) na coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e6f30-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) object in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="e6f30-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="e6f30-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="e6f30-110">O endereço da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="e6f30-110">The address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e6f30-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e6f30-111">See Also</span></span>

[<span data-ttu-id="e6f30-112">**IAgentCommand**</span><span class="sxs-lookup"><span data-stu-id="e6f30-112">**IAgentCommand**</span></span>](iagentcommand.md)


 

 