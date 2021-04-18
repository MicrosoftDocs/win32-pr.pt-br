---
title: Transação de XTYP_ADVSTOP (ddeml. h)
description: Um cliente usa a \_ transação XTYP ADVSTOP para encerrar um loop de aviso com um servidor. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), DdeCallback, recebe essa transação quando um cliente especifica XTYP \_ ADVSTOP na função DdeClientTransaction.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- Troca de dados de transação XTYP_ADVSTOP
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105798062"
---
# <a name="xtyp_advstop-transaction"></a><span data-ttu-id="10baf-105">\_Transação XTYP ADVSTOP</span><span class="sxs-lookup"><span data-stu-id="10baf-105">XTYP\_ADVSTOP transaction</span></span>

<span data-ttu-id="10baf-106">Um cliente usa a transação **XTYP \_ ADVSTOP** para encerrar um loop de aviso com um servidor.</span><span class="sxs-lookup"><span data-stu-id="10baf-106">A client uses the **XTYP\_ADVSTOP** transaction to end an advise loop with a server.</span></span> <span data-ttu-id="10baf-107">Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_ ADVSTOP** na função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="10baf-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTOP** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a><span data-ttu-id="10baf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10baf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10baf-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="10baf-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-110">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="10baf-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="10baf-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="10baf-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-112">O formato de dados associado ao loop de aviso que está sendo finalizado.</span><span class="sxs-lookup"><span data-stu-id="10baf-112">The data format associated with the advise loop being ended.</span></span>

</dd> <dt>

<span data-ttu-id="10baf-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="10baf-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-114">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="10baf-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="10baf-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="10baf-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-116">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="10baf-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="10baf-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="10baf-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-118">Um identificador para o nome do item.</span><span class="sxs-lookup"><span data-stu-id="10baf-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="10baf-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="10baf-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="10baf-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="10baf-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="10baf-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="10baf-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="10baf-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="10baf-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="10baf-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="10baf-124">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10baf-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="10baf-125">Remarks</span></span>

<span data-ttu-id="10baf-126">Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF de \_ \_ aviso de falha** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="10baf-126">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10baf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10baf-127">Requirements</span></span>



| <span data-ttu-id="10baf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="10baf-128">Requirement</span></span> | <span data-ttu-id="10baf-129">Valor</span><span class="sxs-lookup"><span data-stu-id="10baf-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10baf-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10baf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="10baf-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10baf-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="10baf-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10baf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="10baf-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10baf-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="10baf-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10baf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="10baf-135"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10baf-135"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10baf-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="10baf-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="10baf-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="10baf-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10baf-138">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="10baf-138">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="10baf-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="10baf-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="10baf-140">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="10baf-140">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="10baf-141">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="10baf-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="10baf-142">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="10baf-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

