---
description: Especifica a ID do provedor da rede de celular.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: Elemento ProviderId (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164574"
---
# <a name="providerid-providertype-element"></a><span data-ttu-id="ae2be-103">Elemento ProviderId (providerType)</span><span class="sxs-lookup"><span data-stu-id="ae2be-103">ProviderID (providerType) Element</span></span>

<span data-ttu-id="ae2be-104">O elemento **ProviderId (ProviderType)** especifica a ID do provedor da rede de celular.</span><span class="sxs-lookup"><span data-stu-id="ae2be-104">The **ProviderID (providerType)** element specifies the provider ID of the cellular network.</span></span>

<span data-ttu-id="ae2be-105">O elemento é uma sequência de dígitos com um máximo de 6 dígitos.</span><span class="sxs-lookup"><span data-stu-id="ae2be-105">The element is a sequence of digits with a maximum of 6 digits.</span></span>

<span data-ttu-id="ae2be-106">Esse elemento é necessário dentro do elemento [**Provider**](schema-provider-dataroamingpartners-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2be-106">This element is required within the [**Provider**](schema-provider-dataroamingpartners-element.md) element.</span></span>

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

<span data-ttu-id="ae2be-107">O elemento **ProviderID** é definido pelo tipo complexo [**ProviderType**](schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2be-107">The **ProviderID** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2be-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae2be-108">Requirements</span></span>



| <span data-ttu-id="ae2be-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae2be-109">Requirement</span></span> | <span data-ttu-id="ae2be-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ae2be-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ae2be-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae2be-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2be-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ae2be-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ae2be-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae2be-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2be-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ae2be-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ae2be-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae2be-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae2be-116">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="ae2be-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ae2be-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="ae2be-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="ae2be-118">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="ae2be-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ae2be-119">**Provedor (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="ae2be-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




