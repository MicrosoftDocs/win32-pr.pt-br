---
title: Elemento User
description: Saiba mais sobre o elemento user. Esse elemento não é usado ao usar métodos herdados por meio de APIs do EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Elemento de usuário EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641865"
---
# <a name="user-element"></a><span data-ttu-id="175eb-105">Elemento User</span><span class="sxs-lookup"><span data-stu-id="175eb-105">User Element</span></span>

<span data-ttu-id="175eb-106">O elemento **User** não é usado ao usar métodos herdados por meio de APIs EAPHost.</span><span class="sxs-lookup"><span data-stu-id="175eb-106">The **User** element is not used when using legacy methods via the EAPHost APIs.</span></span>

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="175eb-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="175eb-107">Child elements</span></span>



| <span data-ttu-id="175eb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="175eb-108">Element</span></span>                                                  | <span data-ttu-id="175eb-109">Type</span><span class="sxs-lookup"><span data-stu-id="175eb-109">Type</span></span> | <span data-ttu-id="175eb-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="175eb-110">Description</span></span>                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="175eb-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="175eb-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md) |      | <span data-ttu-id="175eb-112">Captura o tipo de método e as informações de credencial específicas do método.</span><span class="sxs-lookup"><span data-stu-id="175eb-112">Captures the method type and method specific credential information.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="175eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="175eb-113">Requirements</span></span>



| <span data-ttu-id="175eb-114">Função</span><span class="sxs-lookup"><span data-stu-id="175eb-114">Role</span></span> | <span data-ttu-id="175eb-115">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="175eb-115">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="175eb-116">Cliente</span><span class="sxs-lookup"><span data-stu-id="175eb-116">Client</span></span><br/> | <span data-ttu-id="175eb-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="175eb-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="175eb-118">Servidor</span><span class="sxs-lookup"><span data-stu-id="175eb-118">Server</span></span><br/> | <span data-ttu-id="175eb-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="175eb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="175eb-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="175eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175eb-121">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="175eb-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="175eb-122">Esquema eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="175eb-122">eapuserpropertiesv1 Schema</span></span>](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





