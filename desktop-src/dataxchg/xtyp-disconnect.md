---
title: Transação de XTYP_DISCONNECT (ddeml. h)
description: A função de retorno de chamada de troca dinâmica de dados (DDE) de um aplicativo, DdeCallback, recebe a \_ transação de desconexão de XTYP quando o parceiro do aplicativo em uma conversa usa a função DdeDisconnect para encerrar a conversa.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Troca de dados de transação XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644357"
---
# <a name="xtyp_disconnect-transaction"></a><span data-ttu-id="2f0ca-104">\_Transação de desconexão de XTYP</span><span class="sxs-lookup"><span data-stu-id="2f0ca-104">XTYP\_DISCONNECT transaction</span></span>

<span data-ttu-id="2f0ca-105">A função de retorno de chamada de troca dinâmica de dados (DDE) de um aplicativo, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ desconexão de XTYP** quando o parceiro do aplicativo em uma conversa usa a função [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) para encerrar a conversa.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-105">An application's Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_DISCONNECT** transaction when the application's partner in a conversation uses the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function to terminate the conversation.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="2f0ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f0ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f0ca-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-108">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="2f0ca-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f0ca-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-112">Um identificador para que a conversa foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-112">A handle to that the conversation was terminated.</span></span>

</dd> <dt>

<span data-ttu-id="2f0ca-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-114">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-114">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f0ca-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f0ca-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f0ca-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f0ca-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="2f0ca-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0ca-122">Especifica se os parceiros na conversa são a mesma instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-122">Specifies whether the partners in the conversation are the same application instance.</span></span> <span data-ttu-id="2f0ca-123">Se esse parâmetro for 1, os parceiros serão a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-123">If this parameter is 1, the partners are the same instance.</span></span> <span data-ttu-id="2f0ca-124">Se esse parâmetro for 0, os parceiros serão instâncias diferentes.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-124">If this parameter is 0, the partners are different instances.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f0ca-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f0ca-125">Remarks</span></span>

<span data-ttu-id="2f0ca-126">Essa transação será filtrada se o aplicativo tiver especificado o sinalizador **CBF \_ ignorar \_ desconexões** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="2f0ca-126">This transaction is filtered if the application specified the **CBF\_SKIP\_DISCONNECTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="2f0ca-127">O aplicativo pode obter o status da conversa encerrada chamando a função [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante o processamento dessa transação.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-127">The application can obtain the status of the terminated conversation by calling the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function while processing this transaction.</span></span> <span data-ttu-id="2f0ca-128">O identificador de conversa se torna inválido depois que a função de retorno de chamada retorna.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-128">The conversation handle becomes invalid after the callback function returns.</span></span>

<span data-ttu-id="2f0ca-129">Um aplicativo não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="2f0ca-129">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f0ca-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f0ca-130">Requirements</span></span>



| <span data-ttu-id="2f0ca-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f0ca-131">Requirement</span></span> | <span data-ttu-id="2f0ca-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2f0ca-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0ca-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f0ca-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2f0ca-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f0ca-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f0ca-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f0ca-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2f0ca-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f0ca-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="2f0ca-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2f0ca-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f0ca-138"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f0ca-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f0ca-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f0ca-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f0ca-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2f0ca-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f0ca-141">**DdeDisconnect**</span><span class="sxs-lookup"><span data-stu-id="2f0ca-141">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[<span data-ttu-id="2f0ca-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="2f0ca-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="2f0ca-143">**DdeQueryConvInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0ca-143">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

<span data-ttu-id="2f0ca-144">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2f0ca-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f0ca-145">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2f0ca-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

