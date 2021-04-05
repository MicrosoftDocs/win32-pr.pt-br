---
description: Define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de diretiva de LAN com fio.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: tipo simples nametype (LAN_policy)
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
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922126"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="fbfc8-103">tipo simples nametype (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="fbfc8-103">nameType simple type (LAN_policy)</span></span>

<span data-ttu-id="fbfc8-104">O tipo simples nametype define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de diretiva de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="fbfc8-104">The nameType simple type defines a string type for either the name or the description of a wired LAN policy profile.</span></span> <span data-ttu-id="fbfc8-105">Os nomes e as descrições são cadeias de caracteres com pelo menos um caractere e no máximo 255 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="fbfc8-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="fbfc8-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbfc8-106">Requirements</span></span>



| <span data-ttu-id="fbfc8-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbfc8-107">Requirement</span></span> | <span data-ttu-id="fbfc8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="fbfc8-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbfc8-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbfc8-109">Minimum supported client</span></span><br/> | <span data-ttu-id="fbfc8-110">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbfc8-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbfc8-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbfc8-111">Minimum supported server</span></span><br/> | <span data-ttu-id="fbfc8-112">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbfc8-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




