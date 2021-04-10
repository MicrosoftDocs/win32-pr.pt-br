---
title: associação de canal
description: Associações especificam o protocolo de conexão e o comportamento local para um canal.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Associação de serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723a729b87dc26849dbd1f84038805c5e47a0ea4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292313"
---
# <a name="channel-binding"></a><span data-ttu-id="c673f-106">associação de canal</span><span class="sxs-lookup"><span data-stu-id="c673f-106">Channel Binding</span></span>

<span data-ttu-id="c673f-107">Associações especificam o protocolo de conexão e o comportamento local para um canal.</span><span class="sxs-lookup"><span data-stu-id="c673f-107">Bindings specify the wire protocol and local behavior for a channel.</span></span> <span data-ttu-id="c673f-108">As associações são feitas dos seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="c673f-108">Bindings are made up of the following components:</span></span>

-   <span data-ttu-id="c673f-109">Uma [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica o protocolo de transferência a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c673f-109">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use.</span></span>
-   <span data-ttu-id="c673f-110">Uma [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica como proteger o canal.</span><span class="sxs-lookup"><span data-stu-id="c673f-110">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="c673f-111">Um conjunto [**de \_ \_ Propriedades s do WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), que especificam configurações opcionais adicionais (consulte também [**ID de Propriedade do WS \_ Channel \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span><span class="sxs-lookup"><span data-stu-id="c673f-111">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings (see also [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span></span>

 

 




