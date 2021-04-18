---
description: A função AbortPrinter excluirá um arquivo de spool de impressoras se a impressora estiver configurada para o spool.
ms.assetid: b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc
title: Função AbortPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbortPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f28e0c921db8fd075b6cad0e1df07401faaaffb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771781"
---
# <a name="abortprinter-function"></a><span data-ttu-id="5ac63-103">Função AbortPrinter</span><span class="sxs-lookup"><span data-stu-id="5ac63-103">AbortPrinter function</span></span>

<span data-ttu-id="5ac63-104">A função **AbortPrinter** excluirá o arquivo de spool de uma impressora se a impressora estiver configurada para o spool.</span><span class="sxs-lookup"><span data-stu-id="5ac63-104">The **AbortPrinter** function deletes a printer's spool file if the printer is configured for spooling.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac63-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ac63-105">Syntax</span></span>


```C++
BOOL AbortPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="5ac63-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ac63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac63-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ac63-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac63-108">Identificador para a impressora da qual o arquivo de spool é excluído.</span><span class="sxs-lookup"><span data-stu-id="5ac63-108">Handle to the printer from which the spool file is deleted.</span></span> <span data-ttu-id="5ac63-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="5ac63-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac63-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ac63-110">Return value</span></span>

<span data-ttu-id="5ac63-111">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5ac63-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5ac63-112">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="5ac63-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac63-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ac63-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ac63-114">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5ac63-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5ac63-115">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ac63-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5ac63-116">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="5ac63-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5ac63-117">Se a impressora não estiver configurada para o spool, a função **AbortPrinter** não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="5ac63-117">If the printer is not configured for spooling, the **AbortPrinter** function has no effect.</span></span>

<span data-ttu-id="5ac63-118">A sequência para um trabalho de impressão é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="5ac63-118">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="5ac63-119">Para iniciar um trabalho de impressão, chame [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="5ac63-119">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="5ac63-120">Para iniciar cada página, chame [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="5ac63-120">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="5ac63-121">Para gravar dados em uma página, chame [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="5ac63-121">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="5ac63-122">Para encerrar cada página, chame [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="5ac63-122">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="5ac63-123">Repita 2, 3 e 4 para quantas páginas forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="5ac63-123">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="5ac63-124">Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="5ac63-124">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="5ac63-125">Quando uma página em um arquivo em spool excede aproximadamente 350 MB, ela pode falhar ao imprimir e não enviar uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="5ac63-125">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="5ac63-126">Por exemplo, isso pode ocorrer ao imprimir arquivos EMF grandes.</span><span class="sxs-lookup"><span data-stu-id="5ac63-126">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="5ac63-127">O limite de tamanho de página depende de muitos fatores, incluindo a quantidade de memória virtual disponível, a quantidade de memória alocada por processos de chamada e a quantidade de fragmentação no heap de processo.</span><span class="sxs-lookup"><span data-stu-id="5ac63-127">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac63-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ac63-128">Requirements</span></span>



| <span data-ttu-id="5ac63-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac63-129">Requirement</span></span> | <span data-ttu-id="5ac63-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5ac63-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac63-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ac63-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac63-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ac63-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ac63-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ac63-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac63-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ac63-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ac63-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5ac63-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac63-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac63-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5ac63-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ac63-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ac63-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ac63-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5ac63-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5ac63-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ac63-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ac63-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="5ac63-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ac63-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac63-142">Impressão</span><span class="sxs-lookup"><span data-stu-id="5ac63-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5ac63-143">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="5ac63-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5ac63-144">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="5ac63-144">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="5ac63-145">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="5ac63-145">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="5ac63-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="5ac63-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="5ac63-147">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="5ac63-147">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="5ac63-148">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="5ac63-148">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="5ac63-149">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="5ac63-149">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




