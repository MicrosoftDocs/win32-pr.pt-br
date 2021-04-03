---
description: Contém um hexBinary de 1 byte que é usado para diferenciar as NICs feitas pelo mesmo IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Elemento Type (OUIHeader)
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
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828844"
---
# <a name="type-ouiheader-element"></a><span data-ttu-id="3fe18-103">Elemento Type (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="3fe18-103">type (OUIHeader) Element</span></span>

<span data-ttu-id="3fe18-104">O elemento Type (OUIHeader) contém um hexBinary de 1 byte que é usado para diferenciar as NICs feitas pelo mesmo IHV.</span><span class="sxs-lookup"><span data-stu-id="3fe18-104">The type (OUIHeader) element contains a 1-byte hexBinary that is used to differentiate between NICs made by the same IHV.</span></span>

<span data-ttu-id="3fe18-105">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="3fe18-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="type">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="3fe18-106">O elemento é definido pelo elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe18-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fe18-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fe18-107">Requirements</span></span>



| <span data-ttu-id="3fe18-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fe18-108">Requirement</span></span> | <span data-ttu-id="3fe18-109">Valor</span><span class="sxs-lookup"><span data-stu-id="3fe18-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fe18-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fe18-110">Minimum supported client</span></span><br/> | <span data-ttu-id="3fe18-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fe18-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3fe18-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fe18-112">Minimum supported server</span></span><br/> | <span data-ttu-id="3fe18-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fe18-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fe18-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fe18-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="3fe18-115">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="3fe18-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3fe18-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="3fe18-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="3fe18-117">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="3fe18-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3fe18-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="3fe18-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




