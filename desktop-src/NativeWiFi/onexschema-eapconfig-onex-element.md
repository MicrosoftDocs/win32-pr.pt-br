---
description: Especifica a configuração do EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Elemento EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766853"
---
# <a name="eapconfig-onex-element"></a><span data-ttu-id="f2bea-103">Elemento EAPConfig (OneX)</span><span class="sxs-lookup"><span data-stu-id="f2bea-103">EAPConfig (OneX) Element</span></span>

<span data-ttu-id="f2bea-104">O elemento **EAPConfig** (Onex) especifica a configuração do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="f2bea-104">The **EAPConfig** (OneX) element specifies the EAPHost configuration.</span></span>

<span data-ttu-id="f2bea-105">Ao contrário da maioria dos elementos no esquema de perfil 802.1 X, esse elemento está no `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span><span class="sxs-lookup"><span data-stu-id="f2bea-105">Unlike most elements in the 802.1X profile schema, this element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span> <span data-ttu-id="f2bea-106">Seus elementos filho são definidos no [esquema eaphostconfig](../eaphost/eaphostconfigschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="f2bea-106">Its child elements are defined in the [eaphostconfig schema](../eaphost/eaphostconfigschema-schema.md).</span></span> <span data-ttu-id="f2bea-107">O elemento [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) é um filho do elemento **EAPConfig** .</span><span class="sxs-lookup"><span data-stu-id="f2bea-107">The [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) element is a child of the **EAPConfig** element.</span></span>

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f2bea-108">O elemento **EAPConfig** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f2bea-108">The **EAPConfig** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bea-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2bea-109">Requirements</span></span>



| <span data-ttu-id="f2bea-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2bea-110">Requirement</span></span> | <span data-ttu-id="f2bea-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f2bea-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f2bea-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2bea-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bea-113">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f2bea-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f2bea-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2bea-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bea-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f2bea-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f2bea-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f2bea-116">Redistributable</span></span><br/>          | <span data-ttu-id="f2bea-117">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="f2bea-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f2bea-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2bea-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2bea-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f2bea-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f2bea-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="f2bea-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="f2bea-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f2bea-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f2bea-122">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="f2bea-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
