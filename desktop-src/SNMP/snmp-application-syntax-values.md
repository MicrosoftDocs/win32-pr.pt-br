---
title: Valores de sintaxe de aplicativo SNMP (SNMP. h)
description: Os valores de sintaxe do aplicativo SNMP são usados por aplicativos de gerenciamento que empregam a API de gerenciamento SNMP da Microsoft.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085435"
---
# <a name="snmp-application-syntax-values"></a><span data-ttu-id="940e4-103">Valores de sintaxe do aplicativo SNMP</span><span class="sxs-lookup"><span data-stu-id="940e4-103">SNMP Application Syntax Values</span></span>

<span data-ttu-id="940e4-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="940e4-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="940e4-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="940e4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="940e4-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="940e4-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="940e4-107">Os valores de sintaxe do aplicativo SNMP são usados por aplicativos de gerenciamento que empregam a API de gerenciamento SNMP da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="940e4-107">The SNMP Application Syntax Values are used by management applications that employ the Microsoft SNMP Management API.</span></span>



| <span data-ttu-id="940e4-108">Constante</span><span class="sxs-lookup"><span data-stu-id="940e4-108">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="940e4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="940e4-109">Description</span></span>                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <span data-ttu-id="940e4-110"><dt>**IPAddress do ASN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-110"><dt>**ASN\_IPADDRESS**</dt></span></span> </dl>                             | <span data-ttu-id="940e4-111">Indica uma variável de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="940e4-111">Indicates an IP address variable.</span></span><br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <span data-ttu-id="940e4-112"><dt>**\_COUNTER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-112"><dt>**ASN\_COUNTER32**</dt></span></span> </dl>                             | <span data-ttu-id="940e4-113">Indica uma variável de contador.</span><span class="sxs-lookup"><span data-stu-id="940e4-113">Indicates a counter variable.</span></span><br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <span data-ttu-id="940e4-114"><dt>**\_GAUGE32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-114"><dt>**ASN\_GAUGE32**</dt></span></span> </dl>                                   | <span data-ttu-id="940e4-115">Indica uma variável de medidor.</span><span class="sxs-lookup"><span data-stu-id="940e4-115">Indicates a gauge variable.</span></span> <span data-ttu-id="940e4-116">Essa variável descreve um tipo Unsigned32 em conformidade com RFC 1902.</span><span class="sxs-lookup"><span data-stu-id="940e4-116">This variable describes an Unsigned32 type in conformance with RFC 1902.</span></span><br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <span data-ttu-id="940e4-117"><dt>**\_TIMEtiques ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-117"><dt>**ASN\_TIMETICKS**</dt></span></span> </dl>                             | <span data-ttu-id="940e4-118">Indica uma variável timetiques.</span><span class="sxs-lookup"><span data-stu-id="940e4-118">Indicates a timeticks variable.</span></span><br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <span data-ttu-id="940e4-119"><dt>**ASN \_ opaco**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-119"><dt>**ASN\_OPAQUE**</dt></span></span> </dl>                                      | <span data-ttu-id="940e4-120">Indica uma variável opaca.</span><span class="sxs-lookup"><span data-stu-id="940e4-120">Indicates an opaque variable.</span></span><br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <span data-ttu-id="940e4-121"><dt>**\_COUNTER64 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-121"><dt>**ASN\_COUNTER64**</dt></span></span> </dl>                             | <span data-ttu-id="940e4-122">Indica uma variável de contador que aumenta até atingir um valor máximo de (2 ^ 64)-1.</span><span class="sxs-lookup"><span data-stu-id="940e4-122">Indicates a counter variable that increases until it reaches a maximum value of (2^64) - 1.</span></span><br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <span data-ttu-id="940e4-123"><dt>**\_UINTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-123"><dt>**ASN\_UINTEGER32**</dt></span></span> </dl>                          | <span data-ttu-id="940e4-124">Indica uma variável de inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="940e4-124">Indicates a 32-bit unsigned integer variable.</span></span> <span data-ttu-id="940e4-125">Essa variável descreve um tipo UInteger32 em conformidade com RFC 1442.</span><span class="sxs-lookup"><span data-stu-id="940e4-125">This variable describes a UInteger32 type in conformance with RFC 1442.</span></span><br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <span data-ttu-id="940e4-126"><dt>**\_UNSIGNED32 RFC2578 \_ ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-126"><dt>**ASN\_RFC2578\_UNSIGNED32**</dt></span></span> </dl> | <span data-ttu-id="940e4-127">Consulte \_ GAUGE32 ASN.</span><span class="sxs-lookup"><span data-stu-id="940e4-127">See ASN\_GAUGE32.</span></span><br/>                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="940e4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="940e4-128">Requirements</span></span>



| <span data-ttu-id="940e4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="940e4-129">Requirement</span></span> | <span data-ttu-id="940e4-130">Valor</span><span class="sxs-lookup"><span data-stu-id="940e4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="940e4-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="940e4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="940e4-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="940e4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="940e4-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="940e4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="940e4-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="940e4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="940e4-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="940e4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="940e4-136"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="940e4-136"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940e4-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="940e4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940e4-138">Visão geral do Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="940e4-138">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="940e4-139">Referência de SNMP</span><span class="sxs-lookup"><span data-stu-id="940e4-139">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="940e4-140">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="940e4-140">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

