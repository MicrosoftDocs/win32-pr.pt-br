---
description: Contém um hexBinary de 3 bytes que identifica o IHV.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: Elemento OUI (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770472"
---
# <a name="oui-ouiheader-element"></a><span data-ttu-id="58365-103">Elemento OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="58365-103">OUI (OUIHeader) Element</span></span>

<span data-ttu-id="58365-104">O elemento OUI (OUIHeader) contém um hexBinary de 3 bytes que identifica o IHV.</span><span class="sxs-lookup"><span data-stu-id="58365-104">The OUI (OUIHeader) element contains a 3 byte hexBinary that identifies the IHV.</span></span>

<span data-ttu-id="58365-105">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="58365-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUI">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="58365-106">O elemento é definido pelo elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .</span><span class="sxs-lookup"><span data-stu-id="58365-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="58365-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58365-107">Requirements</span></span>



| <span data-ttu-id="58365-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="58365-108">Requirement</span></span> | <span data-ttu-id="58365-109">Valor</span><span class="sxs-lookup"><span data-stu-id="58365-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58365-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58365-110">Minimum supported client</span></span><br/> | <span data-ttu-id="58365-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58365-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58365-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58365-112">Minimum supported server</span></span><br/> | <span data-ttu-id="58365-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58365-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58365-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="58365-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="58365-115">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="58365-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="58365-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="58365-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="58365-117">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="58365-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="58365-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="58365-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




