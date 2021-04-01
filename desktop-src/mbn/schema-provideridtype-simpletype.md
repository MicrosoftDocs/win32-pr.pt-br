---
description: Define um tipo para o elemento ProviderID do perfil de banda larga móvel.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Tipo simples de providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090300"
---
# <a name="provideridtype-simple-type"></a><span data-ttu-id="fbbf0-103">Tipo simples de providerIdType</span><span class="sxs-lookup"><span data-stu-id="fbbf0-103">providerIdType Simple Type</span></span>

<span data-ttu-id="fbbf0-104">O tipo simples **providerIdType** define um tipo para o elemento [**ProviderID**](schema-providerid-providertype-element.md) do perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="fbbf0-104">The **providerIdType** simple type defines a type for the [**ProviderID**](schema-providerid-providertype-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="fbbf0-105">Esse tipo é uma coleção de dígitos com pelo menos um dígito e, no máximo, seis dígitos.</span><span class="sxs-lookup"><span data-stu-id="fbbf0-105">This type is a collection of digits at least one digit long and at most 6 digits long.</span></span>

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="fbbf0-106">Padrões</span><span class="sxs-lookup"><span data-stu-id="fbbf0-106">Patterns</span></span>

<span data-ttu-id="fbbf0-107">O tipo simples **providerIdType** é um token que é restrito pelo seguinte padrão:</span><span class="sxs-lookup"><span data-stu-id="fbbf0-107">The **providerIdType** simple type is a token that is restricted by the following pattern:</span></span>

-   `\d{1,6}`

## <a name="requirements"></a><span data-ttu-id="fbbf0-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbbf0-108">Requirements</span></span>



| <span data-ttu-id="fbbf0-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbbf0-109">Requirement</span></span> | <span data-ttu-id="fbbf0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="fbbf0-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="fbbf0-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbbf0-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbf0-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fbbf0-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="fbbf0-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbbf0-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbf0-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fbbf0-114">None supported</span></span><br/>                         |



 

 




