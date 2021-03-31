---
title: Tipos de variáveis SNMP e tipos de PDU de solicitação
description: As definições para alguns tipos de variáveis SNMP e tipos de PDU de solicitação foram alteradas. O arquivo SNMP. h mapeia os tipos antigos para os novos tipos correspondentes.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641513"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a><span data-ttu-id="40ed2-104">Tipos de variáveis SNMP e tipos de PDU de solicitação</span><span class="sxs-lookup"><span data-stu-id="40ed2-104">SNMP Variable Types and Request PDU Types</span></span>

<span data-ttu-id="40ed2-105">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="40ed2-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="40ed2-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="40ed2-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="40ed2-107">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="40ed2-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="40ed2-108">As definições para alguns tipos de variáveis SNMP e tipos de PDU de solicitação foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="40ed2-108">The definitions for some SNMP variable types and request PDU types have changed.</span></span> <span data-ttu-id="40ed2-109">O arquivo SNMP. h mapeia os tipos antigos para os novos tipos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="40ed2-109">The Snmp.h file maps old types to the corresponding new types.</span></span>

## <a name="modified-snmp-variable-types"></a><span data-ttu-id="40ed2-110">Tipos de variáveis SNMP modificados</span><span class="sxs-lookup"><span data-stu-id="40ed2-110">Modified SNMP Variable Types</span></span>

<span data-ttu-id="40ed2-111">Você deve usar os novos tipos de variáveis SNMP listados na tabela a seguir ao desenvolver aplicativos de Gerenciador que usam a API de gerenciamento SNMP da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="40ed2-111">You should use the new SNMP variable types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="40ed2-112">A tabela lista os tipos de variáveis SNMP antigos com os novos tipos de variáveis correspondentes.</span><span class="sxs-lookup"><span data-stu-id="40ed2-112">The table lists the old SNMP variable types with the corresponding new variable types.</span></span>

| <span data-ttu-id="40ed2-113">Tipo de variável antiga</span><span class="sxs-lookup"><span data-stu-id="40ed2-113">Old variable type</span></span>        | <span data-ttu-id="40ed2-114">Novo tipo de variável</span><span class="sxs-lookup"><span data-stu-id="40ed2-114">New variable type</span></span> |
|--------------------------|-------------------|
| <span data-ttu-id="40ed2-115">\_IPAddress de RFC1155 ASN \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-115">ASN\_RFC1155\_IPADDRESS</span></span>  | <span data-ttu-id="40ed2-116">IPAddress do ASN \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-116">ASN\_IPADDRESS</span></span>    |
| <span data-ttu-id="40ed2-117">\_Contador de RFC1155 ASN \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-117">ASN\_RFC1155\_COUNTER</span></span>    | <span data-ttu-id="40ed2-118">\_COUNTER32 ASN</span><span class="sxs-lookup"><span data-stu-id="40ed2-118">ASN\_COUNTER32</span></span>    |
| <span data-ttu-id="40ed2-119">\_Medidor de RFC1155 ASN \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-119">ASN\_RFC1155\_GAUGE</span></span>      | <span data-ttu-id="40ed2-120">\_GAUGE32 ASN</span><span class="sxs-lookup"><span data-stu-id="40ed2-120">ASN\_GAUGE32</span></span>      |
| <span data-ttu-id="40ed2-121">\_TIMEtiques de RFC1155 ASN \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-121">ASN\_RFC1155\_TIMETICKS</span></span>  | <span data-ttu-id="40ed2-122">\_TIMEtiques ASN</span><span class="sxs-lookup"><span data-stu-id="40ed2-122">ASN\_TIMETICKS</span></span>    |
| <span data-ttu-id="40ed2-123">ASN \_ RFC1155 \_ opaco</span><span class="sxs-lookup"><span data-stu-id="40ed2-123">ASN\_RFC1155\_OPAQUE</span></span>     | <span data-ttu-id="40ed2-124">ASN \_ opaco</span><span class="sxs-lookup"><span data-stu-id="40ed2-124">ASN\_OPAQUE</span></span>       |
| <span data-ttu-id="40ed2-125">Disp. de \_ RFC1213 ASN \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-125">ASN\_RFC1213\_DISPSTRING</span></span> | <span data-ttu-id="40ed2-126">\_octetstring ASN</span><span class="sxs-lookup"><span data-stu-id="40ed2-126">ASN\_OCTETSTRING</span></span>  |



 

## <a name="modified-snmp-pdu-request-types"></a><span data-ttu-id="40ed2-127">Tipos de solicitação de PDU do SNMP modificados</span><span class="sxs-lookup"><span data-stu-id="40ed2-127">Modified SNMP PDU Request Types</span></span>

<span data-ttu-id="40ed2-128">Você deve usar os novos tipos de PDU de SNMP listados na tabela a seguir ao desenvolver aplicativos de Gerenciador que usam a API de gerenciamento SNMP da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="40ed2-128">You should use the new SNMP PDU types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="40ed2-129">A tabela lista os tipos de PDU do SNMP antigos com os novos tipos de PDU correspondentes.</span><span class="sxs-lookup"><span data-stu-id="40ed2-129">The table lists the old SNMP PDU types with the corresponding new PDU types.</span></span>

| <span data-ttu-id="40ed2-130">Tipo antigo de PDU</span><span class="sxs-lookup"><span data-stu-id="40ed2-130">Old PDU type</span></span>                 | <span data-ttu-id="40ed2-131">Novo tipo de PDU</span><span class="sxs-lookup"><span data-stu-id="40ed2-131">New PDU type</span></span>        |
|------------------------------|---------------------|
| <span data-ttu-id="40ed2-132">RFC1157 ASN de \_ \_ solicitação</span><span class="sxs-lookup"><span data-stu-id="40ed2-132">ASN\_RFC1157\_GETREQUEST</span></span>     | <span data-ttu-id="40ed2-133">\_Get SNMP PDU \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-133">SNMP\_PDU\_GET</span></span>      |
| <span data-ttu-id="40ed2-134">\_GETNEXTREQUEST RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="40ed2-134">ASN\_RFC1157\_GETNEXTREQUEST</span></span> | <span data-ttu-id="40ed2-135">o SNMP \_ PDU \_ GetNext</span><span class="sxs-lookup"><span data-stu-id="40ed2-135">SNMP\_PDU\_GETNEXT</span></span>  |
| <span data-ttu-id="40ed2-136">\_GETRESPONSE RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="40ed2-136">ASN\_RFC1157\_GETRESPONSE</span></span>    | <span data-ttu-id="40ed2-137">\_resposta de PDU de SNMP \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-137">SNMP\_PDU\_RESPONSE</span></span> |
| <span data-ttu-id="40ed2-138">RFC1157 ASN de \_ \_ solicitação</span><span class="sxs-lookup"><span data-stu-id="40ed2-138">ASN\_RFC1157\_SETREQUEST</span></span>     | <span data-ttu-id="40ed2-139">\_conjunto de PDU SNMP \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-139">SNMP\_PDU\_SET</span></span>      |
| <span data-ttu-id="40ed2-140">\_ \_ Interceptação ASN RFC1157</span><span class="sxs-lookup"><span data-stu-id="40ed2-140">ASN\_RFC1157\_TRAP</span></span>           | <span data-ttu-id="40ed2-141">\_V1TRAP de PDU SNMP \_</span><span class="sxs-lookup"><span data-stu-id="40ed2-141">SNMP\_PDU\_V1TRAP</span></span>   |



 

 

 