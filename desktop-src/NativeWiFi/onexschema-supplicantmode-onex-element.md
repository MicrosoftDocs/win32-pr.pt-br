---
description: Especifica o método de transmissão usado para EAPOL-Start mensagens.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Elemento suplicable (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775681"
---
# <a name="supplicantmode-onex-element"></a><span data-ttu-id="8ed7b-103">Elemento suplicable (OneX)</span><span class="sxs-lookup"><span data-stu-id="8ed7b-103">supplicantMode (OneX) Element</span></span>

<span data-ttu-id="8ed7b-104">O elemento suplicable (OneX) especifica o método de transmissão usado para EAPOL-Start mensagens.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-104">The supplicantMode (OneX) element specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="8ed7b-105">A tabela a seguir descreve os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="8ed7b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8ed7b-106">Value</span></span>               | <span data-ttu-id="8ed7b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ed7b-107">Description</span></span>                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed7b-108">inhibitTransmission</span><span class="sxs-lookup"><span data-stu-id="8ed7b-108">inhibitTransmission</span></span> | <span data-ttu-id="8ed7b-109">EAPOL-Start mensagens não são transmitidas.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-109">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="8ed7b-110">Válido somente para perfis de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-110">Valid for wired LAN profiles only.</span></span>                                                                                             |
| <span data-ttu-id="8ed7b-111">includeLearning</span><span class="sxs-lookup"><span data-stu-id="8ed7b-111">includeLearning</span></span>     | <span data-ttu-id="8ed7b-112">O cliente determina quando enviar EAPOL-Start pacotes com base na capacidade de rede.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-112">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="8ed7b-113">EAPOL-Start mensagens são enviadas somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-113">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="8ed7b-114">Válido somente para perfis de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-114">Valid for wired LAN profiles only.</span></span> |
| <span data-ttu-id="8ed7b-115">conformidade</span><span class="sxs-lookup"><span data-stu-id="8ed7b-115">compliant</span></span>           | <span data-ttu-id="8ed7b-116">EAPOL-Start mensagens são transmitidas conforme especificado pelo 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-116">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="8ed7b-117">Válido para perfis de LAN com e sem fio.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-117">Valid for both wired and wireless LAN profiles.</span></span>                                                             |



 

<span data-ttu-id="8ed7b-118">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-118">This element is optional.</span></span> <span data-ttu-id="8ed7b-119">Quando suplicamode não é especificado em um perfil, um valor de `compliant` é usado para perfis de LAN com e sem fio.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-119">When supplicantMode is not specified in a profile, a value of `compliant` is used for both wired and wireless LAN profiles.</span></span>

<span data-ttu-id="8ed7b-120">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="8ed7b-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8ed7b-121">O elemento **suplicamode** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8ed7b-121">The **supplicantMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed7b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ed7b-122">Requirements</span></span>



| <span data-ttu-id="8ed7b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed7b-123">Requirement</span></span> | <span data-ttu-id="8ed7b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8ed7b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ed7b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ed7b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed7b-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ed7b-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ed7b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ed7b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed7b-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ed7b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ed7b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ed7b-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ed7b-130">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="8ed7b-130">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8ed7b-131">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="8ed7b-131">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="8ed7b-132">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="8ed7b-132">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8ed7b-133">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="8ed7b-133">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




