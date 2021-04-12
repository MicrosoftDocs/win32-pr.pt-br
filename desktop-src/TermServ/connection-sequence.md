---
title: Sequência de conexão
description: Uma ilustração que mostra as chamadas de método feitas entre o serviço de Serviços de Área de Trabalho Remota e o protocolo durante a sequência de conexão do cliente.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364347"
---
# <a name="connection-sequence"></a><span data-ttu-id="73e8a-103">Sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="73e8a-103">Connection Sequence</span></span>

<span data-ttu-id="73e8a-104">A ilustração a seguir mostra as chamadas de método feitas entre o serviço de Serviços de Área de Trabalho Remota e o protocolo durante a sequência de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="73e8a-104">The following illustration shows the method calls made between the Remote Desktop Services service and your protocol during the client connection sequence.</span></span> <span data-ttu-id="73e8a-105">As ações mostradas aqui seguem a [sequência de início](start-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="73e8a-105">The actions shown here follow the [Start Sequence](start-sequence.md).</span></span> <span data-ttu-id="73e8a-106">A interação entre o serviço e o objeto [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) representa o handshake de licenciamento para o cliente.</span><span class="sxs-lookup"><span data-stu-id="73e8a-106">The interaction between the service and the [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) object represents the licensing handshake for the client.</span></span>

![sequência de conexão do cliente](images/protocol-connectionsequence.png)

## <a name="related-topics"></a><span data-ttu-id="73e8a-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73e8a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73e8a-109">Sequência de chamada de método</span><span class="sxs-lookup"><span data-stu-id="73e8a-109">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="73e8a-110">Reconectar sequência</span><span class="sxs-lookup"><span data-stu-id="73e8a-110">Reconnect Sequence</span></span>](reconnect-sequence.md)
</dt> <dt>

[<span data-ttu-id="73e8a-111">Iniciar sequência</span><span class="sxs-lookup"><span data-stu-id="73e8a-111">Start Sequence</span></span>](start-sequence.md)
</dt> </dl>

 

 




