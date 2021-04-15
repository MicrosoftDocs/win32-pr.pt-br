---
description: Contém as configurações globais para o módulo de configuração automática (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Elemento globalFlags (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506207"
---
# <a name="globalflags-wlanpolicy-element"></a><span data-ttu-id="b79cd-103">Elemento globalFlags (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="b79cd-103">globalFlags (WLANPolicy) Element</span></span>

<span data-ttu-id="b79cd-104">O elemento globalFlags (WLANPolicy) contém as configurações globais para o ACM (módulo de configuração automática).</span><span class="sxs-lookup"><span data-stu-id="b79cd-104">The globalFlags (WLANPolicy) element contains the global settings for the Auto Configuration Module (ACM).</span></span> <span data-ttu-id="b79cd-105">Esse elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b79cd-105">This element is mandatory.</span></span>

``` syntax
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
```

<span data-ttu-id="b79cd-106">O elemento **globalFlags** é definido pelo elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b79cd-106">The **globalFlags** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b79cd-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b79cd-107">Child elements</span></span>



| <span data-ttu-id="b79cd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b79cd-108">Element</span></span>                                                                                                                    | <span data-ttu-id="b79cd-109">Type</span><span class="sxs-lookup"><span data-stu-id="b79cd-109">Type</span></span>    | <span data-ttu-id="b79cd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b79cd-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b79cd-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="b79cd-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="b79cd-112">booleano</span><span class="sxs-lookup"><span data-stu-id="b79cd-112">boolean</span></span> | <span data-ttu-id="b79cd-113">Especifica se qualquer usuário pode criar um perfil de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="b79cd-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="b79cd-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="b79cd-114">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="b79cd-115">booleano</span><span class="sxs-lookup"><span data-stu-id="b79cd-115">boolean</span></span> | <span data-ttu-id="b79cd-116">Especifica se os computadores usam o serviço interno de configuração automática (autoconfiguração) para gerenciar conexões sem fio.</span><span class="sxs-lookup"><span data-stu-id="b79cd-116">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="b79cd-117">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="b79cd-117">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="b79cd-118">booleano</span><span class="sxs-lookup"><span data-stu-id="b79cd-118">boolean</span></span> | <span data-ttu-id="b79cd-119">Especifica se as redes negadas aparecem no assistente **conectar-se a uma rede** .</span><span class="sxs-lookup"><span data-stu-id="b79cd-119">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="requirements"></a><span data-ttu-id="b79cd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b79cd-120">Requirements</span></span>



| <span data-ttu-id="b79cd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b79cd-121">Requirement</span></span> | <span data-ttu-id="b79cd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b79cd-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b79cd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b79cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b79cd-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b79cd-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b79cd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b79cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b79cd-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b79cd-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b79cd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b79cd-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b79cd-128">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="b79cd-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b79cd-129">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="b79cd-129">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="b79cd-130">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="b79cd-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b79cd-131">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="b79cd-131">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




