---
description: A função ResetPrinter especifica o tipo de dados e os valores do modo de dispositivo a serem usados para imprimir documentos enviados pela função StartDocPrinter. Esses valores podem ser substituídos usando a função SetJob após o início da impressão do documento.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Função ResetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813997"
---
# <a name="resetprinter-function"></a><span data-ttu-id="01d4b-104">Função ResetPrinter</span><span class="sxs-lookup"><span data-stu-id="01d4b-104">ResetPrinter function</span></span>

<span data-ttu-id="01d4b-105">A função **ResetPrinter** especifica o tipo de dados e os valores do modo de dispositivo a serem usados para imprimir documentos enviados pela função [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="01d4b-105">The **ResetPrinter** function specifies the data type and device mode values to be used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="01d4b-106">Esses valores podem ser substituídos usando a função [**SetJob**](setjob.md) após o início da impressão do documento.</span><span class="sxs-lookup"><span data-stu-id="01d4b-106">These values can be overridden by using the [**SetJob**](setjob.md) function after document printing has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d4b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01d4b-107">Syntax</span></span>


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="01d4b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01d4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d4b-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01d4b-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d4b-110">Identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="01d4b-110">Handle to the printer.</span></span> <span data-ttu-id="01d4b-111">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="01d4b-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="01d4b-112">*pDefault* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01d4b-112">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d4b-113">Ponteiro para uma estrutura de [**\_ padrões de impressora**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="01d4b-113">Pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span>

<span data-ttu-id="01d4b-114">A função **ResetPrinter** ignora o membro **desiredAccess** da estrutura de [**\_ padrões da impressora**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="01d4b-114">The **ResetPrinter** function ignores the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="01d4b-115">Defina esse membro como zero.</span><span class="sxs-lookup"><span data-stu-id="01d4b-115">Set that member to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d4b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01d4b-116">Return value</span></span>

<span data-ttu-id="01d4b-117">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="01d4b-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="01d4b-118">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="01d4b-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d4b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="01d4b-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01d4b-120">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="01d4b-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="01d4b-121">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01d4b-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="01d4b-122">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="01d4b-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01d4b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01d4b-123">Requirements</span></span>



| <span data-ttu-id="01d4b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="01d4b-124">Requirement</span></span> | <span data-ttu-id="01d4b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="01d4b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d4b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01d4b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="01d4b-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01d4b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="01d4b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01d4b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="01d4b-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01d4b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="01d4b-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="01d4b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="01d4b-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01d4b-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="01d4b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01d4b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="01d4b-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01d4b-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="01d4b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="01d4b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d4b-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="01d4b-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="01d4b-136">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="01d4b-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="01d4b-137">**ResetPrinterW** (Unicode) e **ResetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="01d4b-137">**ResetPrinterW** (Unicode) and **ResetPrinterA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="01d4b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="01d4b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d4b-139">Impressão</span><span class="sxs-lookup"><span data-stu-id="01d4b-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="01d4b-140">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="01d4b-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="01d4b-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="01d4b-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="01d4b-142">**padrões de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="01d4b-142">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="01d4b-143">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="01d4b-143">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="01d4b-144">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="01d4b-144">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




