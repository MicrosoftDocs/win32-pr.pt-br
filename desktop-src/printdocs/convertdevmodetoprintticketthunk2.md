---
description: Converte uma estrutura DEVMODE em um tíquete de impressão.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: Função ConvertDevModeToPrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785321"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a><span data-ttu-id="d6d52-103">Função ConvertDevModeToPrintTicketThunk2</span><span class="sxs-lookup"><span data-stu-id="d6d52-103">ConvertDevModeToPrintTicketThunk2 function</span></span>

<span data-ttu-id="d6d52-104">\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6d52-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="d6d52-105">O [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fornece funcionalidade equivalente e deve ser usado em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="d6d52-106">Converte uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) em um tíquete de impressão.</span><span class="sxs-lookup"><span data-stu-id="d6d52-106">Converts a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to a print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d52-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6d52-107">Syntax</span></span>


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a><span data-ttu-id="d6d52-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6d52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d52-109">*hProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d52-110">Um identificador para um provedor de tíquete de impressão aberto.</span><span class="sxs-lookup"><span data-stu-id="d6d52-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="d6d52-111">Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d52-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d6d52-112">*pDevmode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-112">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d52-113">Um ponteiro para o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="d6d52-113">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to convert.</span></span>

</dd> <dt>

<span data-ttu-id="d6d52-114">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d52-115">O tamanho, em bytes, do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passado em *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="d6d52-115">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="d6d52-116">*escopo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-116">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d52-117">Um valor que especifica o escopo de *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="d6d52-117">A value that specifies the scope of *ppPrintTicket*.</span></span> <span data-ttu-id="d6d52-118">Esse valor pode especificar uma única página, um documento inteiro ou todos os documentos no trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="d6d52-118">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="d6d52-119">O valor desse parâmetro deve ser um membro da enumeração [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , Cast como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="d6d52-119">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="d6d52-120">*ppPrintTicket* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-120">*ppPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d52-121">O endereço do buffer que contém um tíquete de impressão que representa o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passado em *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="d6d52-121">The address of the buffer that contains a print ticket that represents the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span> <span data-ttu-id="d6d52-122">Essa função chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar esse buffer.</span><span class="sxs-lookup"><span data-stu-id="d6d52-122">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="d6d52-123">Quando o buffer não for mais necessário, o chamador deverá liberá-lo chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="d6d52-123">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="d6d52-124">*pcbPrintTicketLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-124">*pcbPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d52-125">O tamanho, em bytes, do tíquete de impressão retornado em *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="d6d52-125">The size, in bytes, of the print ticket returned in *ppPrintTicket*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d52-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6d52-126">Return value</span></span>

<span data-ttu-id="d6d52-127">Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6d52-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="d6d52-128">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="d6d52-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d52-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6d52-129">Requirements</span></span>



| <span data-ttu-id="d6d52-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6d52-130">Requirement</span></span> | <span data-ttu-id="d6d52-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d6d52-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d52-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6d52-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d52-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d6d52-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6d52-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d52-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d6d52-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d6d52-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d52-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d52-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d52-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d52-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6d52-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d52-139">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="d6d52-139">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="d6d52-140">**PTConvertDevModeToPrintTicket**</span><span class="sxs-lookup"><span data-stu-id="d6d52-140">**PTConvertDevModeToPrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[<span data-ttu-id="d6d52-141">Impressão</span><span class="sxs-lookup"><span data-stu-id="d6d52-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d6d52-142">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="d6d52-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

