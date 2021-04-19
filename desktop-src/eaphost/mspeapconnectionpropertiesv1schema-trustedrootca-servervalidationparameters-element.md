---
title: Elemento TrustedRootCA (ServerValidationParameters) (v1)
description: Captura a impressão em miniatura das CAs (autoridades de certificação) raiz confiáveis do cliente. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
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
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389076"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="2a496-105">Elemento TrustedRootCA (ServerValidationParameters)</span><span class="sxs-lookup"><span data-stu-id="2a496-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="2a496-106">O elemento de elemento **TrustedRootCA (ServerValidationParameters)** captura a impressão digital das CAS (autoridades de certificação) raiz confiáveis do cliente.</span><span class="sxs-lookup"><span data-stu-id="2a496-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="2a496-107">O elemento **TrustedRootCA** é definido pelo tipo complexo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2a496-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a496-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a496-108">Remarks</span></span>

<span data-ttu-id="2a496-109">O Thumb Print é uma cadeia de caracteres hexadecimal que contém o hash SHA-1 do certificado.</span><span class="sxs-lookup"><span data-stu-id="2a496-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="2a496-110">O elemento **TrustedRootCA** é opcional.</span><span class="sxs-lookup"><span data-stu-id="2a496-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a496-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a496-111">Requirements</span></span>



| <span data-ttu-id="2a496-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a496-112">Requirement</span></span> | <span data-ttu-id="2a496-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2a496-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a496-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a496-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2a496-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a496-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2a496-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a496-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2a496-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a496-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a496-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a496-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a496-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="2a496-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2a496-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="2a496-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="2a496-121">**Possíveis elementos pai imediatos na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="2a496-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2a496-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="2a496-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="2a496-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2a496-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="2a496-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="2a496-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2a496-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2a496-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2a496-126">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2a496-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





