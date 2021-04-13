---
title: Propriedades de conexão do EAP MS-CHAPv2
description: Saiba mais sobre as propriedades de conexão do EAP MS-CHAPv2. Veja um exemplo que é uma instância do esquema herdado mschapv2connectionpropertiesv1.
ms.assetid: d6a057e0-56f6-4a31-9391-fde631ac2898
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e353c4685e131c2e7301db35de26d927b5882c06
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366850"
---
# <a name="eap-ms-chapv2-connection-properties"></a><span data-ttu-id="bd763-104">Propriedades de conexão do EAP MS-CHAPv2</span><span class="sxs-lookup"><span data-stu-id="bd763-104">EAP MS-CHAPv2 Connection Properties</span></span>

<span data-ttu-id="bd763-105">Este exemplo é uma instância do esquema herdado [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) ..</span><span class="sxs-lookup"><span data-stu-id="bd763-105">This sample is an instance of the [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) legacy schema..</span></span>

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>26</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
      xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>26</baseEap:Type> 
        <msChapV2:EapType>
        <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
        </msChapV2:EapType>
      </baseEap:Eap>
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a><span data-ttu-id="bd763-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd763-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd763-107">Propriedades da conexão</span><span class="sxs-lookup"><span data-stu-id="bd763-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="bd763-108">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="bd763-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




