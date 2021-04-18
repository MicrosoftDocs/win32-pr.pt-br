---
description: Indica o período de tempo, em minutos, que um cache de PMK será mantido.
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: Elemento PMKCacheTTL (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758597"
---
# <a name="pmkcachettl-security-element"></a><span data-ttu-id="8ee53-103">Elemento PMKCacheTTL (segurança)</span><span class="sxs-lookup"><span data-stu-id="8ee53-103">PMKCacheTTL (security) Element</span></span>

<span data-ttu-id="8ee53-104">O elemento PMKCacheTTL (Security) indica o período de tempo, em minutos, que um cache PMK será mantido.</span><span class="sxs-lookup"><span data-stu-id="8ee53-104">The PMKCacheTTL (security) element indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="8ee53-105">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="8ee53-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span>

<span data-ttu-id="8ee53-106">O cache PMK é descrito na especificação [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="8ee53-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="8ee53-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="8ee53-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8ee53-108">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee53-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee53-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee53-109">Requirements</span></span>



| <span data-ttu-id="8ee53-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ee53-110">Requirement</span></span> | <span data-ttu-id="8ee53-111">Valor</span><span class="sxs-lookup"><span data-stu-id="8ee53-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ee53-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ee53-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee53-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ee53-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ee53-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ee53-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee53-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ee53-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ee53-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ee53-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ee53-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="8ee53-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8ee53-118">**segurança**</span><span class="sxs-lookup"><span data-stu-id="8ee53-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="8ee53-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="8ee53-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8ee53-120">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="8ee53-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




