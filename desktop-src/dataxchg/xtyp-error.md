---
title: Transação de XTYP_ERROR (ddeml. h)
description: Uma função de retorno de chamada troca dinâmica de dados (DDE), DdeCallback, recebe a \_ transação de erro XTYP quando ocorre um erro crítico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Troca de dados de transação XTYP_ERROR
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105791496"
---
# <a name="xtyp_error-transaction"></a><span data-ttu-id="c1995-104">\_Transação de erro XTYP</span><span class="sxs-lookup"><span data-stu-id="c1995-104">XTYP\_ERROR transaction</span></span>

<span data-ttu-id="c1995-105">Uma função de retorno de chamada troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ erro XTYP** quando ocorre um erro crítico.</span><span class="sxs-lookup"><span data-stu-id="c1995-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_ERROR** transaction when a critical error occurs.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="c1995-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1995-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1995-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="c1995-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-108">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="c1995-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="c1995-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c1995-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="c1995-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-112">Um identificador para a conversa associada ao erro.</span><span class="sxs-lookup"><span data-stu-id="c1995-112">A handle to the conversation associated with the error.</span></span> <span data-ttu-id="c1995-113">Esse parâmetro será **nulo** se o erro não estiver associado a uma conversa.</span><span class="sxs-lookup"><span data-stu-id="c1995-113">This parameter is **NULL** if the error is not associated with a conversation.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c1995-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-115">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c1995-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c1995-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c1995-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="c1995-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-119">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c1995-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1995-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c1995-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-121">O código de erro na palavra de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="c1995-121">The error code in the low-order word.</span></span> <span data-ttu-id="c1995-122">Atualmente, há suporte apenas para o código de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1995-122">Currently, only the following error code is supported.</span></span>



| <span data-ttu-id="c1995-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c1995-123">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="c1995-124">Significado</span><span class="sxs-lookup"><span data-stu-id="c1995-124">Meaning</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <span data-ttu-id="c1995-125"><dt>**\_memória insuficiente do DMLERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1995-125"><dt>**DMLERR\_LOW\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1995-126">A memória é baixa; aconselhar, examinar ou executar dados podem ser perdidos ou o sistema pode falhar.</span><span class="sxs-lookup"><span data-stu-id="c1995-126">Memory is low; advise, poke, or execute data may be lost, or the system may fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c1995-127">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c1995-127">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c1995-128">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c1995-128">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1995-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1995-129">Remarks</span></span>

<span data-ttu-id="c1995-130">Um aplicativo não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1995-130">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span> <span data-ttu-id="c1995-131">A biblioteca de gerenciamento de troca dinâmica de dados (DDEML) tenta liberar memória removendo recursos não críticos.</span><span class="sxs-lookup"><span data-stu-id="c1995-131">The Dynamic Data Exchange Management Library (DDEML) attempts to free memory by removing noncritical resources.</span></span> <span data-ttu-id="c1995-132">Um aplicativo que tenha conversas bloqueadas deve desbloqueá-las.</span><span class="sxs-lookup"><span data-stu-id="c1995-132">An application that has blocked conversations should unblock them.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1995-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1995-133">Requirements</span></span>



| <span data-ttu-id="c1995-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1995-134">Requirement</span></span> | <span data-ttu-id="c1995-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c1995-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1995-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1995-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c1995-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1995-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1995-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1995-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c1995-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1995-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c1995-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c1995-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1995-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1995-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1995-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1995-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1995-143">Visão geral da biblioteca de gerenciamento de troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="c1995-143">Dynamic Data Exchange Management Library Overview</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

