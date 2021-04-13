---
description: Define um tipo de cadeia de caracteres para o elemento ProviderName no perfil de banda larga móvel.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Tipo simples de providerNametype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501645"
---
# <a name="providernametype-simple-type"></a><span data-ttu-id="47d6e-103">Tipo simples de providerNametype</span><span class="sxs-lookup"><span data-stu-id="47d6e-103">providerNameType Simple Type</span></span>

<span data-ttu-id="47d6e-104">O tipo simples **providernametype** define um tipo de cadeia de caracteres para o elemento [**ProviderName**](schema-providername-providertype-element.md) no perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="47d6e-104">The **providerNameType** simple type defines a string type for the [**ProviderName**](schema-providername-providertype-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="47d6e-105">Essa cadeia de caracteres tem pelo menos um caractere de comprimento e no máximo 20 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47d6e-105">This string is at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="47d6e-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47d6e-106">Requirements</span></span>



| <span data-ttu-id="47d6e-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d6e-107">Requirement</span></span> | <span data-ttu-id="47d6e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="47d6e-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="47d6e-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47d6e-109">Minimum supported client</span></span><br/> | <span data-ttu-id="47d6e-110">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="47d6e-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="47d6e-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47d6e-111">Minimum supported server</span></span><br/> | <span data-ttu-id="47d6e-112">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="47d6e-112">None supported</span></span><br/>                         |



 

 




