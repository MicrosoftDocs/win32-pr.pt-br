---
description: Define um tipo para o elemento SimIccID do perfil de banda larga móvel.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo simples de simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750721"
---
# <a name="simiccidtype-simple-type"></a><span data-ttu-id="f5dec-103">Tipo simples de simIccIDType</span><span class="sxs-lookup"><span data-stu-id="f5dec-103">simIccIDType Simple Type</span></span>

<span data-ttu-id="f5dec-104">O tipo simples **simIccIDType** define um tipo para o elemento [**SimIccID**](schema-simiccid-mbnprofile-element.md) do perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="f5dec-104">The **simIccIDType** simple type defines a type for the [**SimIccID**](schema-simiccid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="f5dec-105">Esse tipo é uma coleção de dígitos e/ou letras maiúsculas e minúsculas, pelo menos um caractere de comprimento e no máximo 20 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5dec-105">This type is a collection of digits and/or upper- and lower-case letters, at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="f5dec-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="f5dec-106">Patterns</span></span>

<span data-ttu-id="f5dec-107">O tipo simples **simIccIDType** é um token que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="f5dec-107">The **simIccIDType** simple type is a token that is restricted by the following pattern:</span></span>

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a><span data-ttu-id="f5dec-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5dec-108">Requirements</span></span>



| <span data-ttu-id="f5dec-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5dec-109">Requirement</span></span> | <span data-ttu-id="f5dec-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f5dec-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f5dec-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5dec-111">Minimum supported client</span></span><br/> | <span data-ttu-id="f5dec-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f5dec-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f5dec-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5dec-113">Minimum supported server</span></span><br/> | <span data-ttu-id="f5dec-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5dec-114">None supported</span></span><br/>                         |



 

 




