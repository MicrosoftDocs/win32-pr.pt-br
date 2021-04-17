---
title: Elemento TrustedRootCA (ServerValidationParameters)-conexão
description: Captura a impressão em miniatura das CAs (autoridades de certificação) raiz confiáveis do cliente. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
keywords:
- Elemento TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105772921"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a><span data-ttu-id="77376-105">Elemento TrustedRootCA (ServerValidationParameters) para propriedades de conexão</span><span class="sxs-lookup"><span data-stu-id="77376-105">TrustedRootCA (ServerValidationParameters) Element for connection properties</span></span>

<span data-ttu-id="77376-106">O elemento **TrustedRootCA (ServerValidationParameters)** captura a impressão digital das CAS (autoridades de certificação) raiz confiáveis do cliente.</span><span class="sxs-lookup"><span data-stu-id="77376-106">The **TrustedRootCA (ServerValidationParameters)** element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="77376-107">O elemento **TrustedRootCA** é definido pelo tipo complexo [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="77376-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="77376-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="77376-108">Remarks</span></span>

<span data-ttu-id="77376-109">O Thumb Print é uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.</span><span class="sxs-lookup"><span data-stu-id="77376-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="77376-110">O elemento **TrustedRootCA** é opcional.</span><span class="sxs-lookup"><span data-stu-id="77376-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="77376-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77376-111">Requirements</span></span>



| <span data-ttu-id="77376-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="77376-112">Requirement</span></span> | <span data-ttu-id="77376-113">Valor</span><span class="sxs-lookup"><span data-stu-id="77376-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77376-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77376-114">Minimum supported client</span></span><br/> | <span data-ttu-id="77376-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77376-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77376-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77376-116">Minimum supported server</span></span><br/> | <span data-ttu-id="77376-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77376-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77376-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="77376-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="77376-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="77376-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="77376-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="77376-120">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="77376-121">**Possíveis elementos pai imediatos na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="77376-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="77376-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="77376-122">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="77376-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="77376-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="77376-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="77376-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="77376-125">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="77376-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="77376-126">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="77376-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





