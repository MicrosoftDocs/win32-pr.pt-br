---
description: Contém uma política de LAN sem fio.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Elemento WLANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091013"
---
# <a name="wlanpolicy-element"></a><span data-ttu-id="7f4e4-103">Elemento WLANPolicy</span><span class="sxs-lookup"><span data-stu-id="7f4e4-103">WLANPolicy Element</span></span>

<span data-ttu-id="7f4e4-104">O elemento **WLANPolicy** contém uma política de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-104">The **WLANPolicy** element contains a wireless LAN policy.</span></span> <span data-ttu-id="7f4e4-105">Esse é o elemento raiz exclusivo para um perfil de política sem fio.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-105">This element is the unique root element for a wireless policy profile.</span></span>

<span data-ttu-id="7f4e4-106">O namespace de destino para o elemento **WLANPolicy** é `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="7f4e4-106">The target namespace for the **WLANPolicy** element is `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
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

## <a name="child-elements"></a><span data-ttu-id="7f4e4-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7f4e4-107">Child elements</span></span>



| <span data-ttu-id="7f4e4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7f4e4-108">Element</span></span>                                                                                                                    | <span data-ttu-id="7f4e4-109">Type</span><span class="sxs-lookup"><span data-stu-id="7f4e4-109">Type</span></span>                                                                     | <span data-ttu-id="7f4e4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f4e4-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f4e4-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="7f4e4-112">booleano</span><span class="sxs-lookup"><span data-stu-id="7f4e4-112">boolean</span></span>                                                                  | <span data-ttu-id="7f4e4-113">Especifica se qualquer usuário pode criar um perfil de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="7f4e4-114">**Lista**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-114">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="7f4e4-115">A lista de redes LAN sem fio às quais qualquer computador deve ter permissão para se conectar.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-115">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/>                                       |
| [<span data-ttu-id="7f4e4-116">**Bloqueios**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="7f4e4-117">A lista de redes LAN sem fio às quais um computador não deve se conectar.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-117">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>                                                    |
| [<span data-ttu-id="7f4e4-118">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-118">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | <span data-ttu-id="7f4e4-119">booleano</span><span class="sxs-lookup"><span data-stu-id="7f4e4-119">boolean</span></span>                                                                  | <span data-ttu-id="7f4e4-120">Especifica se o acesso a todas as redes de infraestrutura está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-120">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                                                           |
| [<span data-ttu-id="7f4e4-121">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-121">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | <span data-ttu-id="7f4e4-122">booleano</span><span class="sxs-lookup"><span data-stu-id="7f4e4-122">boolean</span></span>                                                                  | <span data-ttu-id="7f4e4-123">Especifica se o acesso a todas as redes ad hoc está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-123">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                                                                   |
| [<span data-ttu-id="7f4e4-124">**ndescrição**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-124">**description**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [<span data-ttu-id="7f4e4-125">**nometype**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-125">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="7f4e4-126">A descrição de uma política de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-126">The description of a wireless LAN policy.</span></span> <br/>                                                                                |
| [<span data-ttu-id="7f4e4-127">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-127">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="7f4e4-128">booleano</span><span class="sxs-lookup"><span data-stu-id="7f4e4-128">boolean</span></span>                                                                  | <span data-ttu-id="7f4e4-129">Especifica se os computadores usam o serviço interno de configuração automática (autoconfiguração) para gerenciar conexões sem fio.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-129">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="7f4e4-130">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-130">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="7f4e4-131">Contém as configurações globais para o módulo de configuração automática (ACM).</span><span class="sxs-lookup"><span data-stu-id="7f4e4-131">Contains the global settings for the Auto Configuration Module (ACM).</span></span> <br/>                                                    |
| [<span data-ttu-id="7f4e4-132">**nomes**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-132">**name**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [<span data-ttu-id="7f4e4-133">**nometype**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-133">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="7f4e4-134">O nome de uma política de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-134">The name of a wireless LAN policy.</span></span> <br/>                                                                                       |
| [<span data-ttu-id="7f4e4-135">**rede**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-135">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)                                                             | [<span data-ttu-id="7f4e4-136">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-136">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="7f4e4-137">Uma rede permitida.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-137">An allowed network.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="7f4e4-138">**rede**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-138">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)                                                             | [<span data-ttu-id="7f4e4-139">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-139">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="7f4e4-140">Uma rede bloqueada.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-140">A blocked network.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="7f4e4-141">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-141">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | <span data-ttu-id="7f4e4-142">A lista de redes permitidas e negadas.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-142">The list of allowed and denied networks.</span></span><br/>                                                                                  |
| [<span data-ttu-id="7f4e4-143">**ProfileList**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-143">**profileList**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="7f4e4-144">Contém uma lista de perfis a serem aplicados no nível de domínio ou computador.</span><span class="sxs-lookup"><span data-stu-id="7f4e4-144">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                |
| [<span data-ttu-id="7f4e4-145">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="7f4e4-145">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="7f4e4-146">booleano</span><span class="sxs-lookup"><span data-stu-id="7f4e4-146">boolean</span></span>                                                                  | <span data-ttu-id="7f4e4-147">Especifica se as redes negadas aparecem no assistente **conectar-se a uma rede** .</span><span class="sxs-lookup"><span data-stu-id="7f4e4-147">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="remarks"></a><span data-ttu-id="7f4e4-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f4e4-148">Remarks</span></span>

<span data-ttu-id="7f4e4-149">Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [ \_ elementos do esquema da política de WLAN](wlan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="7f4e4-149">To view the list of child elements in a tree-like structure, see [WLAN\_policy Schema Elements](wlan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f4e4-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f4e4-150">Requirements</span></span>



| <span data-ttu-id="7f4e4-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f4e4-151">Requirement</span></span> | <span data-ttu-id="7f4e4-152">Valor</span><span class="sxs-lookup"><span data-stu-id="7f4e4-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f4e4-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f4e4-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4e4-154">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f4e4-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f4e4-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f4e4-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4e4-156">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f4e4-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




