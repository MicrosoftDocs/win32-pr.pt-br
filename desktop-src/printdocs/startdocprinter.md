---
description: A função StartDocPrinter notifica o spooler de impressão de que um documento deve ser colocado no spool para impressão.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Função StartDocPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836892"
---
# <a name="startdocprinter-function"></a><span data-ttu-id="20347-103">Função StartDocPrinter</span><span class="sxs-lookup"><span data-stu-id="20347-103">StartDocPrinter function</span></span>

<span data-ttu-id="20347-104">A função **StartDocPrinter** notifica o spooler de impressão de que um documento deve ser colocado no spool para impressão.</span><span class="sxs-lookup"><span data-stu-id="20347-104">The **StartDocPrinter** function notifies the print spooler that a document is to be spooled for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="20347-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20347-105">Syntax</span></span>


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a><span data-ttu-id="20347-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20347-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20347-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20347-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20347-108">Um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="20347-108">A handle to the printer.</span></span> <span data-ttu-id="20347-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="20347-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="20347-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="20347-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20347-111">A versão da estrutura à qual o *pDocInfo* aponta.</span><span class="sxs-lookup"><span data-stu-id="20347-111">The version of the structure to which *pDocInfo* points.</span></span> <span data-ttu-id="20347-112">Esse valor deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="20347-112">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="20347-113">*pDocInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20347-113">*pDocInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20347-114">Um ponteiro para uma [**estrutura \_ info \_**](doc-info-1.md) do documento 1 que descreve o documento a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="20347-114">A pointer to a [**DOC\_INFO\_1**](doc-info-1.md) structure that describes the document to print.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20347-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20347-115">Return value</span></span>

<span data-ttu-id="20347-116">Se a função for realizada com sucesso, o valor de retorno identificará o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="20347-116">If the function succeeds, the return value identifies the print job.</span></span>

<span data-ttu-id="20347-117">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="20347-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="20347-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="20347-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="20347-119">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="20347-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="20347-120">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="20347-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="20347-121">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="20347-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="20347-122">A sequência típica para um trabalho de impressão é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="20347-122">The typical sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="20347-123">Para iniciar um trabalho de impressão, chame **StartDocPrinter**.</span><span class="sxs-lookup"><span data-stu-id="20347-123">To begin a print job, call **StartDocPrinter**.</span></span>
2.  <span data-ttu-id="20347-124">Para iniciar cada página, chame [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="20347-124">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="20347-125">Para gravar dados em uma página, chame [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="20347-125">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="20347-126">Para encerrar cada página, chame [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="20347-126">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="20347-127">Repita 2, 3 e 4 para quantas páginas forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="20347-127">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="20347-128">Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="20347-128">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="20347-129">Observe que a chamada de [**StartPagePrinter**](startpageprinter.md) e [**EndPagePrinter**](endpageprinter.md) pode não ser necessária, como se o tipo de dados de impressão incluir as informações da página.</span><span class="sxs-lookup"><span data-stu-id="20347-129">Note that calling [**StartPagePrinter**](startpageprinter.md) and [**EndPagePrinter**](endpageprinter.md) may not be necessary, such as if the print data type includes the page information.</span></span>

<span data-ttu-id="20347-130">Quando uma página em um arquivo em spool excede aproximadamente 350 MB, ela pode falhar ao imprimir e não enviar uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="20347-130">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="20347-131">Por exemplo, isso pode ocorrer ao imprimir arquivos EMF grandes.</span><span class="sxs-lookup"><span data-stu-id="20347-131">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="20347-132">O limite de tamanho de página depende de muitos fatores, incluindo a quantidade de memória virtual disponível, a quantidade de memória alocada por processos de chamada e a quantidade de fragmentação no heap de processo.</span><span class="sxs-lookup"><span data-stu-id="20347-132">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="20347-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20347-133">Examples</span></span>

<span data-ttu-id="20347-134">Para obter um programa de exemplo que usa essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="20347-134">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20347-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20347-135">Requirements</span></span>



| <span data-ttu-id="20347-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="20347-136">Requirement</span></span> | <span data-ttu-id="20347-137">Valor</span><span class="sxs-lookup"><span data-stu-id="20347-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20347-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20347-138">Minimum supported client</span></span><br/> | <span data-ttu-id="20347-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20347-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="20347-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20347-140">Minimum supported server</span></span><br/> | <span data-ttu-id="20347-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20347-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="20347-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20347-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="20347-143"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20347-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="20347-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20347-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="20347-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20347-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="20347-146">DLL</span><span class="sxs-lookup"><span data-stu-id="20347-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20347-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="20347-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="20347-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="20347-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="20347-149">**StartDocPrinterW** (Unicode) e **StartDocPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="20347-149">**StartDocPrinterW** (Unicode) and **StartDocPrinterA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="20347-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="20347-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20347-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="20347-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="20347-152">**Informações do documento \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="20347-152">**DOC\_INFO\_1**</span></span>](doc-info-1.md)
</dt> <dt>

[<span data-ttu-id="20347-153">**Informações do documento \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="20347-153">**DOC\_INFO\_2**</span></span>](doc-info-2.md)
</dt> <dt>

[<span data-ttu-id="20347-154">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="20347-154">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="20347-155">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="20347-155">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="20347-156">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="20347-156">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="20347-157">Impressão</span><span class="sxs-lookup"><span data-stu-id="20347-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="20347-158">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="20347-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="20347-159">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="20347-159">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="20347-160">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="20347-160">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="20347-161">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="20347-161">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




