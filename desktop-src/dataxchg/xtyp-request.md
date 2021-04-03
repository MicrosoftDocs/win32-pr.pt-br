---
title: Transação de XTYP_REQUEST (ddeml. h)
description: Um cliente usa a \_ transação de solicitação XTYP para solicitar dados de um servidor. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), DdeCallback, recebe essa transação quando um cliente especifica \_ a solicitação XTYP na função DdeClientTransaction.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- Troca de dados de transação XTYP_REQUEST
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644356"
---
# <a name="xtyp_request-transaction"></a><span data-ttu-id="deebf-105">\_Transação de solicitação XTYP</span><span class="sxs-lookup"><span data-stu-id="deebf-105">XTYP\_REQUEST transaction</span></span>

<span data-ttu-id="deebf-106">Um cliente usa a transação de **\_ solicitação XTYP** para solicitar dados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="deebf-106">A client uses the **XTYP\_REQUEST** transaction to request data from a server.</span></span> <span data-ttu-id="deebf-107">Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica a **\_ solicitação XTYP** na função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="deebf-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_REQUEST** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a><span data-ttu-id="deebf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deebf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deebf-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="deebf-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-110">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="deebf-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="deebf-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="deebf-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-112">O formato no qual o servidor deve enviar dados para o cliente.</span><span class="sxs-lookup"><span data-stu-id="deebf-112">The format in which the server should submit data to the client.</span></span>

</dd> <dt>

<span data-ttu-id="deebf-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="deebf-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-114">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="deebf-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="deebf-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="deebf-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-116">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="deebf-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="deebf-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="deebf-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-118">Um identificador para o nome do item.</span><span class="sxs-lookup"><span data-stu-id="deebf-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="deebf-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="deebf-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="deebf-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="deebf-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="deebf-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="deebf-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="deebf-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="deebf-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="deebf-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="deebf-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deebf-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="deebf-125">Return value</span></span>

<span data-ttu-id="deebf-126">O servidor deve chamar a função [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para criar um identificador de dados que identifica os dados e, em seguida, retornar o identificador.</span><span class="sxs-lookup"><span data-stu-id="deebf-126">The server should call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the data and then return the handle.</span></span> <span data-ttu-id="deebf-127">O servidor deverá retornar **NULL** se não for possível concluir a transação.</span><span class="sxs-lookup"><span data-stu-id="deebf-127">The server should return **NULL** if it is unable to complete the transaction.</span></span> <span data-ttu-id="deebf-128">Se o servidor retornar **NULL**, o cliente receberá um \_ sinalizador FNOTPROCESSED do DDE.</span><span class="sxs-lookup"><span data-stu-id="deebf-128">If the server returns **NULL**, the client will receive a DDE\_FNOTPROCESSED flag.</span></span>

## <a name="remarks"></a><span data-ttu-id="deebf-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="deebf-129">Remarks</span></span>

<span data-ttu-id="deebf-130">Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Fail \_ requests** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="deebf-130">This transaction is filtered if the server application specified the **CBF\_FAIL\_REQUESTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="deebf-131">Se responder a essa transação exigir processamento longo, o servidor poderá retornar o código de \_ retorno do bloco CBR para suspender transações futuras na conversa atual e, em seguida, processar a transação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="deebf-131">If responding to this transaction requires lengthy processing, the server can return the CBR\_BLOCK return code to suspend future transactions on the current conversation and then process the transaction asynchronously.</span></span> <span data-ttu-id="deebf-132">Quando o servidor for concluído e os dados estiverem prontos para passar para o cliente, o servidor poderá chamar a função [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) para retomar a conversa.</span><span class="sxs-lookup"><span data-stu-id="deebf-132">When the server has finished and the data is ready to pass to the client, the server can call the [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) function to resume the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="deebf-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deebf-133">Requirements</span></span>



| <span data-ttu-id="deebf-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="deebf-134">Requirement</span></span> | <span data-ttu-id="deebf-135">Valor</span><span class="sxs-lookup"><span data-stu-id="deebf-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deebf-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="deebf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="deebf-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="deebf-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="deebf-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="deebf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="deebf-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="deebf-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="deebf-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="deebf-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="deebf-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="deebf-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deebf-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="deebf-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="deebf-143">**Referência**</span><span class="sxs-lookup"><span data-stu-id="deebf-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="deebf-144">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="deebf-144">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="deebf-145">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="deebf-145">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="deebf-146">**DdeEnableCallback**</span><span class="sxs-lookup"><span data-stu-id="deebf-146">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[<span data-ttu-id="deebf-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="deebf-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="deebf-148">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="deebf-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="deebf-149">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="deebf-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

