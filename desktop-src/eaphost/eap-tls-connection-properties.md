---
title: Propriedades de conexão EAP-TLS
description: Saiba mais sobre as propriedades de conexão EAP-TLS. Veja um exemplo que é uma instância do esquema herdado eaptlsconnectionpropertiesv1.
ms.assetid: 7d8e7771-5263-4187-bb9d-ec0d6c154b17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbda4f345c0feedf6571f9f1c58f0193a876d2d1
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642930"
---
# <a name="eap-tls-connection-properties"></a><span data-ttu-id="09de5-104">Propriedades de conexão EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="09de5-104">EAP-TLS Connection Properties</span></span>

<span data-ttu-id="09de5-105">Este exemplo é uma instância do esquema herdado [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="09de5-105">This sample is an instance of the [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) legacy schema.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="09de5-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09de5-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09de5-107">Propriedades da conexão</span><span class="sxs-lookup"><span data-stu-id="09de5-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="09de5-108">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="09de5-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




