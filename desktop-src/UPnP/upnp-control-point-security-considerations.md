---
title: Considerações de segurança do ponto de controle
description: Ao criar um ponto de controle, você precisa levar em consideração os seguintes problemas de segurança.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916486"
---
# <a name="control-point-security-considerations"></a><span data-ttu-id="39035-103">Considerações de segurança do ponto de controle</span><span class="sxs-lookup"><span data-stu-id="39035-103">Control Point Security Considerations</span></span>

<span data-ttu-id="39035-104">Ao criar um ponto de controle, você precisa levar em consideração os seguintes problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="39035-104">When you are creating a control point, you need to take into consideration the following security issues.</span></span>

-   <span data-ttu-id="39035-105">Todas as pesquisas de ponto de controle são enviadas por padrão com um TTL igual a 1.</span><span class="sxs-lookup"><span data-stu-id="39035-105">All control point searches are by default sent with a TTL of 1.</span></span> <span data-ttu-id="39035-106">Isso significa que somente os dispositivos na mesma sub-rede são descobertos.</span><span class="sxs-lookup"><span data-stu-id="39035-106">This means that only devices within the same subnet are discovered.</span></span> <span data-ttu-id="39035-107">Você pode configurar uma TTL mais alta no registro.</span><span class="sxs-lookup"><span data-stu-id="39035-107">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="39035-108">A descrição do dispositivo e do serviço de um dispositivo será baixada somente se estiver presente no mesmo dispositivo que enviou o comunicado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39035-108">A device's device and service description is only downloaded if it is present on the same device which sent the device announcement.</span></span>
-   <span data-ttu-id="39035-109">Um dispositivo só receberá solicitações de controle e assinatura se suas URLs de controle e assinatura estiverem no mesmo dispositivo que enviou os anúncios do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39035-109">A device is only sent control and subscription requests if its control and subscription URLs are on the same device that sent the device announcements.</span></span>

 

 




