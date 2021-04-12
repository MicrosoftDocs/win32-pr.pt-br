---
description: Contém as configurações globais para a configuração automática de redes com fio.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Elemento globalFlags (LANPolicy)
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
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170415"
---
# <a name="globalflags-lanpolicy-element"></a><span data-ttu-id="6d0c6-103">Elemento globalFlags (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="6d0c6-103">globalFlags (LANPolicy) Element</span></span>

<span data-ttu-id="6d0c6-104">O elemento globalFlags (LANPolicy) contém as configurações globais para a configuração automática de redes com fio.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-104">The globalFlags (LANPolicy) element contains the global settings for the automatic configuration of wired networks.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
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

<span data-ttu-id="6d0c6-105">O elemento **globalFlags** é definido pelo elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6d0c6-105">The **globalFlags** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6d0c6-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6d0c6-106">Child elements</span></span>



| <span data-ttu-id="6d0c6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6d0c6-107">Element</span></span>                                                                           | <span data-ttu-id="6d0c6-108">Type</span><span class="sxs-lookup"><span data-stu-id="6d0c6-108">Type</span></span>    | <span data-ttu-id="6d0c6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d0c6-109">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d0c6-110">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="6d0c6-110">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="6d0c6-111">booleano</span><span class="sxs-lookup"><span data-stu-id="6d0c6-111">boolean</span></span> | <span data-ttu-id="6d0c6-112">Especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="6d0c6-112">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6d0c6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d0c6-113">Requirements</span></span>



| <span data-ttu-id="6d0c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d0c6-114">Requirement</span></span> | <span data-ttu-id="6d0c6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6d0c6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6d0c6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d0c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6d0c6-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d0c6-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6d0c6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d0c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6d0c6-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6d0c6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d0c6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d0c6-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d0c6-121">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="6d0c6-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6d0c6-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="6d0c6-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="6d0c6-123">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="6d0c6-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6d0c6-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="6d0c6-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




