---
description: Define um tipo de cadeia de caracteres para o elemento ICONFilePath no perfil de banda larga móvel.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Tipo simples de iconFileType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090303"
---
# <a name="iconfiletype-simple-type"></a><span data-ttu-id="64222-103">Tipo simples de iconFileType</span><span class="sxs-lookup"><span data-stu-id="64222-103">iconFileType Simple Type</span></span>

<span data-ttu-id="64222-104">O tipo simples **iconFileType** define um tipo de cadeia de caracteres para o elemento [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) no perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="64222-104">The **iconFileType** simple type defines a string type for the [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="64222-105">Essa cadeia de caracteres tem pelo menos um caractere e, no máximo, 1024 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="64222-105">This string is at least one character long and at most 1024 characters long.</span></span>

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="64222-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64222-106">Requirements</span></span>



| <span data-ttu-id="64222-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="64222-107">Requirement</span></span> | <span data-ttu-id="64222-108">Valor</span><span class="sxs-lookup"><span data-stu-id="64222-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="64222-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64222-109">Minimum supported client</span></span><br/> | <span data-ttu-id="64222-110">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="64222-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="64222-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64222-111">Minimum supported server</span></span><br/> | <span data-ttu-id="64222-112">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="64222-112">None supported</span></span><br/>                         |



 

 




