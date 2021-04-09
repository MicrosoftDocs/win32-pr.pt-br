---
description: Define um tipo para o elemento subscriberid do perfil de banda larga móvel.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Tipo simples de subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010467"
---
# <a name="subscriberidtype-simple-type"></a><span data-ttu-id="66d03-103">Tipo simples de subscriberIdType</span><span class="sxs-lookup"><span data-stu-id="66d03-103">subscriberIdType Simple Type</span></span>

<span data-ttu-id="66d03-104">O tipo simples **subscriberIdType** define um tipo para o elemento [**subscriberid**](schema-subscriberid-mbnprofile-element.md) do perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="66d03-104">The **subscriberIdType** simple type defines a type for the [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="66d03-105">Esse tipo é uma coleção de um ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="66d03-105">This type is a collection of one or more characters.</span></span>

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="66d03-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d03-106">Requirements</span></span>



| <span data-ttu-id="66d03-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d03-107">Requirement</span></span> | <span data-ttu-id="66d03-108">Valor</span><span class="sxs-lookup"><span data-stu-id="66d03-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="66d03-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66d03-109">Minimum supported client</span></span><br/> | <span data-ttu-id="66d03-110">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="66d03-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="66d03-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66d03-111">Minimum supported server</span></span><br/> | <span data-ttu-id="66d03-112">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="66d03-112">None supported</span></span><br/>                         |



 

 




