---
description: Define um tipo de cadeia de caracteres para o perfil de banda larga móvel.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: tipo simples nametype (banda larga móvel)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755282"
---
# <a name="nametype-simple-type-mobile-broadband"></a><span data-ttu-id="1020e-103">tipo simples nametype (banda larga móvel)</span><span class="sxs-lookup"><span data-stu-id="1020e-103">nameType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="1020e-104">O tipo simples **nametype** define um tipo de cadeia de caracteres para o perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="1020e-104">The **nameType** simple type defines a string type for the Mobile Broadband profile.</span></span> <span data-ttu-id="1020e-105">Essa cadeia de caracteres tem pelo menos um caractere e, no máximo, 255 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="1020e-105">This string is at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
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

## <a name="requirements"></a><span data-ttu-id="1020e-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1020e-106">Requirements</span></span>



| <span data-ttu-id="1020e-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="1020e-107">Requirement</span></span> | <span data-ttu-id="1020e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1020e-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="1020e-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1020e-109">Minimum supported client</span></span><br/> | <span data-ttu-id="1020e-110">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1020e-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="1020e-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1020e-111">Minimum supported server</span></span><br/> | <span data-ttu-id="1020e-112">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1020e-112">None supported</span></span><br/>                         |



 

 




