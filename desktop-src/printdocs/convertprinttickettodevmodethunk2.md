---
description: Converte um tíquete de impressão em uma estrutura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: Função ConvertPrintTicketToDevModeThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011395"
---
# <a name="convertprinttickettodevmodethunk2-function"></a><span data-ttu-id="f440b-103">Função ConvertPrintTicketToDevModeThunk2</span><span class="sxs-lookup"><span data-stu-id="f440b-103">ConvertPrintTicketToDevModeThunk2 function</span></span>

<span data-ttu-id="f440b-104">\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="f440b-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="f440b-105">O [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) fornece funcionalidade equivalente e deve ser usado em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="f440b-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="f440b-106">Converte um tíquete de impressão em uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="f440b-106">Converts a print ticket to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f440b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f440b-107">Syntax</span></span>


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a><span data-ttu-id="f440b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f440b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f440b-109">*hProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f440b-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-110">Um identificador para um provedor de tíquete de impressão aberto.</span><span class="sxs-lookup"><span data-stu-id="f440b-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="f440b-111">Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="f440b-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f440b-112">*pPrintTicket* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f440b-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-113">O buffer que contém o tíquete de impressão a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="f440b-113">The buffer that contains the print ticket to convert.</span></span>

</dd> <dt>

<span data-ttu-id="f440b-114">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f440b-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-115">O tamanho, em bytes, do buffer passado em *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f440b-115">The size, in bytes, of the buffer passed in *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="f440b-116">*BaseType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f440b-116">*baseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-117">Um valor que indica se [**o DEVMODE padrão do usuário ou o**](/windows/win32/api/wingdi/ns-wingdi-devmodea) **DEVMODE** padrão da fila de impressão é usado para fornecer valores para o **DEVMODE** de saída quando *pPrintTicket* não especifica todas as configurações possíveis para um **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="f440b-117">A value indicating whether the user's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) or the print queue's default **DEVMODE** is used to provide values to the output **DEVMODE** when *pPrintTicket* does not specify every possible setting for a **DEVMODE**.</span></span> <span data-ttu-id="f440b-118">O valor desse parâmetro deve ser um membro da enumeração [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , Cast como um **int**.</span><span class="sxs-lookup"><span data-stu-id="f440b-118">The value of this parameter must be a member of the [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) enumeration, cast as an **INT**.</span></span>

</dd> <dt>

<span data-ttu-id="f440b-119">*escopo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f440b-119">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-120">Um valor que especifica o escopo de *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f440b-120">A value that specifies the scope of *pPrintTicket*.</span></span> <span data-ttu-id="f440b-121">Esse valor pode especificar uma única página, um documento inteiro ou todos os documentos no trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="f440b-121">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="f440b-122">O valor desse parâmetro deve ser um membro da enumeração [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , Cast como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f440b-122">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="f440b-123">*ppDevmode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f440b-123">*ppDevmode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-124">O endereço do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)recém-criado.</span><span class="sxs-lookup"><span data-stu-id="f440b-124">The address of the newly created [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span> <span data-ttu-id="f440b-125">Essa função chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar esse buffer.</span><span class="sxs-lookup"><span data-stu-id="f440b-125">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="f440b-126">Quando o buffer não for mais necessário, o chamador deverá liberá-lo chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f440b-126">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="f440b-127">*pcbDevModeLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f440b-127">*pcbDevModeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-128">O tamanho, em bytes, do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornado em *ppDevmode*.</span><span class="sxs-lookup"><span data-stu-id="f440b-128">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) returned in *ppDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="f440b-129">*errMsg* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f440b-129">*errMsg* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f440b-130">Um ponteiro para uma cadeia de caracteres que especifica o que, se for algo, é inválido sobre o tíquete de impressão no *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="f440b-130">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pPrintTicket*.</span></span> <span data-ttu-id="f440b-131">Se for válido, isso será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f440b-131">If it is valid, this is **NULL**.</span></span> <span data-ttu-id="f440b-132">Se *errMsg* não for **nulo** quando a função retornar, o chamador deverá liberar a cadeia de caracteres com [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="f440b-132">If *errMsg* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f440b-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f440b-133">Return value</span></span>

<span data-ttu-id="f440b-134">Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f440b-134">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="f440b-135">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f440b-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f440b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f440b-136">Requirements</span></span>



| <span data-ttu-id="f440b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f440b-137">Requirement</span></span> | <span data-ttu-id="f440b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="f440b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f440b-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f440b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f440b-140">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f440b-140">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f440b-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f440b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f440b-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f440b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f440b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f440b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f440b-144"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f440b-144"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f440b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="f440b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f440b-146">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="f440b-146">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="f440b-147">**PTConvertPrintTicketToDevMode**</span><span class="sxs-lookup"><span data-stu-id="f440b-147">**PTConvertPrintTicketToDevMode**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[<span data-ttu-id="f440b-148">Impressão</span><span class="sxs-lookup"><span data-stu-id="f440b-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f440b-149">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="f440b-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

