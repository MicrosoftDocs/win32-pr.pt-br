---
title: Tipo complexo PeapExtensionsType (Propriedades de conexão)
description: Saiba mais sobre o tipo complexo PeapExtensionsType. Esse tipo permite aprimoramentos futuros no esquema.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- PeapExtensionsType tipo complexo EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294510"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a><span data-ttu-id="771ae-105">Tipo complexo PeapExtensionsType (Propriedades de conexão)</span><span class="sxs-lookup"><span data-stu-id="771ae-105">PeapExtensionsType complex type (connection properties)</span></span>

<span data-ttu-id="771ae-106">O tipo complexo **PeapExtensionsType** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="771ae-106">The **PeapExtensionsType** complex type enables future enhancements to the schema.</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="771ae-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="771ae-107">Remarks</span></span>

<span data-ttu-id="771ae-108">O tipo complexo **PeapExtensionsType** é opcional.</span><span class="sxs-lookup"><span data-stu-id="771ae-108">The **PeapExtensionsType** complex type is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="771ae-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="771ae-109">Requirements</span></span>



| <span data-ttu-id="771ae-110">Função</span><span class="sxs-lookup"><span data-stu-id="771ae-110">Role</span></span> | <span data-ttu-id="771ae-111">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="771ae-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="771ae-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="771ae-112">Client</span></span><br/> | <span data-ttu-id="771ae-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="771ae-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="771ae-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="771ae-114">Server</span></span><br/> | <span data-ttu-id="771ae-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="771ae-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="771ae-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="771ae-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771ae-117">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="771ae-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="771ae-118">Esquema mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="771ae-118">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





