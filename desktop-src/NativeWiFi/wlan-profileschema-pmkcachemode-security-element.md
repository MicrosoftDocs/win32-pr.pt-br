---
description: Indica se o cache PMK será usado.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Elemento PMKCacheMode (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090220"
---
# <a name="pmkcachemode-security-element"></a><span data-ttu-id="5d2e7-103">Elemento PMKCacheMode (segurança)</span><span class="sxs-lookup"><span data-stu-id="5d2e7-103">PMKCacheMode (security) Element</span></span>

<span data-ttu-id="5d2e7-104">O elemento PMKCacheMode (Security) indica se o cache PMK será usado.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-104">The PMKCacheMode (security) element indicates whether PMK caching will be used.</span></span> <span data-ttu-id="5d2e7-105">Esse elemento é válido somente para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-105">This element is valid only for WPA2-defined networks.</span></span> <span data-ttu-id="5d2e7-106">O cache PMK é descrito na especificação [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="5d2e7-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="5d2e7-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="5d2e7-108">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2e7-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2e7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d2e7-109">Requirements</span></span>



| <span data-ttu-id="5d2e7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d2e7-110">Requirement</span></span> | <span data-ttu-id="5d2e7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5d2e7-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5d2e7-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d2e7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2e7-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d2e7-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5d2e7-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d2e7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2e7-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d2e7-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d2e7-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d2e7-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d2e7-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="5d2e7-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5d2e7-118">**segurança**</span><span class="sxs-lookup"><span data-stu-id="5d2e7-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="5d2e7-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="5d2e7-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5d2e7-120">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="5d2e7-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




