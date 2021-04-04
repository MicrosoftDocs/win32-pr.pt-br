---
description: Depois de determinar como organizar o filtro por meio de uma estrutura CAPTUREFILTER, você deve alocar e preencher a estrutura, que é passada para o driver de Monitor de Rede por meio de um BLOB de configuração.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementando o código de filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837500"
---
# <a name="implementing-the-capture-filter-code"></a><span data-ttu-id="c31ab-103">Implementando o código de filtro de captura</span><span class="sxs-lookup"><span data-stu-id="c31ab-103">Implementing the Capture Filter Code</span></span>

<span data-ttu-id="c31ab-104">Depois de determinar como organizar o filtro por meio de uma estrutura [**CAPTUREFILTER**](capturefilter.md) , você deve alocar e preencher a estrutura, que é passada para o driver de monitor de rede por meio de um blob de configuração.</span><span class="sxs-lookup"><span data-stu-id="c31ab-104">After you determine how to organize your filter through a [**CAPTUREFILTER**](capturefilter.md) structure, you must allocate and fill in the structure, which is then passed to the Network Monitor driver through a configuration BLOB.</span></span>

<span data-ttu-id="c31ab-105">Usuários NPP diretos adicionam o filtro de captura ao BLOB de configuração que é passado para **conectar**, [**Configurar**](configure.md)ou ambos.</span><span class="sxs-lookup"><span data-stu-id="c31ab-105">Direct NPP users add the capture filter to the configuration BLOB that is passed to **Connect**, [**Configure**](configure.md), or both.</span></span> <span data-ttu-id="c31ab-106">Para obter uma lista de interfaces COM que você pode usar para se comunicar com o NPP, consulte [interfaces NPP](npp-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c31ab-106">For a list of COM interfaces that you can use to communicate with the NPP, see [NPP Interfaces](npp-interfaces.md).</span></span>

 

 



