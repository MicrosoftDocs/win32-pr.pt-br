---
title: Propriedades do usuário PEAP-TLS
description: Saiba mais sobre as propriedades do usuário PEAP-TLS. Veja um exemplo que é uma instância do esquema herdado eaptlsuserpropertiesv1.
ms.assetid: f0fb00fa-4cf8-4490-ac59-a8252ddcb5ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32437c54d707c3d278e4494c2b5b4f56ed83c9d4
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105760929"
---
# <a name="peap-tls-user-properties"></a><span data-ttu-id="6a6d0-104">Propriedades do usuário PEAP-TLS</span><span class="sxs-lookup"><span data-stu-id="6a6d0-104">PEAP-TLS User Properties</span></span>

<span data-ttu-id="6a6d0-105">Este exemplo é uma instância do esquema herdado [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="6a6d0-105">This sample is an instance of the [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md) legacy schema.</span></span>

``` syntax
  <?xml version="1.0" ?> 
  <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials"
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon"
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
    <EapMethod>
      <eapCommon:Type>25</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1"
      xmlns:MsPeap="https://www.microsoft.com/provisioning/MsPeapUserPropertiesV1"
      xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsUserPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <MsPeap:EapType>
          <MsPeap:RoutingIdentity>test</MsPeap:RoutingIdentity> 
          <baseEap:Eap>
            <baseEap:Type>13</baseEap:Type> 
            <eapTls:EapType>
              <eapTls:Username>ias-domain\test</eapTls:Username> 
              <eapTls:UserCert /> 
            </eapTls:EapType>
          </baseEap:Eap>
        </MsPeap:EapType>
      </baseEap:Eap>
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a><span data-ttu-id="6a6d0-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a6d0-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a6d0-107">Propriedades do Usuário</span><span class="sxs-lookup"><span data-stu-id="6a6d0-107">User Properties</span></span>](user-profiles.md)
</dt> <dt>

[<span data-ttu-id="6a6d0-108">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="6a6d0-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




