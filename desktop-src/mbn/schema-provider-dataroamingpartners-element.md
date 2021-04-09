---
description: Identifica o nome e a ID do provedor para uma rede de celular.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Elemento Provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090301"
---
# <a name="provider-dataroamingpartners-element"></a><span data-ttu-id="ed85a-103">Elemento Provider (DataRoamingPartners)</span><span class="sxs-lookup"><span data-stu-id="ed85a-103">Provider (DataRoamingPartners) Element</span></span>

<span data-ttu-id="ed85a-104">O elemento **Provider (DataRoamingPartners)** identifica o nome e a ID do provedor para uma rede de celular.</span><span class="sxs-lookup"><span data-stu-id="ed85a-104">The **Provider (DataRoamingPartners)** element identifies the name and provider ID for a cellular network.</span></span>

<span data-ttu-id="ed85a-105">Este elemento tem os seguintes elementos filho.</span><span class="sxs-lookup"><span data-stu-id="ed85a-105">This element has the following child elements.</span></span>

-   [<span data-ttu-id="ed85a-106">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="ed85a-106">**ProviderID**</span></span>](schema-providerid-providertype-element.md)
-   [<span data-ttu-id="ed85a-107">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="ed85a-107">**ProviderName**</span></span>](schema-providername-providertype-element.md)

<span data-ttu-id="ed85a-108">Esse elemento pode ser definido várias vezes dentro do elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ed85a-108">This element can be defined multiple times within the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span> <span data-ttu-id="ed85a-109">Ele deve ser definido pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="ed85a-109">It must be defined at least once.</span></span>

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

<span data-ttu-id="ed85a-110">O elemento **Provider** é definido pelo elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ed85a-110">The **Provider** element is defined by the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed85a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed85a-111">Requirements</span></span>



| <span data-ttu-id="ed85a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed85a-112">Requirement</span></span> | <span data-ttu-id="ed85a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ed85a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ed85a-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed85a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ed85a-115">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ed85a-115">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ed85a-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed85a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ed85a-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ed85a-117">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ed85a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed85a-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed85a-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="ed85a-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ed85a-120">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="ed85a-120">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="ed85a-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="ed85a-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ed85a-122">**DataRoamingPartners (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="ed85a-122">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




