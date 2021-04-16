---
description: Identifica o IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Elemento OUIHeader (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787049"
---
# <a name="ouiheader-ihv-element"></a><span data-ttu-id="05dc7-103">Elemento OUIHeader (IHV)</span><span class="sxs-lookup"><span data-stu-id="05dc7-103">OUIHeader (IHV) Element</span></span>

<span data-ttu-id="05dc7-104">O elemento OUIHeader (IHV) identifica o IHV.</span><span class="sxs-lookup"><span data-stu-id="05dc7-104">The OUIHeader (IHV) element identifies the IHV.</span></span>

<span data-ttu-id="05dc7-105">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="05dc7-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
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
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="05dc7-106">O elemento é definido pelo elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="05dc7-106">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="05dc7-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="05dc7-107">Child elements</span></span>



| <span data-ttu-id="05dc7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="05dc7-108">Element</span></span>                                                   | <span data-ttu-id="05dc7-109">Type</span><span class="sxs-lookup"><span data-stu-id="05dc7-109">Type</span></span> | <span data-ttu-id="05dc7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="05dc7-110">Description</span></span>                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05dc7-111">**OUI**</span><span class="sxs-lookup"><span data-stu-id="05dc7-111">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)   |      | <span data-ttu-id="05dc7-112">Contém um hexBinary de 3 bytes que identifica o IHV.</span><span class="sxs-lookup"><span data-stu-id="05dc7-112">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                            |
| [<span data-ttu-id="05dc7-113">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="05dc7-113">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md) |      | <span data-ttu-id="05dc7-114">Contém um hexBinary de 1 byte que é usado para diferenciar NICs pelo mesmo IHV.</span><span class="sxs-lookup"><span data-stu-id="05dc7-114">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="05dc7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05dc7-115">Requirements</span></span>



| <span data-ttu-id="05dc7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="05dc7-116">Requirement</span></span> | <span data-ttu-id="05dc7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="05dc7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05dc7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05dc7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05dc7-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05dc7-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05dc7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05dc7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05dc7-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05dc7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05dc7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="05dc7-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="05dc7-123">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="05dc7-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="05dc7-124">**IHV**</span><span class="sxs-lookup"><span data-stu-id="05dc7-124">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="05dc7-125">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="05dc7-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="05dc7-126">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="05dc7-126">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




