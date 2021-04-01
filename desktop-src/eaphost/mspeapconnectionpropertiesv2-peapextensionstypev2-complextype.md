---
title: Tipo complexo PeapExtensionsTypeV2
description: Saiba mais sobre o tipo complexo PeapExtensionsTypeV2. Esse tipo permite aprimoramentos futuros no esquema.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917691"
---
# <a name="peapextensionstypev2-complex-type"></a><span data-ttu-id="3fcc2-104">Tipo complexo PeapExtensionsTypeV2</span><span class="sxs-lookup"><span data-stu-id="3fcc2-104">PeapExtensionsTypeV2 Complex Type</span></span>

<span data-ttu-id="3fcc2-105">O tipo complexo **PeapExtensionsTypeV2** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-105">The **PeapExtensionsTypeV2** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="3fcc2-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fcc2-106">Remarks</span></span>

<span data-ttu-id="3fcc2-107">O elemento **PeapExtensionsTypeV2** é opcional.</span><span class="sxs-lookup"><span data-stu-id="3fcc2-107">The **PeapExtensionsTypeV2** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fcc2-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fcc2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fcc2-109">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="3fcc2-109">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3fcc2-110">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="3fcc2-110">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3fcc2-111">Tipos complexos mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="3fcc2-111">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3fcc2-112">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="3fcc2-112">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




