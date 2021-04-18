---
title: Transação de XTYP_XACT_COMPLETE (ddeml. h)
description: Uma função de retorno de chamada do cliente troca dinâmica de dados (DDE), DdeCallback, recebe a \_ \_ transação de conclusão de transações XTYP quando uma transação assíncrona, iniciada por uma chamada para a função DdeClientTransaction, foi concluída.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Troca de dados de transação XTYP_XACT_COMPLETE
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779870"
---
# <a name="xtyp_xact_complete-transaction"></a><span data-ttu-id="a12d7-104">Transação do XTYP \_ \_ Transaction concluída</span><span class="sxs-lookup"><span data-stu-id="a12d7-104">XTYP\_XACT\_COMPLETE transaction</span></span>

<span data-ttu-id="a12d7-105">Uma função de retorno de chamada do cliente troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ \_ conclusão** de transações XTYP quando uma transação assíncrona, iniciada por uma chamada para a função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , foi concluída.</span><span class="sxs-lookup"><span data-stu-id="a12d7-105">A Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_XACT\_COMPLETE** transaction when an asynchronous transaction, initiated by a call to the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function, has completed.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a><span data-ttu-id="a12d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a12d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12d7-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="a12d7-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-108">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="a12d7-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="a12d7-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="a12d7-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-110">O formato dos dados associados à transação concluída (se aplicável) ou **NULL** se nenhum dado foi trocado durante a transação.</span><span class="sxs-lookup"><span data-stu-id="a12d7-110">The format of the data associated with the completed transaction (if applicable) or **NULL** if no data was exchanged during the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a12d7-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="a12d7-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-112">Um identificador para a conversa.</span><span class="sxs-lookup"><span data-stu-id="a12d7-112">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="a12d7-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="a12d7-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-114">Um identificador para o nome do tópico envolvido na transação concluída.</span><span class="sxs-lookup"><span data-stu-id="a12d7-114">A handle to the topic name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a12d7-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="a12d7-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-116">Um identificador para o nome do item envolvido na transação concluída.</span><span class="sxs-lookup"><span data-stu-id="a12d7-116">A handle to the item name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a12d7-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="a12d7-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-118">Um identificador para os dados envolvidos na transação concluída, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="a12d7-118">A handle to the data involved in the completed transaction, if applicable.</span></span> <span data-ttu-id="a12d7-119">Se a transação foi bem-sucedida, mas não envolvia nenhum dado, esse parâmetro é **true**.</span><span class="sxs-lookup"><span data-stu-id="a12d7-119">If the transaction was successful but involved no data, this parameter is **TRUE**.</span></span> <span data-ttu-id="a12d7-120">Esse parâmetro será **nulo** se a transação não tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a12d7-120">This parameter is **NULL** if the transaction was unsuccessful.</span></span>

</dd> <dt>

<span data-ttu-id="a12d7-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="a12d7-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-122">O identificador da transação concluída.</span><span class="sxs-lookup"><span data-stu-id="a12d7-122">The transaction identifier of the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a12d7-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="a12d7-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="a12d7-124">Quaisquer sinalizadores de status **DDE \_** aplicáveis na palavra inferior.</span><span class="sxs-lookup"><span data-stu-id="a12d7-124">Any applicable **DDE\_** status flags in the low word.</span></span> <span data-ttu-id="a12d7-125">Esse parâmetro fornece suporte para aplicativos dependentes de bits **\_ APPSTATUS do DDE** .</span><span class="sxs-lookup"><span data-stu-id="a12d7-125">This parameter provides support for applications dependent on **DDE\_APPSTATUS** bits.</span></span> <span data-ttu-id="a12d7-126">É recomendável que os aplicativos não usem mais esses bits, eles podem não ter suporte em versões futuras do DDEML.</span><span class="sxs-lookup"><span data-stu-id="a12d7-126">It is recommended that applications no longer use these bits   they may not be supported in future versions of the DDEML.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a12d7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a12d7-127">Remarks</span></span>

<span data-ttu-id="a12d7-128">Um aplicativo não deve liberar o identificador de dados obtido durante essa transação.</span><span class="sxs-lookup"><span data-stu-id="a12d7-128">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="a12d7-129">No entanto, um aplicativo deve copiar os dados associados ao identificador de dados se o aplicativo precisar processar os dados depois que a função de retorno de chamada retornar.</span><span class="sxs-lookup"><span data-stu-id="a12d7-129">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="a12d7-130">Um aplicativo pode usar a função [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar os dados.</span><span class="sxs-lookup"><span data-stu-id="a12d7-130">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a12d7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a12d7-131">Requirements</span></span>



| <span data-ttu-id="a12d7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a12d7-132">Requirement</span></span> | <span data-ttu-id="a12d7-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a12d7-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12d7-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a12d7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a12d7-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a12d7-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a12d7-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a12d7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a12d7-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a12d7-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a12d7-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a12d7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a12d7-139"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a12d7-139"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a12d7-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a12d7-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="a12d7-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a12d7-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a12d7-142">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="a12d7-142">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="a12d7-143">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="a12d7-143">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

<span data-ttu-id="a12d7-144">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a12d7-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a12d7-145">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a12d7-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

