---
description: Indica se a pré-autenticação será usada pelo cliente.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: Elemento preAuthMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775678"
---
# <a name="preauthmode-security-element"></a><span data-ttu-id="417ca-103">Elemento preAuthMode (Security)</span><span class="sxs-lookup"><span data-stu-id="417ca-103">preAuthMode (security) Element</span></span>

<span data-ttu-id="417ca-104">O elemento preAuthMode (Security) indica se a pré-autenticação será usada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="417ca-104">The preAuthMode (security) element indicates whether pre-authentication will be used by the client.</span></span> <span data-ttu-id="417ca-105">A pré-autenticação é necessária para o roaming rápido seguro do WPA2.</span><span class="sxs-lookup"><span data-stu-id="417ca-105">Pre-authentication is necessary for WPA2 secure fast roaming.</span></span> <span data-ttu-id="417ca-106">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="417ca-106">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="417ca-107">Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o valor padrão será "Disabled".</span><span class="sxs-lookup"><span data-stu-id="417ca-107">If **PMKCacheMode** is enabled, and this element is absent, the default value is "disabled".</span></span>

<span data-ttu-id="417ca-108">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="417ca-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthMode"
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

<span data-ttu-id="417ca-109">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="417ca-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="417ca-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="417ca-110">Requirements</span></span>



| <span data-ttu-id="417ca-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="417ca-111">Requirement</span></span> | <span data-ttu-id="417ca-112">Valor</span><span class="sxs-lookup"><span data-stu-id="417ca-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="417ca-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="417ca-113">Minimum supported client</span></span><br/> | <span data-ttu-id="417ca-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="417ca-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="417ca-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="417ca-115">Minimum supported server</span></span><br/> | <span data-ttu-id="417ca-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="417ca-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="417ca-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="417ca-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="417ca-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="417ca-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="417ca-119">**segurança**</span><span class="sxs-lookup"><span data-stu-id="417ca-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="417ca-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="417ca-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="417ca-121">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="417ca-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




