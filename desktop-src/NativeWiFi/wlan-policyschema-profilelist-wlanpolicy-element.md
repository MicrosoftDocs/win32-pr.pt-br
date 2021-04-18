---
description: Contém uma lista de perfis a serem aplicados no nível de domínio ou computador.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Elemento ProfileList (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769427"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="2d01d-103">Elemento ProfileList (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="2d01d-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="2d01d-104">O elemento ProfileList (WLANPolicy) contém uma lista de perfis a serem aplicados no nível do domínio ou da máquina.</span><span class="sxs-lookup"><span data-stu-id="2d01d-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="2d01d-105">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="2d01d-105">This element is optional.</span></span> <span data-ttu-id="2d01d-106">Se esse elemento estiver presente, ele deverá conter pelo menos um perfil.</span><span class="sxs-lookup"><span data-stu-id="2d01d-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="2d01d-107">Os perfis devem ser baseados no [ \_ esquema de perfil de WLAN](wlan-profileschema-schema.md), com um elemento raiz de [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="2d01d-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2d01d-108">O elemento **ProfileList** é definido pelo elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2d01d-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d01d-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d01d-109">Requirements</span></span>



| <span data-ttu-id="2d01d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d01d-110">Requirement</span></span> | <span data-ttu-id="2d01d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="2d01d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d01d-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d01d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2d01d-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d01d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d01d-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d01d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2d01d-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d01d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d01d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d01d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d01d-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="2d01d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2d01d-118">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="2d01d-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="2d01d-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="2d01d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2d01d-120">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="2d01d-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




