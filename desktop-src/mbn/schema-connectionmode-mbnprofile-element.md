---
description: Especifica a configuração de conexão automática a ser usada para um dispositivo de banda larga móvel.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Elemento ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920890"
---
# <a name="connectionmode-mbnprofile-element"></a><span data-ttu-id="cea33-103">Elemento ConnectionMode (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="cea33-103">ConnectionMode (MBNProfile) Element</span></span>

<span data-ttu-id="cea33-104">O elemento **ConnectionMode (MBNProfile)** especifica a configuração de conexão automática a ser usada para um dispositivo de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="cea33-104">The **ConnectionMode (MBNProfile)** element specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="cea33-105">Esse elemento pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cea33-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="cea33-106">Valor</span><span class="sxs-lookup"><span data-stu-id="cea33-106">Value</span></span>       | <span data-ttu-id="cea33-107">Significado</span><span class="sxs-lookup"><span data-stu-id="cea33-107">Meaning</span></span>                                                                |
|-------------|------------------------------------------------------------------------|
| <span data-ttu-id="cea33-108">manual</span><span class="sxs-lookup"><span data-stu-id="cea33-108">"manual"</span></span>    | <span data-ttu-id="cea33-109">Nunca conecte-se automaticamente à rede.</span><span class="sxs-lookup"><span data-stu-id="cea33-109">Never automatically connect to the network.</span></span>                            |
| <span data-ttu-id="cea33-110">detectar</span><span class="sxs-lookup"><span data-stu-id="cea33-110">"auto"</span></span>      | <span data-ttu-id="cea33-111">Sempre conecte-se automaticamente à rede.</span><span class="sxs-lookup"><span data-stu-id="cea33-111">Always automatically connect to the network.</span></span>                           |
| <span data-ttu-id="cea33-112">"auto-Home"</span><span class="sxs-lookup"><span data-stu-id="cea33-112">"auto-home"</span></span> | <span data-ttu-id="cea33-113">Conectar-se automaticamente à rede, exceto quando estiver em uma rede de roaming.</span><span class="sxs-lookup"><span data-stu-id="cea33-113">Automatically connect to the network except when in a roaming network.</span></span> |



 

<span data-ttu-id="cea33-114">Esse elemento pode ter um máximo de uma ocorrência.</span><span class="sxs-lookup"><span data-stu-id="cea33-114">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="cea33-115">Este é um elemento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cea33-115">This is a required element.</span></span>

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="cea33-116">O elemento **ConnectionMode** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cea33-116">The **ConnectionMode** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea33-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cea33-117">Requirements</span></span>



| <span data-ttu-id="cea33-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea33-118">Requirement</span></span> | <span data-ttu-id="cea33-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cea33-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="cea33-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cea33-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cea33-121">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cea33-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="cea33-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cea33-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cea33-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cea33-123">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="cea33-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cea33-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cea33-125">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="cea33-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cea33-126">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="cea33-126">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="cea33-127">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="cea33-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cea33-128">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="cea33-128">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




