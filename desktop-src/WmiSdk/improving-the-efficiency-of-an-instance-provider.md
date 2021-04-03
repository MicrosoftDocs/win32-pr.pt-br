---
description: Um provedor de alto desempenho do WMI aumenta muito a velocidade em que um cliente WMI pode obter informações de um provedor de instância do WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Melhorando a eficiência de um provedor de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829272"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a><span data-ttu-id="17ed4-103">Melhorando a eficiência de um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="17ed4-103">Improving the Efficiency of an Instance Provider</span></span>

<span data-ttu-id="17ed4-104">Um provedor de alto desempenho do WMI aumenta muito a velocidade em que um cliente WMI pode obter informações de um provedor de instância do WMI.</span><span class="sxs-lookup"><span data-stu-id="17ed4-104">A WMI high-performance provider greatly increases the speed at which a WMI client can obtain information from a WMI instance provider.</span></span> <span data-ttu-id="17ed4-105">A principal alteração é que um provedor de alto desempenho é executado como um servidor em processo para o aplicativo cliente ou para o WMI.</span><span class="sxs-lookup"><span data-stu-id="17ed4-105">The main change is that a high-performance provider runs as an in-process server to either the client application or to WMI.</span></span> <span data-ttu-id="17ed4-106">Ao colocar o provedor dentro do processo do cliente, você pode acelerar a interação entre os dois.</span><span class="sxs-lookup"><span data-stu-id="17ed4-106">By placing the provider inside the client process, you can speed up the interaction between the two.</span></span>

<span data-ttu-id="17ed4-107">Para obter mais informações sobre como tornar seu provedor de instância um provedor de alto desempenho, consulte [criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="17ed4-107">For more information about how to make your instance provider a high-performance provider, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

 

 



