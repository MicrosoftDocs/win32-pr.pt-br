---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120909"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="a62ba-103">IAgentCharacter:: stopAll</span><span class="sxs-lookup"><span data-stu-id="a62ba-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="a62ba-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a62ba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="a62ba-105">Interrompe todas as animações (solicitações) e as remove da fila de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="a62ba-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="a62ba-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="a62ba-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="a62ba-107">Um campo de bits que indica os tipos de solicitações a serem interrompidas (e removidas da fila de caracteres), compostas a partir do seguinte:</span><span class="sxs-lookup"><span data-stu-id="a62ba-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



| <span data-ttu-id="a62ba-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a62ba-108">Value</span></span>                                                                                  |  <span data-ttu-id="a62ba-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a62ba-109">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a62ba-110">const tipo de interrupção **longa não assinado** **\_ \_ tudo = 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="a62ba-110">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="a62ba-111">Interrompe todas as solicitações de animação, incluindo solicitações de [**preparação**](iagentcharacter--prepare.md) não enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="a62ba-111">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="a62ba-112">**const** **\_ tipo \_** longo de parada não assinado</span><span class="sxs-lookup"><span data-stu-id="a62ba-112">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="a62ba-113">Interrompe todas as solicitações de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a62ba-113">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="a62ba-114">const de tipo de interrupção **longa não assinado constante** **\_ \_ mover = 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="a62ba-114">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="a62ba-115">Interrompe todas as solicitações de [**movimentação**](https://www.bing.com/search?q=**Move**) .</span><span class="sxs-lookup"><span data-stu-id="a62ba-115">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="a62ba-116">const tipo de interrupção **longa não assinado** , **\_ \_ Fale = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="a62ba-116">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="a62ba-117">Interrompe todas as solicitações de [**fala**](iagentcharacter--speak.md) .</span><span class="sxs-lookup"><span data-stu-id="a62ba-117">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="a62ba-118">**const tipo longo de parada sem sinal de constante** **\_ \_ Prepare = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="a62ba-118">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="a62ba-119">Interrompe todas as solicitações de [**preparação**](iagentcharacter--prepare.md) enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="a62ba-119">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="a62ba-120">**const tipo longo de interrupção não assinado** **\_ \_ NONQUEUEDPREPARE = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="a62ba-120">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="a62ba-121">Interrompe todas as solicitações de [**preparação**](iagentcharacter--prepare.md) não enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="a62ba-121">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="a62ba-122">const tipo de interrupção **longa sem sinal** **\_ \_ visível = 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="a62ba-122">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="a62ba-123">Interrompe todas as solicitações de [**ocultar**](iagentcharacter--hide.md) ou [**Mostrar**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="a62ba-123">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a62ba-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a62ba-124">See Also</span></span>

[<span data-ttu-id="a62ba-125">**IAgentCharacter:: Stop**</span><span class="sxs-lookup"><span data-stu-id="a62ba-125">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





