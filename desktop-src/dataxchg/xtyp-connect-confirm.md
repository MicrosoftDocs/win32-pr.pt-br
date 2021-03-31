---
title: Transação de XTYP_CONNECT_CONFIRM (ddeml. h)
description: Uma função de retorno de chamada do servidor troca dinâmica de dados (DDE), DdeCallback, recebe a transação de confirmação do XTYP \_ Connect \_ para confirmar que uma conversa foi estabelecida com um cliente e para fornecer ao servidor o identificador de conversa.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- Troca de dados de transação XTYP_CONNECT_CONFIRM
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369676"
---
# <a name="xtyp_connect_confirm-transaction"></a><span data-ttu-id="7211d-104">\_ \_ Confirmar transação do XTYP Connect</span><span class="sxs-lookup"><span data-stu-id="7211d-104">XTYP\_CONNECT\_CONFIRM transaction</span></span>

<span data-ttu-id="7211d-105">Uma função de retorno de chamada do servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **confirmação do XTYP \_ Connect \_** para confirmar que uma conversa foi estabelecida com um cliente e para fornecer ao servidor o identificador de conversa.</span><span class="sxs-lookup"><span data-stu-id="7211d-105">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_CONNECT\_CONFIRM** transaction to confirm that a conversation has been established with a client and to provide the server with the conversation handle.</span></span> <span data-ttu-id="7211d-106">O sistema envia essa transação como resultado de uma transação [**XTYP \_ Connect**](xtyp-connect.md) ou [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="7211d-106">The system sends this transaction as a result of a previous [**XTYP\_CONNECT**](xtyp-connect.md) or [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="7211d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7211d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7211d-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="7211d-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-109">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="7211d-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="7211d-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="7211d-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7211d-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7211d-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="7211d-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-113">Um identificador para a nova conversa.</span><span class="sxs-lookup"><span data-stu-id="7211d-113">A handle to the new conversation.</span></span>

</dd> <dt>

<span data-ttu-id="7211d-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="7211d-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-115">Um identificador para o nome do tópico no qual a conversa foi estabelecida.</span><span class="sxs-lookup"><span data-stu-id="7211d-115">A handle to the topic name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="7211d-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="7211d-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-117">Um identificador para o nome do serviço no qual a conversa foi estabelecida.</span><span class="sxs-lookup"><span data-stu-id="7211d-117">A handle to the service name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="7211d-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="7211d-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-119">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7211d-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7211d-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="7211d-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-121">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7211d-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7211d-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="7211d-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="7211d-123">Especifica se o cliente é a mesma instância de aplicativo que o servidor.</span><span class="sxs-lookup"><span data-stu-id="7211d-123">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="7211d-124">Se o parâmetro for 1, o cliente será a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="7211d-124">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="7211d-125">Se o parâmetro for 0, o cliente será uma instância diferente.</span><span class="sxs-lookup"><span data-stu-id="7211d-125">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7211d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7211d-126">Remarks</span></span>

<span data-ttu-id="7211d-127">Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Skip \_ Connect \_ confirmations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="7211d-127">This transaction is filtered if the server application specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="7211d-128">Um servidor não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="7211d-128">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7211d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7211d-129">Requirements</span></span>



| <span data-ttu-id="7211d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7211d-130">Requirement</span></span> | <span data-ttu-id="7211d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7211d-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7211d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7211d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7211d-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7211d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7211d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7211d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7211d-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7211d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7211d-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7211d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7211d-137"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7211d-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7211d-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7211d-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="7211d-139">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7211d-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7211d-140">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="7211d-140">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="7211d-141">**DdeConnectList**</span><span class="sxs-lookup"><span data-stu-id="7211d-141">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[<span data-ttu-id="7211d-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="7211d-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="7211d-143">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7211d-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7211d-144">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7211d-144">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

