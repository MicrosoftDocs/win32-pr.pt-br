---
description: A função EndPagePrinter notifica o spooler de impressão que o aplicativo está no final de uma página em um trabalho de impressão.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: Função EndPagePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 45e8ce005953e07f10ec621660ed38e68d50c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091595"
---
# <a name="endpageprinter-function"></a><span data-ttu-id="23fc6-103">Função EndPagePrinter</span><span class="sxs-lookup"><span data-stu-id="23fc6-103">EndPagePrinter function</span></span>

<span data-ttu-id="23fc6-104">A função **EndPagePrinter** notifica o spooler de impressão que o aplicativo está no final de uma página em um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="23fc6-104">The **EndPagePrinter** function notifies the print spooler that the application is at the end of a page in a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fc6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23fc6-105">Syntax</span></span>


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="23fc6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23fc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23fc6-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23fc6-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23fc6-108">Identificador para a impressora para a qual a página será concluída.</span><span class="sxs-lookup"><span data-stu-id="23fc6-108">Handle to the printer for which the page will be concluded.</span></span> <span data-ttu-id="23fc6-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="23fc6-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23fc6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23fc6-110">Return value</span></span>

<span data-ttu-id="23fc6-111">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="23fc6-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="23fc6-112">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="23fc6-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="23fc6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="23fc6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23fc6-114">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="23fc6-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="23fc6-115">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23fc6-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="23fc6-116">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="23fc6-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="23fc6-117">A sequência para um trabalho de impressão é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="23fc6-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="23fc6-118">Para iniciar um trabalho de impressão, chame [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="23fc6-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="23fc6-119">Para iniciar cada página, chame [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="23fc6-119">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="23fc6-120">Para gravar dados em uma página, chame [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="23fc6-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="23fc6-121">Para encerrar cada página, chame **EndPagePrinter**.</span><span class="sxs-lookup"><span data-stu-id="23fc6-121">To end each page, call **EndPagePrinter**.</span></span>
5.  <span data-ttu-id="23fc6-122">Repita 2, 3 e 4 para quantas páginas forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="23fc6-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="23fc6-123">Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="23fc6-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="23fc6-124">Quando uma página em um arquivo em spool excede aproximadamente 350 MB, ela pode falhar ao imprimir e não enviar uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="23fc6-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="23fc6-125">Por exemplo, isso pode ocorrer ao imprimir arquivos EMF grandes.</span><span class="sxs-lookup"><span data-stu-id="23fc6-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="23fc6-126">O limite de tamanho de página depende de muitos fatores, incluindo a quantidade de memória virtual disponível, a quantidade de memória alocada por processos de chamada e a quantidade de fragmentação no heap de processo.</span><span class="sxs-lookup"><span data-stu-id="23fc6-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="23fc6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23fc6-127">Requirements</span></span>



| <span data-ttu-id="23fc6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fc6-128">Requirement</span></span> | <span data-ttu-id="23fc6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="23fc6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23fc6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fc6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="23fc6-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="23fc6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="23fc6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fc6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="23fc6-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="23fc6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="23fc6-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="23fc6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="23fc6-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23fc6-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="23fc6-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23fc6-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="23fc6-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23fc6-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="23fc6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="23fc6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23fc6-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23fc6-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="23fc6-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="23fc6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fc6-141">Impressão</span><span class="sxs-lookup"><span data-stu-id="23fc6-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="23fc6-142">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="23fc6-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="23fc6-143">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="23fc6-143">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="23fc6-144">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="23fc6-144">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="23fc6-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="23fc6-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="23fc6-146">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="23fc6-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="23fc6-147">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="23fc6-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="23fc6-148">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="23fc6-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




