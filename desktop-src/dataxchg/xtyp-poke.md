---
title: Transação de XTYP_POKE (ddeml. h)
description: Um cliente usa a transação XTYP de \_ envio para enviar dados não solicitados ao servidor. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), DdeCallback, recebe essa transação quando um cliente especifica XTYP para \_ a função DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Troca de dados de transação XTYP_POKE
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918360"
---
# <a name="xtyp_poke-transaction"></a><span data-ttu-id="6ff01-105">Transação de XTYP \_</span><span class="sxs-lookup"><span data-stu-id="6ff01-105">XTYP\_POKE transaction</span></span>

<span data-ttu-id="6ff01-106">Um cliente usa a **transação \_ XTYP** de envio para enviar dados não solicitados ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6ff01-106">A client uses the **XTYP\_POKE** transaction to send unsolicited data to the server.</span></span> <span data-ttu-id="6ff01-107">Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_** para a função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="6ff01-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_POKE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="6ff01-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ff01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff01-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="6ff01-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-110">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="6ff01-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="6ff01-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="6ff01-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-112">O formato dos dados enviados do servidor.</span><span class="sxs-lookup"><span data-stu-id="6ff01-112">The format of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="6ff01-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="6ff01-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-114">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="6ff01-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="6ff01-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="6ff01-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-116">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="6ff01-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="6ff01-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="6ff01-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-118">Um identificador para o nome do item.</span><span class="sxs-lookup"><span data-stu-id="6ff01-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="6ff01-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="6ff01-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-120">Um identificador para os dados que o cliente está enviando para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6ff01-120">A handle to the data that the client is sending to the server.</span></span>

</dd> <dt>

<span data-ttu-id="6ff01-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="6ff01-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6ff01-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6ff01-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="6ff01-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff01-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6ff01-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff01-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ff01-125">Return value</span></span>

<span data-ttu-id="6ff01-126">Uma função de retorno de chamada de servidor deve retornar o sinalizador **\_ FACK do DDE** se ele processar essa transação, o sinalizador **DDE \_ FBUSY** se estiver muito ocupado para processar essa transação ou o sinalizador **DDE \_ FNOTPROCESSED** se rejeitar essa transação.</span><span class="sxs-lookup"><span data-stu-id="6ff01-126">A server callback function should return the **DDE\_FACK** flag if it processes this transaction, the **DDE\_FBUSY** flag if it is too busy to process this transaction, or the **DDE\_FNOTPROCESSED** flag if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff01-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ff01-127">Remarks</span></span>

<span data-ttu-id="6ff01-128">Essa transação é filtrada se o aplicativo de servidor especificou o sinalizador **CBF \_ \_ Fail reprovations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="6ff01-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_POKES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff01-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ff01-129">Requirements</span></span>



| <span data-ttu-id="6ff01-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ff01-130">Requirement</span></span> | <span data-ttu-id="6ff01-131">Valor</span><span class="sxs-lookup"><span data-stu-id="6ff01-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff01-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ff01-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff01-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ff01-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ff01-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ff01-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff01-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ff01-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="6ff01-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ff01-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ff01-137"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff01-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff01-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ff01-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ff01-139">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6ff01-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6ff01-140">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="6ff01-140">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="6ff01-141">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="6ff01-141">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="6ff01-142">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6ff01-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6ff01-143">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6ff01-143">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

