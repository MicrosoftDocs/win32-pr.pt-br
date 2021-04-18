---
description: Especifica o número de entradas no cache PMK no cliente.
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: Elemento PMKCacheSize (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759191"
---
# <a name="pmkcachesize-security-element"></a><span data-ttu-id="883b7-103">Elemento PMKCacheSize (segurança)</span><span class="sxs-lookup"><span data-stu-id="883b7-103">PMKCacheSize (security) Element</span></span>

<span data-ttu-id="883b7-104">O elemento PMKCacheSize (Security) especifica o número de entradas no cache PMK no cliente.</span><span class="sxs-lookup"><span data-stu-id="883b7-104">The PMKCacheSize (security) element specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="883b7-105">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="883b7-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="883b7-106">Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o tamanho do cache será padronizado para 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="883b7-106">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span>

<span data-ttu-id="883b7-107">O cache PMK é descrito na especificação [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="883b7-107">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="883b7-108">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="883b7-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="883b7-109">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="883b7-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="883b7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="883b7-110">Requirements</span></span>



| <span data-ttu-id="883b7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="883b7-111">Requirement</span></span> | <span data-ttu-id="883b7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="883b7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="883b7-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="883b7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="883b7-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="883b7-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="883b7-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="883b7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="883b7-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="883b7-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="883b7-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="883b7-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="883b7-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="883b7-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="883b7-119">**segurança**</span><span class="sxs-lookup"><span data-stu-id="883b7-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="883b7-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="883b7-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="883b7-121">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="883b7-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




