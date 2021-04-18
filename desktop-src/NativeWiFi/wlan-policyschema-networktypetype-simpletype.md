---
description: Define os tipos de rede sem fio.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Tipo simples de networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760232"
---
# <a name="networktypetype-simple-type"></a><span data-ttu-id="f5588-103">Tipo simples de networkTypeType</span><span class="sxs-lookup"><span data-stu-id="f5588-103">networkTypeType Simple Type</span></span>

<span data-ttu-id="f5588-104">O tipo simples networkTypeType define os tipos de rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="f5588-104">The networkTypeType simple type defines the wireless network types.</span></span> <span data-ttu-id="f5588-105">Há dois tipos de redes: redes de infraestrutura (ESS) e redes ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="f5588-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="f5588-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="f5588-106">Enumeration values</span></span>

<span data-ttu-id="f5588-107">O tipo simples **networkTypeType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5588-107">The **networkTypeType** simple type defines the following values.</span></span>



| <span data-ttu-id="f5588-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f5588-108">Value</span></span> | <span data-ttu-id="f5588-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5588-109">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f5588-110">IBSS</span><span class="sxs-lookup"><span data-stu-id="f5588-110">IBSS</span></span>  |             |
| <span data-ttu-id="f5588-111">ESS</span><span class="sxs-lookup"><span data-stu-id="f5588-111">ESS</span></span>   |             |



## <a name="requirements"></a><span data-ttu-id="f5588-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5588-112">Requirements</span></span>



| <span data-ttu-id="f5588-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5588-113">Requirement</span></span> | <span data-ttu-id="f5588-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f5588-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5588-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5588-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f5588-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5588-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5588-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5588-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f5588-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5588-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




