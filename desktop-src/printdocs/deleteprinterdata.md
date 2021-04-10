---
description: A função DeletePrinterData exclui os dados de configuração especificados para uma impressora. Os dados de configuração de impressoras consistem em um conjunto de valores nomeados e digitados. A função DeletePrinterData exclui um desses valores, especificados por seu nome de valor.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: Função DeletePrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296711"
---
# <a name="deleteprinterdata-function"></a><span data-ttu-id="e7605-105">Função DeletePrinterData</span><span class="sxs-lookup"><span data-stu-id="e7605-105">DeletePrinterData function</span></span>

<span data-ttu-id="e7605-106">A função **DeletePrinterData** exclui os dados de configuração especificados para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="e7605-106">The **DeletePrinterData** function deletes specified configuration data for a printer.</span></span> <span data-ttu-id="e7605-107">Os dados de configuração de uma impressora consistem em um conjunto de valores nomeados e digitados.</span><span class="sxs-lookup"><span data-stu-id="e7605-107">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="e7605-108">A função **DeletePrinterData** exclui um desses valores, especificados por seu nome de valor.</span><span class="sxs-lookup"><span data-stu-id="e7605-108">The **DeletePrinterData** function deletes one of these values, specified by its value name.</span></span>

<span data-ttu-id="e7605-109">Chamar **DeletePrinterData** é equivalente a chamar a função [**DeletePrinterDataEx**](deleteprinterdataex.md) com o parâmetro *pKeyName* definido como "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="e7605-109">Calling **DeletePrinterData** is equivalent to calling the [**DeletePrinterDataEx**](deleteprinterdataex.md) function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="e7605-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7605-110">Syntax</span></span>


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="e7605-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7605-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7605-112">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7605-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7605-113">Um identificador para a impressora cujos dados de configuração serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="e7605-113">A handle to the printer whose configuration data is to be deleted.</span></span> <span data-ttu-id="e7605-114">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="e7605-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e7605-115">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7605-115">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7605-116">Um ponteiro para o nome de terminação de nulo do valor dos dados de configuração a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="e7605-116">A pointer to the null-terminated name of the configuration data value to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7605-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7605-117">Return value</span></span>

<span data-ttu-id="e7605-118">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="e7605-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e7605-119">Se a função falhar, o valor de retorno será um código de erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="e7605-119">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7605-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7605-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e7605-121">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e7605-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e7605-122">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7605-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e7605-123">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e7605-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7605-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7605-124">Requirements</span></span>



| <span data-ttu-id="e7605-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7605-125">Requirement</span></span> | <span data-ttu-id="e7605-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e7605-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7605-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7605-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e7605-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7605-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e7605-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7605-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e7605-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7605-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e7605-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7605-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7605-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7605-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e7605-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7605-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7605-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7605-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e7605-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e7605-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7605-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e7605-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e7605-137">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e7605-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e7605-138">**DeletePrinterDataW** (Unicode) e **DeletePrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e7605-138">**DeletePrinterDataW** (Unicode) and **DeletePrinterDataA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="e7605-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7605-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7605-140">Impressão</span><span class="sxs-lookup"><span data-stu-id="e7605-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e7605-141">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e7605-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e7605-142">**EnumPrinterData**</span><span class="sxs-lookup"><span data-stu-id="e7605-142">**EnumPrinterData**</span></span>](enumprinterdata.md)
</dt> <dt>

[<span data-ttu-id="e7605-143">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="e7605-143">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="e7605-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e7605-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e7605-145">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="e7605-145">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="e7605-146">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="e7605-146">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

 




