---
title: Propriedades do usuário do SDK
description: Saiba mais sobre as propriedades do usuário do SDK. Veja um exemplo que é uma instância do esquema nativo do eaphostusercredentials.
ms.assetid: e8a9656d-48e7-4580-a84d-2b829e7a692f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c8dab154e1ef6c736849720856a23fdfe2e7b3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104084967"
---
# <a name="sdk-user-properties"></a><span data-ttu-id="d8be3-104">Propriedades do usuário do SDK</span><span class="sxs-lookup"><span data-stu-id="d8be3-104">SDK User Properties</span></span>

<span data-ttu-id="d8be3-105">Este exemplo é uma instância do esquema nativo do [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="d8be3-105">This sample is an instance of the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) native schema.</span></span>

``` syntax
  <?xml version="1.0" ?>  
  <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod> 
    <Credentials>
      <EapType>40</EapType> 
      <Identity>test</Identity> 
      <Password>test</Password> 
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a><span data-ttu-id="d8be3-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8be3-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8be3-107">Propriedades do Usuário</span><span class="sxs-lookup"><span data-stu-id="d8be3-107">User Properties</span></span>](user-profiles.md)
</dt> <dt>

[<span data-ttu-id="d8be3-108">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="d8be3-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




