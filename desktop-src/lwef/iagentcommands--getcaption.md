---
title: IAgentCommands getCaption
description: IAgentCommands getCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105788915"
---
# <a name="iagentcommandsgetcaption"></a><span data-ttu-id="9f620-103">IAgentCommands:: getCaption</span><span class="sxs-lookup"><span data-stu-id="9f620-103">IAgentCommands::GetCaption</span></span>

<span data-ttu-id="9f620-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f620-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

<span data-ttu-id="9f620-105">Recupera a [**legenda**](caption-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="9f620-105">Retrieves the [**Caption**](caption-property.md) for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="9f620-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9f620-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9f620-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span><span class="sxs-lookup"><span data-stu-id="9f620-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="9f620-108">O endereço de um BSTR que recebe o valor da configuração de texto de [**legenda**](caption-property.md) exibida para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="9f620-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text setting displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="9f620-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9f620-109">See Also</span></span>

<span data-ttu-id="9f620-110">[**IAgentCommands:: SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands:: getvisível**](iagentcommands--getvisible.md), [**IAgentCommands:: getvoice**](iagentcommands--getvoice.md)</span><span class="sxs-lookup"><span data-stu-id="9f620-110">[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)</span></span>


 

 