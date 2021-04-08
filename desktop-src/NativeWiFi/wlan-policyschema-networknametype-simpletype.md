---
description: Define um tipo de cadeia de caracteres para SSIDs (identificadores de conjunto de serviços).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Tipo simples de networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922537"
---
# <a name="networknametype-simple-type"></a><span data-ttu-id="7f416-103">Tipo simples de networkNameType</span><span class="sxs-lookup"><span data-stu-id="7f416-103">networkNameType Simple Type</span></span>

<span data-ttu-id="7f416-104">O tipo simples networkNameType define um tipo de cadeia de caracteres para SSIDs (identificadores de conjunto de serviços).</span><span class="sxs-lookup"><span data-stu-id="7f416-104">The networkNameType simple type defines a string type for service set identifiers (SSIDs).</span></span> <span data-ttu-id="7f416-105">Um SSID é uma cadeia de caracteres que tem pelo menos um caractere e, no máximo, 32 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="7f416-105">A SSID is a string that is at least one character long and at most 32 characters long.</span></span>

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="7f416-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f416-106">Requirements</span></span>



| <span data-ttu-id="7f416-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f416-107">Requirement</span></span> | <span data-ttu-id="7f416-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7f416-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f416-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f416-109">Minimum supported client</span></span><br/> | <span data-ttu-id="7f416-110">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f416-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f416-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f416-111">Minimum supported server</span></span><br/> | <span data-ttu-id="7f416-112">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f416-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




