---
description: Especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Elemento authPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010990"
---
# <a name="authperiod-onex-element"></a><span data-ttu-id="6bc88-103">Elemento authPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="6bc88-103">authPeriod (OneX) Element</span></span>

<span data-ttu-id="6bc88-104">O elemento authPeriod (OneX) especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador.</span><span class="sxs-lookup"><span data-stu-id="6bc88-104">The authPeriod (OneX) element specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="6bc88-105">Se uma resposta não for recebida dentro do período especificado, o cliente assumirá que não há um autenticador presente na rede.</span><span class="sxs-lookup"><span data-stu-id="6bc88-105">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="6bc88-106">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="6bc88-106">This element is optional.</span></span> <span data-ttu-id="6bc88-107">Quando authPeriod não é especificado em um perfil, é usado um valor de 18 segundos.</span><span class="sxs-lookup"><span data-stu-id="6bc88-107">When authPeriod is not specified in a profile, a value of 18 seconds is used.</span></span>

<span data-ttu-id="6bc88-108">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="6bc88-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="6bc88-109">O elemento **authPeriod** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6bc88-109">The **authPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc88-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bc88-110">Requirements</span></span>



| <span data-ttu-id="6bc88-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bc88-111">Requirement</span></span> | <span data-ttu-id="6bc88-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6bc88-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6bc88-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc88-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6bc88-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6bc88-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6bc88-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc88-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6bc88-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6bc88-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6bc88-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bc88-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6bc88-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="6bc88-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6bc88-119">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="6bc88-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="6bc88-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="6bc88-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6bc88-121">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="6bc88-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




