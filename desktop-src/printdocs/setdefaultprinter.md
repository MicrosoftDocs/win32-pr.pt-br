---
description: A função SetDefaultPrinter define o nome da impressora padrão para o usuário atual no computador local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Função SetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764267"
---
# <a name="setdefaultprinter-function"></a><span data-ttu-id="e122d-103">Função SetDefaultPrinter</span><span class="sxs-lookup"><span data-stu-id="e122d-103">SetDefaultPrinter function</span></span>

<span data-ttu-id="e122d-104">A função **SetDefaultPrinter** define o nome da impressora padrão para o usuário atual no computador local.</span><span class="sxs-lookup"><span data-stu-id="e122d-104">The **SetDefaultPrinter** function sets the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e122d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e122d-105">Syntax</span></span>


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="e122d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e122d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e122d-107">*pszPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e122d-107">*pszPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e122d-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="e122d-108">A pointer to a null-terminated string containing the default printer name.</span></span> <span data-ttu-id="e122d-109">Para uma conexão de impressora remota, o formato de nome é **\\\\** _Server_ *_\\_* _PrinterName_.</span><span class="sxs-lookup"><span data-stu-id="e122d-109">For a remote printer connection, the name format is **\\\\**_server_*_\\_*_printername_.</span></span> <span data-ttu-id="e122d-110">Para uma impressora local, o formato de nome é *PrinterName*.</span><span class="sxs-lookup"><span data-stu-id="e122d-110">For a local printer, the name format is *printername*.</span></span>

<span data-ttu-id="e122d-111">Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, ou seja, "", o **SetDefaultPrinter** selecionará uma impressora padrão de uma das impressoras instaladas.</span><span class="sxs-lookup"><span data-stu-id="e122d-111">If this parameter is **NULL** or an empty string, that is, "", **SetDefaultPrinter** will select a default printer from one of the installed printers.</span></span> <span data-ttu-id="e122d-112">Se uma impressora padrão já existir, chamar **SetDefaultPrinter** com uma cadeia de caracteres **nula** ou vazia nesse parâmetro poderá alterar a impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="e122d-112">If a default printer already exists, calling **SetDefaultPrinter** with a **NULL** or an empty string in this parameter might change the default printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e122d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e122d-113">Return value</span></span>

<span data-ttu-id="e122d-114">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e122d-114">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e122d-115">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="e122d-115">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e122d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e122d-116">Remarks</span></span>

<span data-ttu-id="e122d-117">Ao usar esse método, você deve especificar uma impressora, Driver e porta válidos.</span><span class="sxs-lookup"><span data-stu-id="e122d-117">When using this method, you must specify a valid printer, driver, and port.</span></span> <span data-ttu-id="e122d-118">Se forem inválidas, as APIs não falharão, mas o resultado não será definido.</span><span class="sxs-lookup"><span data-stu-id="e122d-118">If they are invalid, the APIs do not fail but the result is not defined.</span></span> <span data-ttu-id="e122d-119">Isso pode fazer com que outros programas configurassem a impressora de volta para a impressora válida anterior.</span><span class="sxs-lookup"><span data-stu-id="e122d-119">This could cause other programs to set the printer back to the previous valid printer.</span></span> <span data-ttu-id="e122d-120">Você pode usar [**EnumPrinters**](enumprinters.md) para recuperar o nome da impressora, o nome do driver e o nome da porta de todas as impressoras disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e122d-120">You can use [**EnumPrinters**](enumprinters.md) to retrieve the printer name, driver name, and port name of all available printers.</span></span>

> [!Note]  
> <span data-ttu-id="e122d-121">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e122d-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e122d-122">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e122d-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e122d-123">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e122d-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e122d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e122d-124">Requirements</span></span>



| <span data-ttu-id="e122d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e122d-125">Requirement</span></span> | <span data-ttu-id="e122d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e122d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e122d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e122d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e122d-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e122d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e122d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e122d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e122d-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e122d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e122d-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e122d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e122d-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e122d-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e122d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e122d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e122d-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e122d-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e122d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e122d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e122d-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e122d-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e122d-137">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e122d-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e122d-138">**SetDefaultPrinterW** (Unicode) e **SetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e122d-138">**SetDefaultPrinterW** (Unicode) and **SetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="e122d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e122d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e122d-140">Impressão</span><span class="sxs-lookup"><span data-stu-id="e122d-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e122d-141">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e122d-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e122d-142">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="e122d-142">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="e122d-143">**GetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="e122d-143">**GetDefaultPrinter**</span></span>](getdefaultprinter.md)
</dt> </dl>

 

 




