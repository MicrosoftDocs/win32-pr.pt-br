---
title: Tipos de solicitação SNMP (SNMP. h)
description: Os tipos de solicitação SNMP são usados para descrever a operação que o serviço SNMP está solicitando que o agente de extensão execute.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455717"
---
# <a name="snmp-request-types"></a><span data-ttu-id="d1dfc-103">Tipos de solicitação SNMP</span><span class="sxs-lookup"><span data-stu-id="d1dfc-103">SNMP Request Types</span></span>

<span data-ttu-id="d1dfc-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d1dfc-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d1dfc-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="d1dfc-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="d1dfc-107">Os tipos de solicitação SNMP são usados para descrever a operação que o serviço SNMP está solicitando que o agente de extensão execute.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-107">The SNMP Request Types are used to describe the operation that the SNMP service is requesting the extension agent to perform.</span></span>



| <span data-ttu-id="d1dfc-108">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="d1dfc-108">Constant/value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="d1dfc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1dfc-109">Description</span></span>                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <span data-ttu-id="d1dfc-110"><dt>**SNMP \_ EXTENSÃO \_ obter**</dt> <dt>SNMP \_ PDU \_ Get</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfc-110"><dt>**SNMP\_EXTENSION\_GET**</dt> <dt>SNMP\_PDU\_GET</dt></span></span> </dl>                       | <span data-ttu-id="d1dfc-111">Recupere o valor de valores das variáveis especificadas.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-111">Retrieve the value of values of the specified variables.</span></span><br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <span data-ttu-id="d1dfc-112"><dt>**SNMP \_ EXTENSÃO \_ obter \_ próximo**</dt> <dt>SNMP \_ PDU \_ GetNext</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfc-112"><dt>**SNMP\_EXTENSION\_GET\_NEXT**</dt> <dt>SNMP\_PDU\_GETNEXT</dt></span></span> </dl>   | <span data-ttu-id="d1dfc-113">Recupere o valor ou os valores do sucessor lexicográfica das variáveis especificadas.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-113">Retrieve the value or values of the lexicographic successor of the specified variables.</span></span><br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <span data-ttu-id="d1dfc-114"><dt>**SNMP \_ EXTENSÃO \_ obter \_**</dt> o <dt>SNMP \_ PDU \_</dt> em massa/massa</span><span class="sxs-lookup"><span data-stu-id="d1dfc-114"><dt>**SNMP\_EXTENSION\_GET\_BULK**</dt> <dt>SNMP\_PDU\_GETBULK</dt></span></span> </dl>   | <span data-ttu-id="d1dfc-115">Pesquise e recupere vários valores com uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-115">Search and retrieve multiple values with a single request.</span></span><br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <span data-ttu-id="d1dfc-116"><dt>**\_teste de \_ conjunto de extensões SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfc-116"><dt>**SNMP\_EXTENSION\_SET\_TEST**</dt></span></span> </dl>                                                                           | <span data-ttu-id="d1dfc-117">Valide os valores das variáveis especificadas.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-117">Validate the values of the specified variables.</span></span> <span data-ttu-id="d1dfc-118">Esta operação maximiza a probabilidade de uma operação de gravação bem-sucedida durante a solicitação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-118">This operation maximizes the probability of a successful write operation during the COMMIT request.</span></span> <span data-ttu-id="d1dfc-119">Para obter mais informações, consulte a função [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .</span><span class="sxs-lookup"><span data-stu-id="d1dfc-119">For more information, see the [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) function.</span></span><br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <span data-ttu-id="d1dfc-120"><dt>**SNMP \_ conjunto de extensões \_ \_ confirmar**</dt> <dt> \_ \_ conjunto de PDU SNMP</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfc-120"><dt>**SNMP\_EXTENSION\_SET\_COMMIT**</dt> <dt>SNMP\_PDU\_SET</dt></span></span> </dl> | <span data-ttu-id="d1dfc-121">Grave os novos valores nas variáveis especificadas.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-121">Write the new values to the specified variables.</span></span><br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <span data-ttu-id="d1dfc-122"><dt>**\_desfazer do \_ conjunto de extensões SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfc-122"><dt>**SNMP\_EXTENSION\_SET\_UNDO**</dt></span></span> </dl>                                                                           | <span data-ttu-id="d1dfc-123">Redefina os valores das variáveis especificadas para seus valores antes da solicitação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-123">Reset the values of the specified variables to their values before the COMMIT request.</span></span><br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <span data-ttu-id="d1dfc-124"><dt>**\_limpeza do \_ conjunto de extensões SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfc-124"><dt>**SNMP\_EXTENSION\_SET\_CLEANUP**</dt></span></span> </dl>                                                                  | <span data-ttu-id="d1dfc-125">Libere os recursos alocados em operações e solicitações anteriores.</span><span class="sxs-lookup"><span data-stu-id="d1dfc-125">Release the resources allocated in previous requests and operations.</span></span><br/>                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="d1dfc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1dfc-126">Requirements</span></span>



| <span data-ttu-id="d1dfc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1dfc-127">Requirement</span></span> | <span data-ttu-id="d1dfc-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d1dfc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d1dfc-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1dfc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d1dfc-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1dfc-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="d1dfc-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1dfc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d1dfc-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1dfc-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d1dfc-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1dfc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1dfc-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1dfc-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1dfc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1dfc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1dfc-136">Visão geral do Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="d1dfc-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="d1dfc-137">Referência de SNMP</span><span class="sxs-lookup"><span data-stu-id="d1dfc-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="d1dfc-138">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="d1dfc-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

