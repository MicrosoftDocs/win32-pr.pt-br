---
description: Especifica quando o logon único é executado.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Elemento Type (logon único)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768706"
---
# <a name="type-singlesignon-element"></a><span data-ttu-id="c3bda-103">Elemento Type (logon único)</span><span class="sxs-lookup"><span data-stu-id="c3bda-103">type (singleSignOn) Element</span></span>

<span data-ttu-id="c3bda-104">O elemento Type (logon único) especifica quando o logon único é executado.</span><span class="sxs-lookup"><span data-stu-id="c3bda-104">The type (singleSignOn) element specifies when single sign on is performed.</span></span> <span data-ttu-id="c3bda-105">Quando definido como `preLogon` , o logon único é executado antes de o usuário fazer logon.</span><span class="sxs-lookup"><span data-stu-id="c3bda-105">When set to `preLogon`, single sign on is performed before the user logs on.</span></span> <span data-ttu-id="c3bda-106">Quando definido como `postLogon` , o logon único é executado imediatamente após o usuário fazer logon.</span><span class="sxs-lookup"><span data-stu-id="c3bda-106">When set to `postLogon`, single sign on is performed immediately after the user logs on.</span></span>

<span data-ttu-id="c3bda-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="c3bda-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="c3bda-108">O elemento **Type** é definido pelo elemento [**logon único**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c3bda-108">The **type** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3bda-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3bda-109">Requirements</span></span>



| <span data-ttu-id="c3bda-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3bda-110">Requirement</span></span> | <span data-ttu-id="c3bda-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c3bda-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3bda-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3bda-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c3bda-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3bda-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3bda-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3bda-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c3bda-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3bda-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3bda-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3bda-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3bda-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="c3bda-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c3bda-118">**Logon único**</span><span class="sxs-lookup"><span data-stu-id="c3bda-118">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="c3bda-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="c3bda-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c3bda-120">**Logon único (OneX)**</span><span class="sxs-lookup"><span data-stu-id="c3bda-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




