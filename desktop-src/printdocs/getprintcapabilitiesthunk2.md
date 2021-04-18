---
description: Recupera os recursos de impressoras formatados em conformidade com o esquema de impressão XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: Função GetPrintCapabilitiesThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789314"
---
# <a name="getprintcapabilitiesthunk2-function"></a><span data-ttu-id="5263a-103">Função GetPrintCapabilitiesThunk2</span><span class="sxs-lookup"><span data-stu-id="5263a-103">GetPrintCapabilitiesThunk2 function</span></span>

<span data-ttu-id="5263a-104">\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="5263a-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="5263a-105">O [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) fornece funcionalidade equivalente e deve ser usado em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="5263a-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="5263a-106">Recupera os recursos da impressora formatados em conformidade com o [esquema de impressão](./printschema.md)XML.</span><span class="sxs-lookup"><span data-stu-id="5263a-106">Retrieves the printer's capabilities formatted in compliance with the XML [Print Schema](./printschema.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5263a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5263a-107">Syntax</span></span>


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="5263a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5263a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5263a-109">*hProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5263a-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5263a-110">Um identificador para um provedor de tíquete de impressão aberto.</span><span class="sxs-lookup"><span data-stu-id="5263a-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="5263a-111">Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="5263a-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5263a-112">*pPrintTicket* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5263a-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5263a-113">O buffer que contém os dados de tíquete de impressão, expressos em XML, conforme descrito no [esquema de impressão](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="5263a-113">The buffer that contains the print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="5263a-114">*cbPrintTicket* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5263a-114">*cbPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5263a-115">O tamanho, em bytes, do buffer referenciado por *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="5263a-115">The size, in bytes, of the buffer referenced by *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="5263a-116">*ppbPrintCapabilities* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5263a-116">*ppbPrintCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5263a-117">O endereço do buffer que é alocado por essa função e contém as informações válidas de recursos de impressão, codificados como XML.</span><span class="sxs-lookup"><span data-stu-id="5263a-117">The address of the buffer that is allocated by this function and contains the valid print capabilities information, encoded as XML.</span></span> <span data-ttu-id="5263a-118">Essa função chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar esse buffer.</span><span class="sxs-lookup"><span data-stu-id="5263a-118">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="5263a-119">Quando o buffer não for mais necessário, o chamador deverá liberá-lo chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="5263a-119">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="5263a-120">*pcbPrintCapabilitiesLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5263a-120">*pcbPrintCapabilitiesLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5263a-121">O tamanho, em bytes, do buffer referenciado por *ppbPrintCapabilities*.</span><span class="sxs-lookup"><span data-stu-id="5263a-121">The size, in bytes, of the buffer referenced by *ppbPrintCapabilities*.</span></span>

</dd> <dt>

<span data-ttu-id="5263a-122">*pbstrErrorMessage* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5263a-122">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5263a-123">Um ponteiro para uma cadeia de caracteres que especifica o que, se for algo, é inválido sobre *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="5263a-123">A pointer to a string that specifies what, if anything, is invalid about *pPrintTicket*.</span></span> <span data-ttu-id="5263a-124">Se for válido, esse valor será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5263a-124">If it is valid, this value is **NULL**.</span></span> <span data-ttu-id="5263a-125">Se *pbstrErrorMessage* não for **nulo** quando a função retornar, o chamador deverá liberar a cadeia de caracteres com [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="5263a-125">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5263a-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5263a-126">Return value</span></span>

<span data-ttu-id="5263a-127">Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5263a-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="5263a-128">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="5263a-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5263a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5263a-129">Requirements</span></span>



| <span data-ttu-id="5263a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5263a-130">Requirement</span></span> | <span data-ttu-id="5263a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5263a-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5263a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5263a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5263a-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5263a-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5263a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5263a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5263a-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5263a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5263a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5263a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5263a-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5263a-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5263a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5263a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5263a-139">**PTGetPrintCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5263a-139">**PTGetPrintCapabilities**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[<span data-ttu-id="5263a-140">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="5263a-140">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="5263a-141">Impressão</span><span class="sxs-lookup"><span data-stu-id="5263a-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5263a-142">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="5263a-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

