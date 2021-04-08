---
description: A função StartPagePrinter notifica o spooler de que uma página está prestes a ser impressa na impressora especificada.
ms.assetid: 8ac7c47b-b3a7-4642-bfb7-54e014139fbf
title: Função StartPagePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f8d1c5cc296fae1b166b891fc881a6abcdb6b2af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921604"
---
# <a name="startpageprinter-function"></a><span data-ttu-id="d6feb-103">Função StartPagePrinter</span><span class="sxs-lookup"><span data-stu-id="d6feb-103">StartPagePrinter function</span></span>

<span data-ttu-id="d6feb-104">A função **StartPagePrinter** notifica o spooler de que uma página está prestes a ser impressa na impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="d6feb-104">The **StartPagePrinter** function notifies the spooler that a page is about to be printed on the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6feb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6feb-105">Syntax</span></span>


```C++
BOOL StartPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="d6feb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6feb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6feb-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6feb-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6feb-108">Identificador para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="d6feb-108">Handle to a printer.</span></span> <span data-ttu-id="d6feb-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="d6feb-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6feb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6feb-110">Return value</span></span>

<span data-ttu-id="d6feb-111">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d6feb-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d6feb-112">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="d6feb-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6feb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6feb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6feb-114">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d6feb-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d6feb-115">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6feb-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d6feb-116">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="d6feb-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d6feb-117">A sequência para um trabalho de impressão é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="d6feb-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="d6feb-118">Para iniciar um trabalho de impressão, chame [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d6feb-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="d6feb-119">Para iniciar cada página, chame **StartPagePrinter**.</span><span class="sxs-lookup"><span data-stu-id="d6feb-119">To begin each page, call **StartPagePrinter**.</span></span>
3.  <span data-ttu-id="d6feb-120">Para gravar dados em uma página, chame [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d6feb-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="d6feb-121">Para encerrar cada página, chame [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d6feb-121">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="d6feb-122">Repita 2, 3 e 4 para quantas páginas forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="d6feb-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="d6feb-123">Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="d6feb-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="d6feb-124">Quando uma página em um arquivo em spool excede aproximadamente 350 MB, ela pode falhar ao imprimir e não enviar uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="d6feb-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="d6feb-125">Por exemplo, isso pode ocorrer ao imprimir arquivos EMF grandes.</span><span class="sxs-lookup"><span data-stu-id="d6feb-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="d6feb-126">O limite de tamanho de página depende de muitos fatores, incluindo a quantidade de memória virtual disponível, a quantidade de memória alocada por processos de chamada e a quantidade de fragmentação no heap de processo.</span><span class="sxs-lookup"><span data-stu-id="d6feb-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="d6feb-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6feb-127">Examples</span></span>

<span data-ttu-id="d6feb-128">Para obter um programa de exemplo que usa essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="d6feb-128">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6feb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6feb-129">Requirements</span></span>



| <span data-ttu-id="d6feb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6feb-130">Requirement</span></span> | <span data-ttu-id="d6feb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d6feb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6feb-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6feb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d6feb-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6feb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d6feb-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6feb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d6feb-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6feb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d6feb-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d6feb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6feb-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6feb-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d6feb-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6feb-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6feb-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6feb-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d6feb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d6feb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6feb-141"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6feb-141"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d6feb-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6feb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6feb-143">Impressão</span><span class="sxs-lookup"><span data-stu-id="d6feb-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d6feb-144">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="d6feb-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d6feb-145">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="d6feb-145">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="d6feb-146">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="d6feb-146">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="d6feb-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d6feb-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d6feb-148">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="d6feb-148">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="d6feb-149">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="d6feb-149">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="d6feb-150">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="d6feb-150">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




