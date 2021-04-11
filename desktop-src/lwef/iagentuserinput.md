---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365934"
---
# <a name="iagentuserinput"></a><span data-ttu-id="dac08-103">IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="dac08-103">IAgentUserInput</span></span>

<span data-ttu-id="dac08-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dac08-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="dac08-105">Quando o servidor notifica o cliente de entrada-ativo com [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), ele retorna informações por meio do objeto [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="dac08-105">When the server notifies the input-active client with [**IAgentNotifySink::Command**](iagentnotifysink--command.md), it returns information through the [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="dac08-106">**IAgentUserInput** define uma interface que permite que os aplicativos consultem esses valores.</span><span class="sxs-lookup"><span data-stu-id="dac08-106">**IAgentUserInput** defines an interface that allows applications to query these values.</span></span>

<span data-ttu-id="dac08-107">**Métodos em ordem vtable**</span><span class="sxs-lookup"><span data-stu-id="dac08-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="dac08-108">Métodos IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="dac08-108">IAgentUserInput Methods</span></span>                                         | <span data-ttu-id="dac08-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="dac08-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dac08-110">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="dac08-110">**GetCount**</span></span>](iagentuserinput--getcount.md)                   | <span data-ttu-id="dac08-111">Retorna o número de alternativas de comando retornadas em um evento de [**comando**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="dac08-111">Returns the number of command alternatives returned in a [**Command**](command-event.md) event.</span></span>                                         |
| [<span data-ttu-id="dac08-112">**Getitemid**</span><span class="sxs-lookup"><span data-stu-id="dac08-112">**GetItemID**</span></span>](iagentuserinput--getitemid.md)                 | <span data-ttu-id="dac08-113">Retorna a ID para uma alternativa de [**comando**](command-event.md) específico.</span><span class="sxs-lookup"><span data-stu-id="dac08-113">Returns the ID for a specific [**Command**](command-event.md) alternative.</span></span>                                                              |
| [<span data-ttu-id="dac08-114">**GetItemConfidence**</span><span class="sxs-lookup"><span data-stu-id="dac08-114">**GetItemConfidence**</span></span>](iagentuserinput--getitemconfidence.md) | <span data-ttu-id="dac08-115">Retorna o valor da propriedade [**int**](confidence-property.md) para uma alternativa de [**comando**](command-event.md) específico.</span><span class="sxs-lookup"><span data-stu-id="dac08-115">Returns the value of the [**Confidence**](confidence-property.md) property for a specific [**Command**](command-event.md) alternative.</span></span> |
| [<span data-ttu-id="dac08-116">**GetItemText**</span><span class="sxs-lookup"><span data-stu-id="dac08-116">**GetItemText**</span></span>](iagentuserinput--getitemtext.md)             | <span data-ttu-id="dac08-117">Retorna o valor do texto de [**voz**](voice-property.md) para uma alternativa de [**comando**](command-event.md) específico.</span><span class="sxs-lookup"><span data-stu-id="dac08-117">Returns the value of [**Voice**](voice-property.md) text for a specific [**Command**](command-event.md) alternative.</span></span>                   |
| [<span data-ttu-id="dac08-118">**GetAllItemData**</span><span class="sxs-lookup"><span data-stu-id="dac08-118">**GetAllItemData**</span></span>](iagentuserinput--getallitemdata.md)       | <span data-ttu-id="dac08-119">Retorna os dados para todas as alternativas de [**comando**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="dac08-119">Returns the data for all [**Command**](command-event.md) alternatives.</span></span>                                                                  |



 

 

 