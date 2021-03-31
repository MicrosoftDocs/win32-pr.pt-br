---
title: Tipo simples de counttype
description: Define um tipo de contagem que é usado para especificar o número de elementos em uma matriz.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- EventLog de tipo simples de counttype
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645234"
---
# <a name="counttype-simple-type"></a><span data-ttu-id="f1054-104">Tipo simples de counttype</span><span class="sxs-lookup"><span data-stu-id="f1054-104">CountType Simple Type</span></span>

<span data-ttu-id="f1054-105">Define um tipo de contagem que é usado para especificar o número de elementos em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="f1054-105">Defines a count type that is used to specify the number of elements in an array.</span></span> <span data-ttu-id="f1054-106">O valor pode ser especificado como um valor xs: unsignedShort ou como uma cadeia de caracteres que faz referência ao nome do nó de item de dados que contém o valor curto de unsiged.</span><span class="sxs-lookup"><span data-stu-id="f1054-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsiged short value.</span></span>

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="f1054-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1054-107">Requirements</span></span>



| <span data-ttu-id="f1054-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1054-108">Requirement</span></span> | <span data-ttu-id="f1054-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f1054-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1054-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1054-110">Minimum supported client</span></span><br/> | <span data-ttu-id="f1054-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1054-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1054-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1054-112">Minimum supported server</span></span><br/> | <span data-ttu-id="f1054-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1054-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





