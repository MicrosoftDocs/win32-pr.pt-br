---
description: Mescla dois tíquetes de impressão e retorna um tíquete de impressão válido e viável.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: Função MergeAndValidatePrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759684"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a><span data-ttu-id="cd1f1-103">Função MergeAndValidatePrintTicketThunk2</span><span class="sxs-lookup"><span data-stu-id="cd1f1-103">MergeAndValidatePrintTicketThunk2 function</span></span>

<span data-ttu-id="cd1f1-104">\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="cd1f1-105">O [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) fornece funcionalidade equivalente e deve ser usado em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="cd1f1-106">Mescla dois tíquetes de impressão e retorna um tíquete de impressão válido e viável.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-106">Merges two print tickets and returns a valid, viable print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd1f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd1f1-107">Syntax</span></span>


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="cd1f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd1f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd1f1-109">*hProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-110">Um identificador para um provedor de tíquete de impressão aberto.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="cd1f1-111">Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1f1-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-112">*pBasePrintTicket* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-112">*pBasePrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-113">O buffer que contém os dados de tíquete de impressão base, expressos em XML, conforme descrito no [esquema de impressão](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="cd1f1-113">The buffer that contains the base print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-114">*basePrintTicketLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-114">*basePrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-115">O tamanho, em bytes, do buffer referenciado por *pBasePrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-115">The size, in bytes, of the buffer referenced by *pBasePrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-116">*pDeltaPrintTicket* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-116">*pDeltaPrintTicket* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-117">O buffer que contém o tíquete de impressão a ser mesclado.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-117">The buffer that contains the print ticket to merge.</span></span> <span data-ttu-id="cd1f1-118">Os dados de tíquete de impressão são expressos em XML, conforme descrito no [esquema de impressão](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="cd1f1-118">The print ticket data is expressed in XML as described in the [Print Schema](./printschema.md).</span></span> <span data-ttu-id="cd1f1-119">O valor desse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-119">The value of this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-120">*deltaPrintTicketLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-120">*deltaPrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-121">O tamanho, em bytes, do buffer referenciado por *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-121">The size, in bytes, of the buffer referenced by *pDeltaPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-122">*escopo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-122">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-123">O valor que especifica se o escopo de *pDeltaPrintTicket* e *ppValidatedPrintTicket* é uma página única, um documento inteiro ou todos os documentos no trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-123">The value that specifies whether the scope of *pDeltaPrintTicket* and *ppValidatedPrintTicket* is a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="cd1f1-124">O valor desse parâmetro deve ser um membro da enumeração [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , Cast como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-124">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-125">*ppValidatedPrintTicket* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-125">*ppValidatedPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-126">O endereço do buffer que contém o tíquete de impressão mesclado e validado.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-126">The address of the buffer that contains the merged and validated print ticket.</span></span> <span data-ttu-id="cd1f1-127">Essa função chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar esse buffer.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-127">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="cd1f1-128">Quando o buffer não for mais necessário, o chamador deverá liberá-lo chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="cd1f1-128">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-129">*pValidatedPrintTicketLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-129">*pValidatedPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-130">O tamanho, em bytes, do buffer referenciado por *ppValidatedPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-130">The size, in bytes, of the buffer referenced by *ppValidatedPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f1-131">*pbstrErrorMessage* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-131">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd1f1-132">Um ponteiro para uma cadeia de caracteres que especifica o que, se for algo, é inválido sobre o tíquete de impressão em *pBasePrintTicket* ou *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-132">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pBasePrintTicket* or *pDeltaPrintTicket*.</span></span> <span data-ttu-id="cd1f1-133">Se forem válidos, esse valor será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd1f1-133">If they are both valid, this value is **NULL**.</span></span> <span data-ttu-id="cd1f1-134">Se *pbstrErrorMessage* não for **nulo** quando a função retornar, o chamador deverá liberar a cadeia de caracteres com [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="cd1f1-134">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd1f1-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd1f1-135">Return value</span></span>

<span data-ttu-id="cd1f1-136">Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd1f1-136">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="cd1f1-137">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="cd1f1-137">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd1f1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd1f1-138">Requirements</span></span>



| <span data-ttu-id="cd1f1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd1f1-139">Requirement</span></span> | <span data-ttu-id="cd1f1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="cd1f1-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1f1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd1f1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cd1f1-142">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-142">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cd1f1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd1f1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cd1f1-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd1f1-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cd1f1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cd1f1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd1f1-146"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd1f1-146"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd1f1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd1f1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd1f1-148">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="cd1f1-148">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="cd1f1-149">**PTMergeAndValidatePrintTicket**</span><span class="sxs-lookup"><span data-stu-id="cd1f1-149">**PTMergeAndValidatePrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[<span data-ttu-id="cd1f1-150">Impressão</span><span class="sxs-lookup"><span data-stu-id="cd1f1-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cd1f1-151">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="cd1f1-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

