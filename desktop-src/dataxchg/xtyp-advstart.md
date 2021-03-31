---
title: Transação de XTYP_ADVSTART (ddeml. h)
description: Um cliente usa a \_ transação XTYP ADVSTART para estabelecer um loop de aviso com um servidor.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- Troca de dados de transação XTYP_ADVSTART
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644739"
---
# <a name="xtyp_advstart-transaction"></a><span data-ttu-id="7d055-104">\_Transação XTYP ADVSTART</span><span class="sxs-lookup"><span data-stu-id="7d055-104">XTYP\_ADVSTART transaction</span></span>

<span data-ttu-id="7d055-105">Um cliente usa a transação **XTYP \_ ADVSTART** para estabelecer um loop de aviso com um servidor.</span><span class="sxs-lookup"><span data-stu-id="7d055-105">A client uses the **XTYP\_ADVSTART** transaction to establish an advise loop with a server.</span></span> <span data-ttu-id="7d055-106">Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_ ADVSTART** como o parâmetro *wType* da função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="7d055-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTART** as the *wType* parameter of the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a><span data-ttu-id="7d055-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d055-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d055-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="7d055-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-109">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="7d055-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="7d055-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="7d055-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-111">O formato de dados solicitado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="7d055-111">The data format requested by the client.</span></span>

</dd> <dt>

<span data-ttu-id="7d055-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="7d055-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-113">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="7d055-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="7d055-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="7d055-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-115">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="7d055-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="7d055-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="7d055-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-117">Um identificador para o nome do item.</span><span class="sxs-lookup"><span data-stu-id="7d055-117">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="7d055-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="7d055-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-119">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7d055-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d055-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="7d055-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-121">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7d055-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d055-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="7d055-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d055-123">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7d055-123">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d055-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d055-124">Return value</span></span>

<span data-ttu-id="7d055-125">Uma função de retorno de chamada de servidor deve retornar **true** para permitir um loop de aviso no nome do tópico e no par do nome do item especificados, ou **false** para negar o loop de aviso.</span><span class="sxs-lookup"><span data-stu-id="7d055-125">A server callback function should return **TRUE** to allow an advise loop on the specified topic name and item name pair, or **FALSE** to deny the advise loop.</span></span> <span data-ttu-id="7d055-126">Se a função de retorno de chamada retornar **true**, todas as chamadas subsequentes para a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) pelo servidor no mesmo nome de tópico e par de nome de item fazem com que o sistema envie transações [**XTYP \_ ADVREQ**](xtyp-advreq.md) para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7d055-126">If the callback function returns **TRUE**, any subsequent calls to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function by the server on the same topic name and item name pair causes the system to send [**XTYP\_ADVREQ**](xtyp-advreq.md) transactions to the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d055-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d055-127">Remarks</span></span>

<span data-ttu-id="7d055-128">Se um cliente solicitar um loop de aviso em um nome de tópico, nome de item e formato de dados para um loop de aviso que já esteja estabelecido, a troca dinâmica de dados biblioteca de gerenciamento (DDEML) não criará um loop de aviso duplicado, mas, em vez disso, alterará os sinalizadores de loop de aviso (**XTYPF \_ ACKREQ** e **XTYPF \_ NODATA**) para corresponder à solicitação mais recente.</span><span class="sxs-lookup"><span data-stu-id="7d055-128">If a client requests an advise loop on a topic name, item name, and data format for an advise loop that is already established, the Dynamic Data Exchange Management Library (DDEML) does not create a duplicate advise loop but instead alters the advise loop flags (**XTYPF\_ACKREQ** and **XTYPF\_NODATA**) to match the latest request.</span></span>

<span data-ttu-id="7d055-129">Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF de \_ \_ aviso de falha** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="7d055-129">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d055-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d055-130">Requirements</span></span>



| <span data-ttu-id="7d055-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d055-131">Requirement</span></span> | <span data-ttu-id="7d055-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7d055-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d055-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d055-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7d055-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d055-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7d055-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d055-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7d055-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d055-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7d055-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7d055-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d055-138"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d055-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d055-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7d055-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d055-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7d055-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7d055-141">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="7d055-141">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="7d055-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="7d055-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="7d055-143">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="7d055-143">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="7d055-144">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7d055-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7d055-145">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7d055-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

