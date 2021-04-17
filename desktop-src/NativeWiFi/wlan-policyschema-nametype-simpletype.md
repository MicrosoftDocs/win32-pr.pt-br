---
description: Define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de política de LAN sem fio.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Tipo simples nametype (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759483"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="8f8a3-103">Tipo simples nametype (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="8f8a3-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="8f8a3-104">O tipo simples nametype define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de diretiva de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-104">The nameType simple type defines a string type for either the name or the description of a wireless LAN policy profile.</span></span> <span data-ttu-id="8f8a3-105">Os nomes e as descrições são cadeias de caracteres com pelo menos um caractere e no máximo 255 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="8f8a3-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f8a3-106">Requirements</span></span>



| <span data-ttu-id="8f8a3-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f8a3-107">Requirement</span></span> | <span data-ttu-id="8f8a3-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8f8a3-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f8a3-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f8a3-109">Minimum supported client</span></span><br/> | <span data-ttu-id="8f8a3-110">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f8a3-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f8a3-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f8a3-111">Minimum supported server</span></span><br/> | <span data-ttu-id="8f8a3-112">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8f8a3-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




