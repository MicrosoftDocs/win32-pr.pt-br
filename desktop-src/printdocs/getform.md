---
description: A função GetForm recupera informações sobre um formulário especificado.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: Função GetForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785025"
---
# <a name="getform-function"></a><span data-ttu-id="c7c7e-103">Função GetForm</span><span class="sxs-lookup"><span data-stu-id="c7c7e-103">GetForm function</span></span>

<span data-ttu-id="c7c7e-104">A função **GetForm** recupera informações sobre um formulário especificado.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-104">The **GetForm** function retrieves information about a specified form.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c7e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7c7e-105">Syntax</span></span>


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="c7c7e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7c7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c7e-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c7e-108">Um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-108">A handle to the printer.</span></span> <span data-ttu-id="c7c7e-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="c7c7e-110">*pFormName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c7e-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do formulário.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-111">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="c7c7e-112">Para obter os nomes dos formulários com suporte pela impressora, chame a função [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="c7c7e-112">To get the names of the forms supported by the printer, call the [**EnumForms**](enumforms.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c7c7e-113">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c7e-114">A versão da estrutura à qual o *pForm* aponta.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-114">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="c7c7e-115">Esse valor deve ser 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-115">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c7c7e-116">*pForm* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-116">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c7e-117">Um ponteiro para uma matriz de bytes que recebe a estrutura do formulário inicializado [**\_ info \_ 1**](form-info-1.md) ou [**Form \_ info \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c7c7e-117">A pointer to an array of bytes that receives the initialized [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7c7e-118">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c7e-119">O tamanho, em bytes, da matriz *pForm* .</span><span class="sxs-lookup"><span data-stu-id="c7c7e-119">The size, in bytes, of the *pForm* array.</span></span>

</dd> <dt>

<span data-ttu-id="c7c7e-120">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c7e-121">Um ponteiro para um valor que especifica o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-121">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c7e-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7c7e-122">Return value</span></span>

<span data-ttu-id="c7c7e-123">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c7c7e-124">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c7e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7c7e-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c7c7e-126">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c7c7e-127">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c7c7e-128">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c7c7e-129">Se o chamador for remoto e o *nível* for 2, o valor de **StringType** do formulário retornado [**\_ informações \_ 2**](form-info-2.md) sempre será uma cadeia de caracteres \_ LANGPAIR.</span><span class="sxs-lookup"><span data-stu-id="c7c7e-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) will always be STRING\_LANGPAIR.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c7e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c7e-130">Requirements</span></span>



| <span data-ttu-id="c7c7e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c7e-131">Requirement</span></span> | <span data-ttu-id="c7c7e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c7c7e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c7e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c7e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c7e-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c7c7e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c7e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c7e-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7c7e-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c7c7e-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7c7e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c7e-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7c7e-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c7c7e-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7c7e-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7c7e-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7c7e-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c7c7e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c7e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c7e-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c7c7e-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c7c7e-143">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c7c7e-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c7c7e-144">**GetFormW** (Unicode) e **getformaa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c7c7e-144">**GetFormW** (Unicode) and **GetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="c7c7e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7c7e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c7e-146">Impressão</span><span class="sxs-lookup"><span data-stu-id="c7c7e-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c7c7e-147">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="c7c7e-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c7c7e-148">**AddFormat**</span><span class="sxs-lookup"><span data-stu-id="c7c7e-148">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="c7c7e-149">**DeleteForm**</span><span class="sxs-lookup"><span data-stu-id="c7c7e-149">**DeleteForm**</span></span>](deleteform.md)
</dt> <dt>

[<span data-ttu-id="c7c7e-150">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c7c7e-150">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c7c7e-151">**Formulário**</span><span class="sxs-lookup"><span data-stu-id="c7c7e-151">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




