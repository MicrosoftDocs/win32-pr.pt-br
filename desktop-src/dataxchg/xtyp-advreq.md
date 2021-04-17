---
title: Transação de XTYP_ADVREQ (ddeml. h)
description: A \_ transação XTYP ADVREQ informa ao servidor que uma transação de aviso está pendente no nome do tópico e no par do nome do item especificados e que os dados correspondentes ao nome do tópico e ao par do nome do item foram alterados.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- Troca de dados de transação XTYP_ADVREQ
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369678"
---
# <a name="xtyp_advreq-transaction"></a><span data-ttu-id="da4c3-104">\_Transação XTYP ADVREQ</span><span class="sxs-lookup"><span data-stu-id="da4c3-104">XTYP\_ADVREQ transaction</span></span>

<span data-ttu-id="da4c3-105">A transação **XTYP \_ ADVREQ** informa ao servidor que uma transação de aviso está pendente no nome do tópico e no par do nome do item especificados e que os dados correspondentes ao nome do tópico e ao par do nome do item foram alterados.</span><span class="sxs-lookup"><span data-stu-id="da4c3-105">The **XTYP\_ADVREQ** transaction informs the server that an advise transaction is outstanding on the specified topic name and item name pair and that data corresponding to the topic name and item name pair has changed.</span></span> <span data-ttu-id="da4c3-106">O sistema envia essa transação para a função de retorno de chamada troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), depois que o servidor chama a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="da4c3-106">The system sends this transaction to the Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), after the server calls the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="da4c3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da4c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4c3-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="da4c3-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-109">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="da4c3-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="da4c3-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="da4c3-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-111">O formato no qual os dados devem ser enviados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="da4c3-111">The format in which the data should be submitted to the client.</span></span>

</dd> <dt>

<span data-ttu-id="da4c3-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="da4c3-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-113">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="da4c3-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="da4c3-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="da4c3-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-115">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="da4c3-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="da4c3-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="da4c3-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-117">Um identificador para o nome do item que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="da4c3-117">A handle to the item name that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="da4c3-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="da4c3-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-119">Não usado.</span><span class="sxs-lookup"><span data-stu-id="da4c3-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="da4c3-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="da4c3-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-121">A contagem, na palavra de ordem inferior, das transações **XTYP \_ ADVREQ** que permanecem para ser processada no mesmo tópico, item e nome de formato definido no contexto da chamada atual para a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="da4c3-121">The count, in the low-order word, of **XTYP\_ADVREQ** transactions that remain to be processed on the same topic, item, and format name set within the context of the current call to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span> <span data-ttu-id="da4c3-122">A contagem será zero se a transação **XTYP \_ ADVREQ** atual for a última.</span><span class="sxs-lookup"><span data-stu-id="da4c3-122">The count is zero if the current **XTYP\_ADVREQ** transaction is the last one.</span></span> <span data-ttu-id="da4c3-123">Um servidor pode usar essa contagem para determinar se deve criar um identificador de dados **HDATA \_ APPOWNED** para os dados de aviso.</span><span class="sxs-lookup"><span data-stu-id="da4c3-123">A server can use this count to determine whether to create an **HDATA\_APPOWNED** data handle to the advise data.</span></span>

<span data-ttu-id="da4c3-124">A palavra de ordem inferior é definida como **CADV \_ LATEACK** se o ddeml emitiu a transação **\_ ADVREQ do XTYP** devido a uma mensagem de ACK DDE de chegada \_ de um cliente que está sendo OutRun pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="da4c3-124">The low-order word is set to **CADV\_LATEACK** if the DDEML issued the **XTYP\_ADVREQ** transaction because of a late-arriving DDE\_ACK message from a client being outrun by the server.</span></span>

<span data-ttu-id="da4c3-125">A palavra de ordem superior não é usada.</span><span class="sxs-lookup"><span data-stu-id="da4c3-125">The high-order word is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da4c3-126">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="da4c3-126">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="da4c3-127">Não usado.</span><span class="sxs-lookup"><span data-stu-id="da4c3-127">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4c3-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da4c3-128">Return value</span></span>

<span data-ttu-id="da4c3-129">O servidor deve primeiro chamar a função [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para criar um identificador de dados que identifica os dados alterados e, em seguida, retornar o identificador.</span><span class="sxs-lookup"><span data-stu-id="da4c3-129">The server should first call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the changed data and then return the handle.</span></span> <span data-ttu-id="da4c3-130">O servidor deverá retornar **NULL** se não for possível concluir a transação.</span><span class="sxs-lookup"><span data-stu-id="da4c3-130">The server should return **NULL** if it is unable to complete the transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="da4c3-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="da4c3-131">Remarks</span></span>

<span data-ttu-id="da4c3-132">Um servidor não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="da4c3-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4c3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da4c3-133">Requirements</span></span>



| <span data-ttu-id="da4c3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="da4c3-134">Requirement</span></span> | <span data-ttu-id="da4c3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="da4c3-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4c3-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da4c3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="da4c3-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da4c3-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="da4c3-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da4c3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="da4c3-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da4c3-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="da4c3-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="da4c3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="da4c3-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da4c3-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4c3-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="da4c3-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="da4c3-143">**Referência**</span><span class="sxs-lookup"><span data-stu-id="da4c3-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da4c3-144">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="da4c3-144">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="da4c3-145">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="da4c3-145">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="da4c3-146">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="da4c3-146">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="da4c3-147">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="da4c3-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="da4c3-148">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="da4c3-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

