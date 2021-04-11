---
description: Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio. Isso só é usado quando KeyType está definido como &\# 0034; networkKey&\# 0034;.
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: Elemento KeyIndex (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091765"
---
# <a name="keyindex-security-element"></a><span data-ttu-id="46b3f-104">Elemento KeyIndex (Security)</span><span class="sxs-lookup"><span data-stu-id="46b3f-104">keyIndex (security) Element</span></span>

<span data-ttu-id="46b3f-105">O elemento KeyIndex (Security) especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio.</span><span class="sxs-lookup"><span data-stu-id="46b3f-105">The keyIndex (security) element specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="46b3f-106">Isso só é usado quando [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) está definido como "networkKey".</span><span class="sxs-lookup"><span data-stu-id="46b3f-106">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span>

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="46b3f-107">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="46b3f-107">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b3f-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46b3f-108">Requirements</span></span>



| <span data-ttu-id="46b3f-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b3f-109">Requirement</span></span> | <span data-ttu-id="46b3f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="46b3f-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="46b3f-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46b3f-111">Minimum supported client</span></span><br/> | <span data-ttu-id="46b3f-112">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="46b3f-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="46b3f-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46b3f-113">Minimum supported server</span></span><br/> | <span data-ttu-id="46b3f-114">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46b3f-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="46b3f-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="46b3f-115">Redistributable</span></span><br/>          | <span data-ttu-id="46b3f-116">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="46b3f-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="46b3f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="46b3f-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="46b3f-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="46b3f-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="46b3f-119">**segurança**</span><span class="sxs-lookup"><span data-stu-id="46b3f-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="46b3f-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="46b3f-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="46b3f-121">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="46b3f-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




