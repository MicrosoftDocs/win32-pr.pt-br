---
title: Propriedades de conexão EAP-TLS
description: Saiba mais sobre as propriedades de conexão EAP-TLS. Veja um exemplo que é uma instância do esquema herdado eaptlsconnectionpropertiesv1.
ms.assetid: 7d8e7771-5263-4187-bb9d-ec0d6c154b17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040c8860c99fa0a144a0903bde281045657425135545491f38958c34b3af05d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785263"
---
# <a name="eap-tls-connection-properties"></a>Propriedades de conexão EAP-TLS

Este exemplo é uma instância do esquema herdado [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) .

``` syntax
  <?xml version="1.0" ?>
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>13</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
      xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>13</baseEap:Type> 
        <eapTls:EapType>
          <eapTls:CredentialsSource>
            <eapTls:CertificateStore />
          </eapTls:CredentialsSource>
          <eapTls:ServerValidation>
            <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation>
            <eapTls:ServerNames /> 
            <eapTls:TrustedRootCA /> 
          </eapTls:ServerValidation>
          <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
        </eapTls:EapType>
      </baseEap:Eap>
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da conexão](connection-profiles.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> </dl>

 

 




