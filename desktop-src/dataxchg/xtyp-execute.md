---
title: Transação de XTYP_EXECUTE (ddeml. h)
description: Um cliente usa a \_ transação XTYP execute para enviar uma cadeia de caracteres de comando para o servidor. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), DdeCallback, recebe essa transação quando um cliente especifica XTYP \_ Execute na função DdeClientTransaction.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- Troca de dados de transação XTYP_EXECUTE
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009623"
---
# <a name="xtyp_execute-transaction"></a><span data-ttu-id="198e1-105">\_Executar transação XTYP</span><span class="sxs-lookup"><span data-stu-id="198e1-105">XTYP\_EXECUTE transaction</span></span>

<span data-ttu-id="198e1-106">Um cliente usa a transação **XTYP \_ Execute** para enviar uma cadeia de caracteres de comando para o servidor.</span><span class="sxs-lookup"><span data-stu-id="198e1-106">A client uses the **XTYP\_EXECUTE** transaction to send a command string to the server.</span></span> <span data-ttu-id="198e1-107">Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_ Execute** na função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="198e1-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_EXECUTE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="198e1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="198e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198e1-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="198e1-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-110">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="198e1-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="198e1-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="198e1-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="198e1-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="198e1-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="198e1-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-114">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="198e1-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="198e1-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="198e1-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-116">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="198e1-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="198e1-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="198e1-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="198e1-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="198e1-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="198e1-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-120">Um identificador para a cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="198e1-120">A handle to the command string.</span></span>

</dd> <dt>

<span data-ttu-id="198e1-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="198e1-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="198e1-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="198e1-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="198e1-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="198e1-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="198e1-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198e1-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="198e1-125">Return value</span></span>

<span data-ttu-id="198e1-126">Uma função de retorno de chamada de servidor deve retornar **\_ FACK DDE** se ele processar essa transação, o **DDE \_ FBUSY** se estiver muito ocupado para processar essa transação ou o **DDE \_ FNOTPROCESSED** se rejeitar essa transação.</span><span class="sxs-lookup"><span data-stu-id="198e1-126">A server callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="198e1-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="198e1-127">Remarks</span></span>

<span data-ttu-id="198e1-128">Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Fail \_ Execute** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="198e1-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_EXECUTES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="198e1-129">Um aplicativo deve liberar o identificador de dados obtido durante essa transação.</span><span class="sxs-lookup"><span data-stu-id="198e1-129">An application must free the data handle obtained during this transaction.</span></span> <span data-ttu-id="198e1-130">No entanto, um aplicativo deve copiar a cadeia de caracteres de comando associada ao identificador de dados se o aplicativo precisar processar a cadeia de caracteres depois que a função de retorno de chamada retornar.</span><span class="sxs-lookup"><span data-stu-id="198e1-130">An application must, however, copy the command string associated with the data handle if the application must process the string after the callback function returns.</span></span> <span data-ttu-id="198e1-131">Um aplicativo pode usar a função [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar os dados.</span><span class="sxs-lookup"><span data-stu-id="198e1-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

<span data-ttu-id="198e1-132">Como a maioria dos aplicativos cliente espera que um aplicativo de servidor execute uma transação **XTYP \_ Execute** de forma síncrona, um servidor deve tentar executar todo o processamento da transação **XTYP \_ Execute** de dentro da função de retorno de chamada DDE ou retornando o código de retorno de **\_ bloco CBR** .</span><span class="sxs-lookup"><span data-stu-id="198e1-132">Because most client applications expect a server application to perform an **XTYP\_EXECUTE** transaction synchronously, a server should attempt to perform all processing of the **XTYP\_EXECUTE** transaction either from within the DDE callback function or by returning the **CBR\_BLOCK** return code.</span></span> <span data-ttu-id="198e1-133">Se o parâmetro *hData* for um comando que instrui o servidor a terminar, o servidor deverá fazer isso depois de processar a transação de **\_ execução XTYP** .</span><span class="sxs-lookup"><span data-stu-id="198e1-133">If the *hdata* parameter is a command that instructs the server to terminate, the server should do so after processing the **XTYP\_EXECUTE** transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="198e1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="198e1-134">Requirements</span></span>



| <span data-ttu-id="198e1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="198e1-135">Requirement</span></span> | <span data-ttu-id="198e1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="198e1-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="198e1-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="198e1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="198e1-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="198e1-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="198e1-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="198e1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="198e1-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="198e1-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="198e1-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="198e1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="198e1-142"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="198e1-142"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="198e1-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="198e1-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="198e1-144">**Referência**</span><span class="sxs-lookup"><span data-stu-id="198e1-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="198e1-145">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="198e1-145">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="198e1-146">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="198e1-146">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="198e1-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="198e1-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="198e1-148">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="198e1-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="198e1-149">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="198e1-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

