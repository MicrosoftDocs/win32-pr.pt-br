---
description: Contém várias configurações de conectividade.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: Elemento Connectivity (MSM)
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
ms.openlocfilehash: 938e5b19ffab490066fbbe299bd250191d9226a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758451"
---
# <a name="connectivity-msm-element"></a><span data-ttu-id="8aa69-103">Elemento Connectivity (MSM)</span><span class="sxs-lookup"><span data-stu-id="8aa69-103">connectivity (MSM) Element</span></span>

<span data-ttu-id="8aa69-104">O elemento Connectivity (MSM) contém várias configurações de conectividade.</span><span class="sxs-lookup"><span data-stu-id="8aa69-104">The connectivity (MSM) element contains various connectivity settings.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
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

<span data-ttu-id="8aa69-105">O elemento é definido pelo elemento [**msm**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8aa69-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8aa69-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8aa69-106">Child elements</span></span>



| <span data-ttu-id="8aa69-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8aa69-107">Element</span></span>                                                            | <span data-ttu-id="8aa69-108">Type</span><span class="sxs-lookup"><span data-stu-id="8aa69-108">Type</span></span> |
|--------------------------------------------------------------------|------|
| [<span data-ttu-id="8aa69-109">**phyType**</span><span class="sxs-lookup"><span data-stu-id="8aa69-109">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a><span data-ttu-id="8aa69-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8aa69-110">Examples</span></span>

<span data-ttu-id="8aa69-111">Para exibir perfis de exemplo que usam o elemento de **conectividade** , consulte [exemplos de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8aa69-111">To view sample profiles that use the **connectivity** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa69-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aa69-112">Requirements</span></span>



| <span data-ttu-id="8aa69-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa69-113">Requirement</span></span> | <span data-ttu-id="8aa69-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8aa69-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8aa69-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aa69-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa69-116">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="8aa69-116">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8aa69-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aa69-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa69-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8aa69-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="8aa69-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8aa69-119">Redistributable</span></span><br/>          | <span data-ttu-id="8aa69-120">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="8aa69-120">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8aa69-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8aa69-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="8aa69-122">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="8aa69-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8aa69-123">**MSM**</span><span class="sxs-lookup"><span data-stu-id="8aa69-123">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="8aa69-124">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="8aa69-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8aa69-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8aa69-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




