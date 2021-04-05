---
title: Identificadores de direito de acesso (Fwpmu. h)
description: A WFP (Windows Filtering Platform) usa os direitos de acesso padrão do Win32, além de um conjunto de direitos de acesso específicos de WFP incorporados à plataforma de filtragem.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919120"
---
# <a name="access-right-identifiers"></a><span data-ttu-id="943be-103">Identificadores de direito de acesso</span><span class="sxs-lookup"><span data-stu-id="943be-103">Access Right Identifiers</span></span>

<span data-ttu-id="943be-104">A WFP (Windows Filtering Platform) usa os [direitos de acesso padrão do Win32](/windows/desktop/SecAuthZ/standard-access-rights) , além de um conjunto de direitos de acesso específicos de WFP incorporados à plataforma de filtragem.</span><span class="sxs-lookup"><span data-stu-id="943be-104">Windows Filtering Platform (WFP) uses the [standard Win32 access rights](/windows/desktop/SecAuthZ/standard-access-rights) plus a set of WFP-specific access rights built into the filtering platform.</span></span> <span data-ttu-id="943be-105">Esses direitos de acesso são usados para proteger objetos somente no modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="943be-105">These access rights are used to secure objects in user mode only.</span></span> <span data-ttu-id="943be-106">Os chamadores de modo kernel ignoram todas as verificações de acesso.</span><span class="sxs-lookup"><span data-stu-id="943be-106">Kernel-mode callers bypass all access checks.</span></span>

