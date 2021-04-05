---
title: Tipos de interceptação SNMPv1 (SNMP. h)
description: Os tipos de interceptação SNMPv1 descrevem um conjunto predefinido de tipos de interceptação genéricos que são formatados para serem compatíveis com o padrão de PDU de interceptação SNMPv1.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824785"
---
# <a name="snmpv1-trap-types"></a><span data-ttu-id="83cfd-103">Tipos de interceptação SNMPv1</span><span class="sxs-lookup"><span data-stu-id="83cfd-103">SNMPv1 Trap Types</span></span>

<span data-ttu-id="83cfd-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="83cfd-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="83cfd-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="83cfd-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="83cfd-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="83cfd-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="83cfd-107">Os tipos de interceptação SNMPv1 descrevem um conjunto predefinido de tipos de interceptação genéricos que são formatados para serem compatíveis com o padrão de PDU de interceptação SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="83cfd-107">The SNMPv1 trap types describe a predefined set of generic trap types that are formatted to comply with the SNMPv1 trap PDU standard.</span></span>



| <span data-ttu-id="83cfd-108">Constante</span><span class="sxs-lookup"><span data-stu-id="83cfd-108">Constant</span></span>                                                                                                                                                                                                          | <span data-ttu-id="83cfd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="83cfd-109">Description</span></span>                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <span data-ttu-id="83cfd-110"><dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-110"><dt>**SNMP\_GENERICTRAP\_COLDSTART**</dt></span></span> </dl>             | <span data-ttu-id="83cfd-111">Indica uma interceptação de início frio.</span><span class="sxs-lookup"><span data-stu-id="83cfd-111">Indicates a cold start trap.</span></span> <span data-ttu-id="83cfd-112">O agente está inicializando entidades de protocolo no modo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="83cfd-112">The agent is initializing protocol entities on the managed mode.</span></span> <span data-ttu-id="83cfd-113">Ele pode alterar objetos em sua exibição.</span><span class="sxs-lookup"><span data-stu-id="83cfd-113">It may alter objects in its view.</span></span><br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <span data-ttu-id="83cfd-114"><dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-114"><dt>**SNMP\_GENERICTRAP\_WARMSTART**</dt></span></span> </dl>             | <span data-ttu-id="83cfd-115">Indica uma interceptação de início quente.</span><span class="sxs-lookup"><span data-stu-id="83cfd-115">Indicates a warm start trap.</span></span> <span data-ttu-id="83cfd-116">O agente está reinicializando a si mesmo, mas não alterará objetos em sua exibição.</span><span class="sxs-lookup"><span data-stu-id="83cfd-116">The agent is reinitializing itself but it will not alter objects in its view.</span></span><br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <span data-ttu-id="83cfd-117"><dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-117"><dt>**SNMP\_GENERICTRAP\_LINKDOWN**</dt></span></span> </dl>                | <span data-ttu-id="83cfd-118">Indica uma interceptação de vínculo abaixo.</span><span class="sxs-lookup"><span data-stu-id="83cfd-118">Indicates a link-down trap.</span></span> <span data-ttu-id="83cfd-119">Uma interface anexada foi alterada do estado para baixo para o estado inoperante.</span><span class="sxs-lookup"><span data-stu-id="83cfd-119">An attached interface has changed from the up state to the down state.</span></span> <span data-ttu-id="83cfd-120">A primeira variável na lista de associações de variáveis identifica a interface.</span><span class="sxs-lookup"><span data-stu-id="83cfd-120">The first variable in the variable bindings list identifies the interface.</span></span><br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <span data-ttu-id="83cfd-121"><dt>**SNMP \_ GENERICTRAP \_ linkup**</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-121"><dt>**SNMP\_GENERICTRAP\_LINKUP**</dt></span></span> </dl>                      | <span data-ttu-id="83cfd-122">Indica uma interceptação de vínculo.</span><span class="sxs-lookup"><span data-stu-id="83cfd-122">Indicates a link-up trap.</span></span> <span data-ttu-id="83cfd-123">Uma interface anexada foi alterada do estado de início para cima.</span><span class="sxs-lookup"><span data-stu-id="83cfd-123">An attached interface has changed from the down start to the up state.</span></span> <span data-ttu-id="83cfd-124">A primeira variável na lista de associações de variáveis identifica a interface.</span><span class="sxs-lookup"><span data-stu-id="83cfd-124">The first variable in the variable bindings list identifies the interface.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <span data-ttu-id="83cfd-125"><dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-125"><dt>**SNMP\_GENERICTRAP\_AUTHFAILURE**</dt></span></span> </dl>       | <span data-ttu-id="83cfd-126">Indica uma interceptação de falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="83cfd-126">Indicates an authentication failure trap.</span></span> <span data-ttu-id="83cfd-127">Uma entidade SNMP enviou uma mensagem SNMP, mas, de forma falsa, pediu para pertencer a uma comunidade conhecida.</span><span class="sxs-lookup"><span data-stu-id="83cfd-127">An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.</span></span><br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <span data-ttu-id="83cfd-128"><dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-128"><dt>**SNMP\_GENERICTRAP\_EGPNEIGHLOSS**</dt></span></span> </dl>    | <span data-ttu-id="83cfd-129">Indica uma interceptação de perda de vizinho EGP.</span><span class="sxs-lookup"><span data-stu-id="83cfd-129">Indicates an EGP neighbor loss trap.</span></span> <span data-ttu-id="83cfd-130">Um par EGP foi alterado para o estado inoperante.</span><span class="sxs-lookup"><span data-stu-id="83cfd-130">An EGP peer has changed to the down state.</span></span> <span data-ttu-id="83cfd-131">A primeira variável na lista de associações de variáveis identifica o endereço IP do par EGP.</span><span class="sxs-lookup"><span data-stu-id="83cfd-131">The first variable in the variable bindings list identifies the IP address of the EGP peer.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <span data-ttu-id="83cfd-132"><dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-132"><dt>**SNMP\_GENERICTRAP\_ENTERSPECIFIC**</dt></span></span> </dl> | <span data-ttu-id="83cfd-133">Indica uma interceptação específica da empresa.</span><span class="sxs-lookup"><span data-stu-id="83cfd-133">Indicates an enterprise-specific trap.</span></span> <span data-ttu-id="83cfd-134">Ocorreu um evento extraordinário.</span><span class="sxs-lookup"><span data-stu-id="83cfd-134">An extraordinary event has occurred.</span></span> <span data-ttu-id="83cfd-135">Ele é identificado no parâmetro *specificTrap* com um valor específico da empresa.</span><span class="sxs-lookup"><span data-stu-id="83cfd-135">It is identified in the *specificTrap* parameter with an enterprise-specific value.</span></span><br/>               |



## <a name="requirements"></a><span data-ttu-id="83cfd-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83cfd-136">Requirements</span></span>



| <span data-ttu-id="83cfd-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="83cfd-137">Requirement</span></span> | <span data-ttu-id="83cfd-138">Valor</span><span class="sxs-lookup"><span data-stu-id="83cfd-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="83cfd-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83cfd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="83cfd-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83cfd-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="83cfd-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83cfd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="83cfd-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83cfd-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="83cfd-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="83cfd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="83cfd-144"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="83cfd-144"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83cfd-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="83cfd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83cfd-146">Visão geral do Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="83cfd-146">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="83cfd-147">Referência de SNMP</span><span class="sxs-lookup"><span data-stu-id="83cfd-147">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="83cfd-148">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="83cfd-148">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

