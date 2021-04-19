---
description: Define o tipo que é usado para especificar valores válidos para a cor de determinados elementos em um arquivo XML de diário.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Tipo simples de ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763013"
---
# <a name="colortype-simple-type"></a><span data-ttu-id="f3583-103">Tipo simples de ColorType</span><span class="sxs-lookup"><span data-stu-id="f3583-103">ColorType Simple Type</span></span>

<span data-ttu-id="f3583-104">Define o tipo que é usado para especificar valores válidos para a cor de determinados elementos em um arquivo XML de diário.</span><span class="sxs-lookup"><span data-stu-id="f3583-104">Defines the type that is used to specify valid values for the color of certain elements in a Journal XML file.</span></span>

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="f3583-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3583-105">Remarks</span></span>

<span data-ttu-id="f3583-106">Uma cor pode ser um valor RGB hexadecimal no formato \# RRGGBB.</span><span class="sxs-lookup"><span data-stu-id="f3583-106">A color can be a hexadecimal RGB value in the format \#RRGGBB.</span></span> <span data-ttu-id="f3583-107">Ele deve corresponder à seguinte expressão regular: \# \[ 0-9A-Fa-F \] {6} .</span><span class="sxs-lookup"><span data-stu-id="f3583-107">It must match the following regular expression: \#\[0-9a-fA-F\]{6}.</span></span> <span data-ttu-id="f3583-108">Por exemplo: " \# 4a79B5".</span><span class="sxs-lookup"><span data-stu-id="f3583-108">For example: "\#4a79B5".</span></span>

## <a name="requirements"></a><span data-ttu-id="f3583-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3583-109">Requirements</span></span>



| <span data-ttu-id="f3583-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3583-110">Requirement</span></span> | <span data-ttu-id="f3583-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f3583-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f3583-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3583-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f3583-113">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f3583-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f3583-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3583-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f3583-115">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f3583-115">None supported</span></span><br/>                                     |



 

 