<span data-ttu-id="943be-107">Os identificadores corretos de acesso específico à WFP são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="943be-107">WFP specific access right identifiers are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="943be-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="943be-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-109">Adicione um objeto ao mecanismo de filtragem base (BFE).</span><span class="sxs-lookup"><span data-stu-id="943be-109">Add an object to the Base Filtering Engine (BFE).</span></span> <span data-ttu-id="943be-110">Esse direito de acesso é necessário para chamar as funções do [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .</span><span class="sxs-lookup"><span data-stu-id="943be-110">This access right is needed in order to call [**Fwpm\*Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Add \_ link**</span><span class="sxs-lookup"><span data-stu-id="943be-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-112">Adicione um objeto referenciado por meio de um link.</span><span class="sxs-lookup"><span data-stu-id="943be-112">Add an object referenced through a link.</span></span> <span data-ttu-id="943be-113">Por exemplo, esse direito de acesso é necessário para textos explicativos referenciados por meio de GUIDs.</span><span class="sxs-lookup"><span data-stu-id="943be-113">For example, this access right is needed for callouts referenced through GUIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ begin \_ Read \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="943be-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-115">Iniciar uma transação somente leitura.</span><span class="sxs-lookup"><span data-stu-id="943be-115">Begin a read-only transaction.</span></span> <span data-ttu-id="943be-116">Esse direito de acesso é necessário para chamar [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span><span class="sxs-lookup"><span data-stu-id="943be-116">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="943be-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-118">Iniciar uma transação de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="943be-118">Begin a read/write transaction.</span></span> <span data-ttu-id="943be-119">Esse direito de acesso é necessário para chamar [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) para uma transação de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="943be-119">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) for a read/write transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ classificar**</span><span class="sxs-lookup"><span data-stu-id="943be-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-121">Classificar RPC (chamada de procedimento remoto).</span><span class="sxs-lookup"><span data-stu-id="943be-121">Classify Remote Procedure Call (RPC).</span></span> <span data-ttu-id="943be-122">Esse direito de acesso é necessário para o tempo de execução de RPC a fim de impor filtros RPC.</span><span class="sxs-lookup"><span data-stu-id="943be-122">This access right is needed by the RPC run-time in order to enforce RPC filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ enum**</span><span class="sxs-lookup"><span data-stu-id="943be-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-124">Enumera.</span><span class="sxs-lookup"><span data-stu-id="943be-124">Enumerate.</span></span> <span data-ttu-id="943be-125">Esse direito de acesso é necessário para chamar as funções do [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) .</span><span class="sxs-lookup"><span data-stu-id="943be-125">This access right is needed in order to call [**Fwpm\*CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) functions.</span></span> <span data-ttu-id="943be-126">Para enumerar um objeto, o chamador também precisa \_ de \_ acesso de leitura do FWPM ACTRL ao objeto.</span><span class="sxs-lookup"><span data-stu-id="943be-126">To enumerate an object, the caller also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="943be-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-128">Abra uma sessão para o mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="943be-128">Open a session to the filter engine.</span></span> <span data-ttu-id="943be-129">Esse direito de acesso é necessário para chamar [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="943be-129">This access right is needed in order to call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="943be-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-131">Leitura.</span><span class="sxs-lookup"><span data-stu-id="943be-131">Read.</span></span> <span data-ttu-id="943be-132">Esse direito de acesso é necessário para chamar as funções [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) e [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .</span><span class="sxs-lookup"><span data-stu-id="943be-132">This access right is needed in order to call [**Fwpm\*GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) and [**Fwpm\*GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ Read \_ stats**</span><span class="sxs-lookup"><span data-stu-id="943be-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-134">Ler estatísticas.</span><span class="sxs-lookup"><span data-stu-id="943be-134">Read statistics.</span></span> <span data-ttu-id="943be-135">Esse direito de acesso é necessário para chamar [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) e [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span><span class="sxs-lookup"><span data-stu-id="943be-135">This access right is needed in order to call [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) and [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ assinatura**</span><span class="sxs-lookup"><span data-stu-id="943be-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-137">Inscrever-se.</span><span class="sxs-lookup"><span data-stu-id="943be-137">Subscribe.</span></span> <span data-ttu-id="943be-138">Esse direito de acesso é necessário para chamar as funções do [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) .</span><span class="sxs-lookup"><span data-stu-id="943be-138">This access right is needed in order to call [**Fwpm\*SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) functions.</span></span> <span data-ttu-id="943be-139">Para receber uma notificação de um objeto, um assinante também precisa \_ de \_ acesso de leitura do FWPM ACTRL ao objeto.</span><span class="sxs-lookup"><span data-stu-id="943be-139">To receive a notification for an object, a subscriber also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="943be-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-141">Opções do mecanismo de gravação.</span><span class="sxs-lookup"><span data-stu-id="943be-141">Write engine options.</span></span> <span data-ttu-id="943be-142">Esse direito de acesso é necessário para chamar [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span><span class="sxs-lookup"><span data-stu-id="943be-142">This access right is needed in order to call [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_leitura genérica do FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="943be-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-144">STANDARD \_ Rights \_ Read \| FWPM \_ ACTRL \_ begin \_ Read \_ TXN \| FWPM \_ ACTRL \_ classificar \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM ACTRL \_ \_ Read \_ stats</span><span class="sxs-lookup"><span data-stu-id="943be-144">STANDARD\_RIGHTS\_READ \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_execução genérica do FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="943be-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-146">\_direitos padrão \_ Execute \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Subscribe</span><span class="sxs-lookup"><span data-stu-id="943be-146">STANDARD\_RIGHTS\_EXECUTE \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_SUBSCRIBE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_gravação genérica \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="943be-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-148">STANDARD \_ Rights \_ Write \| excluir \| FWPM \_ ACTRL \_ Adicionar \| FWPM \_ ACTRL \_ Adicionar \_ link \| FWPM \_ ACTRL \_ começar \_ gravação \_ TXN \| \_ \_ FWPM ACTRL gravação</span><span class="sxs-lookup"><span data-stu-id="943be-148">STANDARD\_RIGHTS\_WRITE \| DELETE \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="943be-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ genérico \_ tudo**</span><span class="sxs-lookup"><span data-stu-id="943be-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM\_GENERIC\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="943be-150">\_direitos padrão \_ necessários \| FWPM \_ ACTRL \_ Add \| FWPM \_ ACTRL \_ Add \_ link \| FWPM \_ ACTRL \_ begin \_ Read \_ TXN FWPM ACTRL \| \_ \_ begin \_ Write TXN FWPM ACTRL \_ \| \_ \_ classificar \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ stats FWPM \| \_ ACTRL \_ Subscribe \| \_ \_ FWPM ACTRL Write</span><span class="sxs-lookup"><span data-stu-id="943be-150">STANDARD\_RIGHTS\_REQUIRED \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS \| FWPM\_ACTRL\_SUBSCRIBE \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="943be-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="943be-151">Requirements</span></span>



| <span data-ttu-id="943be-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="943be-152">Requirement</span></span> | <span data-ttu-id="943be-153">Valor</span><span class="sxs-lookup"><span data-stu-id="943be-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="943be-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="943be-154">Minimum supported client</span></span><br/> | <span data-ttu-id="943be-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="943be-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="943be-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="943be-156">Minimum supported server</span></span><br/> | <span data-ttu-id="943be-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="943be-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="943be-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="943be-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="943be-159"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="943be-159"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943be-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="943be-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943be-161">Modelo de controle de acesso da plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="943be-161">Windows Filtering Platform Access Control Model</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="943be-162">Direitos de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="943be-162">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

