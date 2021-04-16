---
description: Especifica o número de tentativas de pré-autenticação para tentar em APs vizinhos.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Elemento preAuthThrottle (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501556"
---
# <a name="preauththrottle-security-element"></a><span data-ttu-id="a6366-103">Elemento preAuthThrottle (segurança)</span><span class="sxs-lookup"><span data-stu-id="a6366-103">preAuthThrottle (security) Element</span></span>

<span data-ttu-id="a6366-104">O elemento preAuthThrottle (segurança) especifica o número de tentativas de pré-autenticação para tentar em APs vizinhos.</span><span class="sxs-lookup"><span data-stu-id="a6366-104">The preAuthThrottle (security) element specifies the number pre-authentication attempts to try on neighboring APs.</span></span> <span data-ttu-id="a6366-105">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="a6366-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="a6366-106">Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o número de tentativas padrão será 3.</span><span class="sxs-lookup"><span data-stu-id="a6366-106">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span>

<span data-ttu-id="a6366-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="a6366-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthThrottle"
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
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a6366-108">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a6366-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6366-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6366-109">Requirements</span></span>



| <span data-ttu-id="a6366-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6366-110">Requirement</span></span> | <span data-ttu-id="a6366-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a6366-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a6366-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6366-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a6366-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6366-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a6366-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6366-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a6366-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6366-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6366-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6366-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6366-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a6366-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a6366-118">**segurança**</span><span class="sxs-lookup"><span data-stu-id="a6366-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="a6366-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a6366-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a6366-120">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="a6366-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




