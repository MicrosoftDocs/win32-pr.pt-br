---
description: A função ClosePrinter fecha o objeto de impressora especificado.
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: Função ClosePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bd21268b86a07357065d4f33b60d1af4b05fa019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171597"
---
# <a name="closeprinter-function"></a><span data-ttu-id="928b3-103">Função ClosePrinter</span><span class="sxs-lookup"><span data-stu-id="928b3-103">ClosePrinter function</span></span>

<span data-ttu-id="928b3-104">A função **ClosePrinter** fecha o objeto de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="928b3-104">The **ClosePrinter** function closes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="928b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="928b3-105">Syntax</span></span>


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="928b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="928b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928b3-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="928b3-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="928b3-108">Um identificador para o objeto de impressora a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="928b3-108">A handle to the printer object to be closed.</span></span> <span data-ttu-id="928b3-109">Esse identificador é retornado pela função [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="928b3-109">This handle is returned by the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928b3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="928b3-110">Return value</span></span>

<span data-ttu-id="928b3-111">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="928b3-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="928b3-112">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="928b3-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="928b3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="928b3-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="928b3-114">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="928b3-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="928b3-115">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="928b3-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="928b3-116">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="928b3-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="928b3-117">Quando a função **ClosePrinter** retorna, o identificador *hPrinter* é inválido, independentemente de a função ter sido bem-sucedida ou falhou.</span><span class="sxs-lookup"><span data-stu-id="928b3-117">When the **ClosePrinter** function returns, the handle *hPrinter* is invalid, regardless of whether the function has succeeded or failed.</span></span>

## <a name="examples"></a><span data-ttu-id="928b3-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="928b3-118">Examples</span></span>

<span data-ttu-id="928b3-119">Para obter um programa de exemplo que usa essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="928b3-119">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="928b3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="928b3-120">Requirements</span></span>



| <span data-ttu-id="928b3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="928b3-121">Requirement</span></span> | <span data-ttu-id="928b3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="928b3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="928b3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="928b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="928b3-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="928b3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="928b3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="928b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="928b3-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="928b3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="928b3-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="928b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="928b3-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="928b3-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="928b3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="928b3-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="928b3-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="928b3-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="928b3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="928b3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="928b3-132"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="928b3-132"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="928b3-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="928b3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="928b3-134">Impressão</span><span class="sxs-lookup"><span data-stu-id="928b3-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="928b3-135">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="928b3-135">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="928b3-136">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="928b3-136">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="928b3-137">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="928b3-137">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




