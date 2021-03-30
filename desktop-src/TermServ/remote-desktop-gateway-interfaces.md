---
title: Interfaces de gateway Área de Trabalho Remota
description: A API do gateway de Área de Trabalho Remota (Gateway RD) dá suporte às seguintes interfaces. Você pode usar essas interfaces para implementar plug-ins que fornecem autenticação e autorização personalizadas.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916001"
---
# <a name="remote-desktop-gateway-interfaces"></a>Interfaces de gateway Área de Trabalho Remota

A API do gateway de Área de Trabalho Remota (Gateway RD) dá suporte às seguintes interfaces. Você pode usar essas interfaces para implementar plug-ins que fornecem autenticação e autorização personalizadas. Não há nenhuma dependência entre o plug-in de autenticação e o plug-in de autorização, e você pode implementar apenas um único plug-in, se escolher.

Os plug-ins de autenticação são [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) e [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).

Os plug-ins de autorização são [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)e [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

Expõe métodos que fornecem informações sobre a criação ou o fechamento de sessões para uma conexão.

</dd> <dt>

[**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

Expõe métodos que notificam o Gateway RD sobre eventos de autenticação.

</dd> <dt>

[**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

Expõe métodos que autenticam usuários para o gateway de área de trabalho remota.

</dd> <dt>

[**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

Expõe métodos que notificam o Gateway RD sobre o resultado de uma tentativa de autorizar uma conexão.

</dd> <dt>

[**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

Expõe métodos que notificam o Gateway RD sobre o resultado de uma tentativa de autorizar um recurso.

</dd> <dt>

[**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

Expõe métodos que autorizam conexões e recursos.

</dd> </dl>

 

 




