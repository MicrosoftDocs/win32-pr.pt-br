---
description: Especifica a lista de provedores de rede preferenciais no momento do roaming.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Elemento DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811240"
---
# <a name="dataroamingpartners-mbnprofile-element"></a><span data-ttu-id="35138-103">Elemento DataRoamingPartners (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="35138-103">DataRoamingPartners (MBNProfile) Element</span></span>

<span data-ttu-id="35138-104">O elemento **DataRoamingPartners (MBNProfile)** especifica a lista de provedores de rede preferenciais no momento do roaming.</span><span class="sxs-lookup"><span data-stu-id="35138-104">The **DataRoamingPartners (MBNProfile)** element specifies the list of preferred network providers at the time of roaming.</span></span>

<span data-ttu-id="35138-105">O serviço de banda larga móvel usa esse elemento para selecionar a rede preferencial fornecida durante o roaming.</span><span class="sxs-lookup"><span data-stu-id="35138-105">The Mobile Broadband service uses this element to select the preferred network provide while roaming.</span></span>

<span data-ttu-id="35138-106">O elemento tem o seguinte elemento filho que deve ser definido pelo menos uma vez, mas pode ser definido várias vezes.</span><span class="sxs-lookup"><span data-stu-id="35138-106">The element has the following child element which must be defined at least once but can be defined multiple times.</span></span>

-   [<span data-ttu-id="35138-107">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="35138-107">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md)

<span data-ttu-id="35138-108">Esse elemento pode ter um máximo de uma ocorrência.</span><span class="sxs-lookup"><span data-stu-id="35138-108">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="35138-109">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="35138-109">This element is optional.</span></span>

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="35138-110">O elemento **DataRoamingPartners** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="35138-110">The **DataRoamingPartners** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="35138-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="35138-111">Child elements</span></span>



| <span data-ttu-id="35138-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="35138-112">Element</span></span>                                                         | <span data-ttu-id="35138-113">Type</span><span class="sxs-lookup"><span data-stu-id="35138-113">Type</span></span>                                                    | <span data-ttu-id="35138-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="35138-114">Description</span></span>                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="35138-115">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="35138-115">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md) | [<span data-ttu-id="35138-116">**providerType**</span><span class="sxs-lookup"><span data-stu-id="35138-116">**providerType**</span></span>](schema-providertype-complextype.md) | <span data-ttu-id="35138-117">Nome e ID de provedor de uma rede de celular.</span><span class="sxs-lookup"><span data-stu-id="35138-117">Name and provider ID of a cellular network.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="35138-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35138-118">Requirements</span></span>



| <span data-ttu-id="35138-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="35138-119">Requirement</span></span> | <span data-ttu-id="35138-120">Valor</span><span class="sxs-lookup"><span data-stu-id="35138-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="35138-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35138-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35138-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="35138-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="35138-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35138-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35138-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="35138-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="35138-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="35138-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="35138-126">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="35138-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="35138-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="35138-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="35138-128">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="35138-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="35138-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="35138-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




