---
description: Os provedores de serviço que dão suporte à abstração OOB (dados fora de banda) para os soquetes de estilo de fluxo devem aderir à semântica nesta seção.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Dados fora de banda no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010483"
---
# <a name="out-of-band-data-in-the-spi"></a><span data-ttu-id="2416d-103">Dados fora de banda no SPI</span><span class="sxs-lookup"><span data-stu-id="2416d-103">Out-of-Band Data in the SPI</span></span>

<span data-ttu-id="2416d-104">Os provedores de serviço que dão suporte à abstração OOB (dados fora de banda) para os soquetes de estilo de fluxo devem aderir à semântica nesta seção.</span><span class="sxs-lookup"><span data-stu-id="2416d-104">The service providers which support the out-of-band data (OOB) abstraction for the stream-style sockets must adhere to the semantics in this section.</span></span> <span data-ttu-id="2416d-105">Descreveremos a manipulação de dados OOB de maneira independente de protocolo.</span><span class="sxs-lookup"><span data-stu-id="2416d-105">We will describe OOB data handling in a protocol-independent manner.</span></span> <span data-ttu-id="2416d-106">Consulte os anexos do [Winsock](winsock-annexes.md) para obter uma discussão sobre os dados OOB implementados usando dados urgentes em provedores de serviços TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2416d-106">Please refer to the [Winsock Annexes](winsock-annexes.md) for a discussion of OOB data implemented using urgent data in TCP/IP service providers.</span></span> <span data-ttu-id="2416d-107">A seguir, o uso de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) também se aplica a [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2416d-107">In the following, the use of [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) also applies to [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span></span>

 

 
