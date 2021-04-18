---
title: Transação de XTYP_ADVDATA (ddeml. h)
description: Informa ao cliente que o valor do item de dados foi alterado. A função de retorno de chamada do cliente troca dinâmica de dados (DDE), DdeCallback, recebe essa transação depois de estabelecer um loop de aviso com um servidor.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- Troca de dados de transação XTYP_ADVDATA
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796286"
---
# <a name="xtyp_advdata-transaction"></a><span data-ttu-id="ed9f5-105">\_Transação XTYP ADVDATA</span><span class="sxs-lookup"><span data-stu-id="ed9f5-105">XTYP\_ADVDATA transaction</span></span>

<span data-ttu-id="ed9f5-106">Informa ao cliente que o valor do item de dados foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-106">Informs the client that the value of the data item has changed.</span></span> <span data-ttu-id="ed9f5-107">A função de retorno de chamada do cliente troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação depois de estabelecer um loop de aviso com um servidor.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-107">The Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction after establishing an advise loop with a server.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="ed9f5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed9f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed9f5-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-110">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="ed9f5-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-112">O formato Atom dos dados enviados do servidor.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-112">The format atom of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="ed9f5-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-114">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="ed9f5-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-116">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="ed9f5-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-118">Um identificador para o nome do item.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="ed9f5-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-120">Um identificador para os dados associados ao nome do tópico e ao par do nome do item.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-120">A handle to the data associated with the topic name and item name pair.</span></span> <span data-ttu-id="ed9f5-121">Esse parâmetro será **nulo** se o cliente tiver especificado o sinalizador **\_ NODATA do XTYPF** quando solicitou o loop de aviso.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-121">This parameter is **NULL** if the client specified the **XTYPF\_NODATA** flag when it requested the advise loop.</span></span>

</dd> <dt>

<span data-ttu-id="ed9f5-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-123">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-123">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ed9f5-124">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="ed9f5-124">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="ed9f5-125">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-125">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed9f5-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed9f5-126">Return value</span></span>

<span data-ttu-id="ed9f5-127">Uma função de retorno de chamada DDE deve retornar **\_ FACK DDE** se ele processar essa transação, o **DDE \_ FBUSY** se estiver muito ocupado para processar essa transação ou o **DDE \_ FNOTPROCESSED** se rejeitar essa transação.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-127">A DDE callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed9f5-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed9f5-128">Remarks</span></span>

<span data-ttu-id="ed9f5-129">Um aplicativo não deve liberar o identificador de dados obtido durante essa transação.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-129">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="ed9f5-130">No entanto, um aplicativo deve copiar os dados associados ao identificador de dados se o aplicativo precisar processar os dados depois que a função de retorno de chamada retornar.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-130">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="ed9f5-131">Um aplicativo pode usar a função [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar os dados.</span><span class="sxs-lookup"><span data-stu-id="ed9f5-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed9f5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed9f5-132">Requirements</span></span>



| <span data-ttu-id="ed9f5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed9f5-133">Requirement</span></span> | <span data-ttu-id="ed9f5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ed9f5-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9f5-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed9f5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ed9f5-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed9f5-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ed9f5-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed9f5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ed9f5-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed9f5-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ed9f5-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed9f5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed9f5-140"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed9f5-140"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed9f5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed9f5-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed9f5-142">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ed9f5-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed9f5-143">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="ed9f5-143">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="ed9f5-144">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="ed9f5-144">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="ed9f5-145">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="ed9f5-145">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="ed9f5-146">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ed9f5-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ed9f5-147">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ed9f5-147">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

