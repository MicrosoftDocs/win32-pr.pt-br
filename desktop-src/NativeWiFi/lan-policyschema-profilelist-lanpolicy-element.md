---
description: Elemento ProfileList (LANPolicy) – contém uma lista de perfis a serem aplicados no nível do domínio ou da máquina.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Elemento ProfileList (LANPolicy)
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
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090774"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="2bee8-103">Elemento ProfileList (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="2bee8-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="2bee8-104">O elemento ProfileList (LANPolicy) contém uma lista de perfis a serem aplicados no nível do domínio ou da máquina.</span><span class="sxs-lookup"><span data-stu-id="2bee8-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="2bee8-105">Os perfis devem ser baseados no [ \_ esquema de perfil de LAN](lan-profileschema-schema.md), com um elemento raiz de [**LANProfile**](lan-profileschema-lanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="2bee8-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="2bee8-106">Perfis com base em qualquer outro esquema serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="2bee8-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="2bee8-107">Quando [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) é definido como false, esse elemento não deve estar presente em um perfil de política de LAN.</span><span class="sxs-lookup"><span data-stu-id="2bee8-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="2bee8-108">Quando **enableAutoConfig** é definido como true, esse elemento é necessário.</span><span class="sxs-lookup"><span data-stu-id="2bee8-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

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

<span data-ttu-id="2bee8-109">O elemento **ProfileList** é definido pelo elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2bee8-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bee8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bee8-110">Remarks</span></span>

<span data-ttu-id="2bee8-111">Esse elemento deve conter exatamente um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="2bee8-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="2bee8-112">Se mais de um perfil for especificado na política, somente a primeira rede será aplicada.</span><span class="sxs-lookup"><span data-stu-id="2bee8-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bee8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bee8-113">Requirements</span></span>



| <span data-ttu-id="2bee8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bee8-114">Requirement</span></span> | <span data-ttu-id="2bee8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2bee8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bee8-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bee8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2bee8-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2bee8-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2bee8-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bee8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2bee8-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2bee8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bee8-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2bee8-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bee8-121">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="2bee8-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2bee8-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="2bee8-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="2bee8-123">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="2bee8-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2bee8-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="2bee8-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




