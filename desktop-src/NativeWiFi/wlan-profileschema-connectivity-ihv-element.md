---
description: Contém configurações de conectividade relacionadas a IHV. Ele não está implementado no momento.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: Elemento de conectividade (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 257addbcbd721e5930405e3954dcb348f367af93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647712"
---
# <a name="connectivity-ihv-element"></a><span data-ttu-id="e90dd-104">Elemento de conectividade (IHV)</span><span class="sxs-lookup"><span data-stu-id="e90dd-104">connectivity (IHV) Element</span></span>

<span data-ttu-id="e90dd-105">O elemento de conectividade (IHV) contém configurações de conectividade relacionadas a IHV.</span><span class="sxs-lookup"><span data-stu-id="e90dd-105">The connectivity (IHV) element contains IHV-related connectivity settings.</span></span> <span data-ttu-id="e90dd-106">Ele não está implementado no momento.</span><span class="sxs-lookup"><span data-stu-id="e90dd-106">It is not currently implemented.</span></span>

<span data-ttu-id="e90dd-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="e90dd-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="e90dd-108">O elemento é definido pelo elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e90dd-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90dd-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e90dd-109">Requirements</span></span>



| <span data-ttu-id="e90dd-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90dd-110">Requirement</span></span> | <span data-ttu-id="e90dd-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e90dd-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e90dd-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e90dd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e90dd-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e90dd-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e90dd-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e90dd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e90dd-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e90dd-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e90dd-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="e90dd-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="e90dd-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="e90dd-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e90dd-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="e90dd-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="e90dd-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="e90dd-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e90dd-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e90dd-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




