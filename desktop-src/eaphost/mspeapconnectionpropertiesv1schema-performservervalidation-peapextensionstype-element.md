---
title: Elemento PerformServerValidation (PeapExtensionsType) (esquema v1)
description: Saiba mais sobre o elemento PerformServerValidation (PeapExtensionsType). Esse elemento indica se a validação do servidor é executada. | Elemento PerformServerValidation (PeapExtensionsType) (esquema v1)
ms.assetid: b0483ed0-a02f-4f60-b1ae-7c5e6be8e196
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256d942d68c30788180f2d8080f963c1d79b401a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105790376"
---
# <a name="performservervalidation-peapextensionstype-element-v1-schema"></a><span data-ttu-id="8b0f0-106">Elemento PerformServerValidation (PeapExtensionsType) (esquema v1)</span><span class="sxs-lookup"><span data-stu-id="8b0f0-106">PerformServerValidation (PeapExtensionsType) element (v1 schema)</span></span>

<span data-ttu-id="8b0f0-107">O elemento **PerformServerValidation (PeapExtensionsType)** indica se a validação do servidor é executada.</span><span class="sxs-lookup"><span data-stu-id="8b0f0-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:PerformServerValidation"
 />
```

<span data-ttu-id="8b0f0-108">O elemento é definido pelo elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8b0f0-108">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b0f0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b0f0-109">Remarks</span></span>

<span data-ttu-id="8b0f0-110">O elemento **PerformServerValidation** é opcional.</span><span class="sxs-lookup"><span data-stu-id="8b0f0-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b0f0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b0f0-111">Requirements</span></span>



| <span data-ttu-id="8b0f0-112">Função</span><span class="sxs-lookup"><span data-stu-id="8b0f0-112">Role</span></span> | <span data-ttu-id="8b0f0-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="8b0f0-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="8b0f0-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="8b0f0-114">Client</span></span><br/> | <span data-ttu-id="8b0f0-115">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8b0f0-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8b0f0-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="8b0f0-116">Server</span></span><br/> | <span data-ttu-id="8b0f0-117">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8b0f0-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b0f0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b0f0-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b0f0-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="8b0f0-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8b0f0-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="8b0f0-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="8b0f0-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="8b0f0-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8b0f0-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="8b0f0-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="8b0f0-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8b0f0-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="8b0f0-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="8b0f0-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8b0f0-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="8b0f0-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="8b0f0-126">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="8b0f0-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8b0f0-127">**PerformServerValidation(PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="8b0f0-127">**PerformServerValidation(PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





