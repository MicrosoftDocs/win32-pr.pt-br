---
title: Transação de XTYP_WILDCONNECT (ddeml. h)
description: Permite que um cliente estabeleça uma conversa em cada nome de serviço do servidor e pares de nome de tópico que correspondam ao nome do serviço especificado e ao nome do tópico.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Troca de dados de transação XTYP_WILDCONNECT
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762983"
---
# <a name="xtyp_wildconnect-transaction"></a><span data-ttu-id="8dc54-104">\_Transação XTYP WILDCONNECT</span><span class="sxs-lookup"><span data-stu-id="8dc54-104">XTYP\_WILDCONNECT transaction</span></span>

<span data-ttu-id="8dc54-105">Permite que um cliente estabeleça uma conversa em cada nome de serviço do servidor e pares de nome de tópico que correspondam ao nome do serviço especificado e ao nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="8dc54-105">Enables a client to establish a conversation on each of the server's service name and topic name pairs that match the specified service name and topic name.</span></span> <span data-ttu-id="8dc54-106">Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica um nome de serviço **nulo** , um nome de tópico **nulo** ou ambos em uma chamada para a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) ou [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="8dc54-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a **NULL** service name, a **NULL** topic name, or both in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) or [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="8dc54-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dc54-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc54-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="8dc54-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-109">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="8dc54-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="8dc54-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="8dc54-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8dc54-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8dc54-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="8dc54-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8dc54-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8dc54-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="8dc54-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-115">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="8dc54-115">A handle to the topic name.</span></span> <span data-ttu-id="8dc54-116">Se esse parâmetro for **nulo**, o cliente está solicitando uma conversa em todos os nomes de tópico aos quais o servidor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="8dc54-116">If this parameter is **NULL**, the client is requesting a conversation on all topic names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="8dc54-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="8dc54-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-118">Um identificador para o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="8dc54-118">A handle to the service name.</span></span> <span data-ttu-id="8dc54-119">Se esse parâmetro for **nulo**, o cliente está solicitando uma conversa em todos os nomes de serviço aos quais o servidor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="8dc54-119">If this parameter is **NULL**, the client is requesting a conversation on all service names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="8dc54-120">*hdata*</span><span class="sxs-lookup"><span data-stu-id="8dc54-120">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-121">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8dc54-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8dc54-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="8dc54-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-123">Um ponteiro para uma estrutura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contém informações de contexto para a conversa.</span><span class="sxs-lookup"><span data-stu-id="8dc54-123">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="8dc54-124">Se o cliente não for um aplicativo DDEML, esse parâmetro será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="8dc54-124">If the client is not a DDEML application, this parameter is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8dc54-125">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="8dc54-125">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc54-126">Especifica se o cliente é a mesma instância de aplicativo que o servidor.</span><span class="sxs-lookup"><span data-stu-id="8dc54-126">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="8dc54-127">Se o parâmetro for 1, o cliente será a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="8dc54-127">If the parameter is 1, the client is same instance.</span></span> <span data-ttu-id="8dc54-128">Se o parâmetro for 0, o cliente será uma instância diferente.</span><span class="sxs-lookup"><span data-stu-id="8dc54-128">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc54-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8dc54-129">Return value</span></span>

<span data-ttu-id="8dc54-130">O servidor deve retornar um identificador de dados que identifica uma matriz de estruturas [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="8dc54-130">The server should return a data handle that identifies an array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="8dc54-131">A matriz deve conter uma estrutura para cada par de nome de serviço e nome de tópico que corresponda ao par nome-do-serviço e tópico-nome solicitado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="8dc54-131">The array should contain one structure for each service-name and topic-name pair that matches the service-name and topic-name pair requested by the client.</span></span> <span data-ttu-id="8dc54-132">A matriz deve ser terminada por um identificador de cadeia de caracteres **nula** .</span><span class="sxs-lookup"><span data-stu-id="8dc54-132">The array must be terminated by a **NULL** string handle.</span></span> <span data-ttu-id="8dc54-133">O sistema envia a transação de [**\_ \_ confirmação do XTYP Connect**](xtyp-connect-confirm.md) para o servidor para confirmar cada conversa e passar os identificadores de conversa para o servidor.</span><span class="sxs-lookup"><span data-stu-id="8dc54-133">The system sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server to confirm each conversation and to pass the conversation handles to the server.</span></span> <span data-ttu-id="8dc54-134">O servidor não receberá essas confirmações se tiver especificado o sinalizador **CBF \_ ignorar \_ Connect \_ confirmations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="8dc54-134">The server will not receive these confirmations if it specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="8dc54-135">O servidor deve retornar **NULL** para recusar a transação **XTYP \_ WILDCONNECT** .</span><span class="sxs-lookup"><span data-stu-id="8dc54-135">The server should return **NULL** to refuse the **XTYP\_WILDCONNECT** transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dc54-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dc54-136">Remarks</span></span>

<span data-ttu-id="8dc54-137">Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Fail \_ Connections** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="8dc54-137">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="8dc54-138">Um servidor não pode bloquear esse tipo de transação; o \_ código de retorno de bloco CBR é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8dc54-138">A server cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc54-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dc54-139">Requirements</span></span>



| <span data-ttu-id="8dc54-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dc54-140">Requirement</span></span> | <span data-ttu-id="8dc54-141">Valor</span><span class="sxs-lookup"><span data-stu-id="8dc54-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc54-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dc54-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc54-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8dc54-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8dc54-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dc54-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc54-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8dc54-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8dc54-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8dc54-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc54-147"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8dc54-147"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc54-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dc54-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="8dc54-149">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8dc54-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8dc54-150">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="8dc54-150">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="8dc54-151">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="8dc54-151">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="8dc54-152">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="8dc54-152">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="8dc54-153">**HSZPAIR**</span><span class="sxs-lookup"><span data-stu-id="8dc54-153">**HSZPAIR**</span></span>](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

<span data-ttu-id="8dc54-154">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8dc54-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8dc54-155">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="8dc54-155">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

