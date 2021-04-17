---
description: Especifica o período de tempo, em segundos, no qual um cliente não tentará realizar a autenticação novamente após uma tentativa de autenticação com falha.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Elemento heldPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780501"
---
# <a name="heldperiod-onex-element"></a><span data-ttu-id="714c8-103">Elemento heldPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="714c8-103">heldPeriod (OneX) Element</span></span>

<span data-ttu-id="714c8-104">O elemento heldPeriod (OneX) especifica o período de tempo, em segundos, no qual um cliente não tentará realizar a autenticação novamente após uma tentativa de autenticação com falha.</span><span class="sxs-lookup"><span data-stu-id="714c8-104">The heldPeriod (OneX) element specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span>

<span data-ttu-id="714c8-105">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="714c8-105">This element is optional.</span></span> <span data-ttu-id="714c8-106">Quando heldPeriod não é especificado em um perfil, é usado um valor de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="714c8-106">When heldPeriod is not specified in a profile, a value of 1 second is used.</span></span>

<span data-ttu-id="714c8-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="714c8-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="714c8-108">O elemento **heldPeriod** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="714c8-108">The **heldPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="714c8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="714c8-109">Requirements</span></span>



| <span data-ttu-id="714c8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="714c8-110">Requirement</span></span> | <span data-ttu-id="714c8-111">Valor</span><span class="sxs-lookup"><span data-stu-id="714c8-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="714c8-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="714c8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="714c8-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="714c8-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="714c8-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="714c8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="714c8-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="714c8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="714c8-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="714c8-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="714c8-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="714c8-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="714c8-118">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="714c8-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="714c8-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="714c8-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="714c8-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="714c8-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




