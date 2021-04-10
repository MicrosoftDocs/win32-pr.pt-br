---
title: Sobre o IMFGetService
description: Sobre o IMFGetService
ms.assetid: c71b1362-a596-42e5-b894-f8a3c0e70140
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
- Plug-ins do Windows Media Player, interface IMFGetService
- plug-ins, interface IMFGetService
- plug-ins de processamento de sinal digital, interface IMFGetService
- Plug-ins do DSP, interface IMFGetService
- Interface IMFGetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235b616afe48db9ae772da1f1d74c4f7de1a74a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291856"
---
# <a name="about-imfgetservice"></a><span data-ttu-id="ea540-113">Sobre o IMFGetService</span><span class="sxs-lookup"><span data-stu-id="ea540-113">About IMFGetService</span></span>

<span data-ttu-id="ea540-114">A interface **IMFGetService** é uma das interfaces que devem ser implementadas por um plug-in DSP de modo duplo.</span><span class="sxs-lookup"><span data-stu-id="ea540-114">The **IMFGetService** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="ea540-115">Ele tem apenas um método, **GetService**.</span><span class="sxs-lookup"><span data-stu-id="ea540-115">It has only one method, **GetService**.</span></span> <span data-ttu-id="ea540-116">Um plug-in do DSP implementa o método **GetService** para que os clientes possam obter ponteiros para as interfaces com suporte do plug-in quando o plug-in estiver sendo executado nativamente no pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ea540-116">A DSP plug-in implements the **GetService** method so that clients can obtain pointers to the interfaces supported by the plug-in when the plug-in is running natively in the Media Foundation pipeline.</span></span>

 

 




