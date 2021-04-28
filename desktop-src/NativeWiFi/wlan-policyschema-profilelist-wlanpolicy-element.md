---
description: Elemento ProfileList (WLANPolicy) – contém uma lista de perfis a serem aplicados no nível do domínio ou da máquina.
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
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109194"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="44822-103">Elemento ProfileList (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="44822-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="44822-104">O elemento ProfileList (WLANPolicy) contém uma lista de perfis a serem aplicados no nível do domínio ou da máquina.</span><span class="sxs-lookup"><span data-stu-id="44822-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="44822-105">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="44822-105">This element is optional.</span></span> <span data-ttu-id="44822-106">Se esse elemento estiver presente, ele deverá conter pelo menos um perfil.</span><span class="sxs-lookup"><span data-stu-id="44822-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="44822-107">Os perfis devem ser baseados no [ \_ esquema de perfil de WLAN](wlan-profileschema-schema.md), com um elemento raiz de [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="44822-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

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

<span data-ttu-id="44822-108">O elemento **ProfileList** é definido pelo elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="44822-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="44822-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44822-109">Requirements</span></span>



| <span data-ttu-id="44822-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="44822-110">Requirement</span></span> | <span data-ttu-id="44822-111">Valor</span><span class="sxs-lookup"><span data-stu-id="44822-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44822-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44822-112">Minimum supported client</span></span><br/> | <span data-ttu-id="44822-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44822-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44822-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44822-114">Minimum supported server</span></span><br/> | <span data-ttu-id="44822-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44822-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44822-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="44822-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="44822-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="44822-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="44822-118">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="44822-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="44822-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="44822-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="44822-120">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="44822-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




