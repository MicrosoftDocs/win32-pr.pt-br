---
description: Especifica o número máximo de falhas de autenticação permitidas para um conjunto de credenciais.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Elemento maxAuthFailures (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505853"
---
# <a name="maxauthfailures-onex-element"></a><span data-ttu-id="b463c-103">Elemento maxAuthFailures (OneX)</span><span class="sxs-lookup"><span data-stu-id="b463c-103">maxAuthFailures (OneX) Element</span></span>

<span data-ttu-id="b463c-104">O elemento maxAuthFailures (OneX) especifica o número máximo de falhas de autenticação permitidas para um conjunto de credenciais.</span><span class="sxs-lookup"><span data-stu-id="b463c-104">The maxAuthFailures (OneX) element specifies the maximum number of authentication failures allowed for a set of credentials.</span></span>

<span data-ttu-id="b463c-105">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="b463c-105">This element is optional.</span></span> <span data-ttu-id="b463c-106">Quando maxAuthFailures não é especificado em um perfil, é usado um valor de um.</span><span class="sxs-lookup"><span data-stu-id="b463c-106">When maxAuthFailures is not specified in a profile, a value of one is used.</span></span>

<span data-ttu-id="b463c-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="b463c-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b463c-108">O elemento **maxAuthFailures** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b463c-108">The **maxAuthFailures** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b463c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b463c-109">Requirements</span></span>



| <span data-ttu-id="b463c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b463c-110">Requirement</span></span> | <span data-ttu-id="b463c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b463c-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b463c-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b463c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b463c-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b463c-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b463c-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b463c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b463c-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b463c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b463c-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="b463c-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b463c-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="b463c-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b463c-118">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="b463c-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="b463c-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="b463c-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b463c-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="b463c-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




