---
description: Especifica o número máximo de EAPOL-Start mensagens enviadas.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Elemento maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779608"
---
# <a name="maxstart-onex-element"></a><span data-ttu-id="2f698-103">Elemento maxStart (OneX)</span><span class="sxs-lookup"><span data-stu-id="2f698-103">maxStart (OneX) Element</span></span>

<span data-ttu-id="2f698-104">O elemento maxStart (OneX) especifica o número máximo de EAPOL-Start mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="2f698-104">The maxStart (OneX) element specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="2f698-105">Depois que o número máximo de mensagens de EAPOL-Start tiver sido enviado, o cliente assumirá que não há um autenticador presente na rede.</span><span class="sxs-lookup"><span data-stu-id="2f698-105">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="2f698-106">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="2f698-106">This element is optional.</span></span> <span data-ttu-id="2f698-107">Quando maxStart não é especificado em um perfil, é usado um valor de 3 mensagens.</span><span class="sxs-lookup"><span data-stu-id="2f698-107">When maxStart is not specified in a profile, a value of 3 messages is used.</span></span>

<span data-ttu-id="2f698-108">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="2f698-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxStart">
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

<span data-ttu-id="2f698-109">O elemento **maxStart** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2f698-109">The **maxStart** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f698-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f698-110">Requirements</span></span>



| <span data-ttu-id="2f698-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f698-111">Requirement</span></span> | <span data-ttu-id="2f698-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2f698-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f698-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f698-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2f698-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f698-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2f698-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f698-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2f698-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f698-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f698-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f698-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f698-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="2f698-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2f698-119">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="2f698-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="2f698-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="2f698-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2f698-121">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="2f698-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




