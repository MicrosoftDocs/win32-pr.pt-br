---
description: A função WritePrinter notifica o spooler de impressão que os dados devem ser gravados na impressora especificada.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Função WritePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771298"
---
# <a name="writeprinter-function"></a><span data-ttu-id="b3d3c-103">Função WritePrinter</span><span class="sxs-lookup"><span data-stu-id="b3d3c-103">WritePrinter function</span></span>

<span data-ttu-id="b3d3c-104">A função **WritePrinter** notifica o spooler de impressão que os dados devem ser gravados na impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-104">The **WritePrinter** function notifies the print spooler that data should be written to the specified printer.</span></span>

> [!Note]  
> <span data-ttu-id="b3d3c-105">O **WritePrinter** dá suporte apenas à impressão GDI e não deve ser usado para impressão em XPS.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-105">**WritePrinter** only supports GDI printing and must not be used for XPS printing.</span></span> <span data-ttu-id="b3d3c-106">Se seu trabalho de impressão usar o caminho de impressão XPS ou OpenXPS, use a [API de impressão XPS](/windows/desktop/printdocs/xps-printing).</span><span class="sxs-lookup"><span data-stu-id="b3d3c-106">If your print job uses the XPS or the OpenXPS print path, then use the [XPS Print API](/windows/desktop/printdocs/xps-printing).</span></span> <span data-ttu-id="b3d3c-107">Não há suporte para o envio de trabalhos de impressão XPS ou OpenXPS para o spooler usando **WritePrinter** e isso pode resultar em resultados indeterminados.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-107">Sending XPS or OpenXPS print jobs to the spooler using **WritePrinter** is not supported and can result in undetermined results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b3d3c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3d3c-108">Syntax</span></span>


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a><span data-ttu-id="b3d3c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3d3c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3d3c-110">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3d3c-110">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d3c-111">Um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-111">A handle to the printer.</span></span> <span data-ttu-id="b3d3c-112">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-112">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b3d3c-113">*pBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3d3c-113">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d3c-114">Um ponteiro para uma matriz de bytes que contém os dados que devem ser gravados na impressora.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-114">A pointer to an array of bytes that contains the data that should be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="b3d3c-115">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3d3c-115">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d3c-116">O tamanho, em bytes, da matriz.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-116">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="b3d3c-117">*pcWritten* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3d3c-117">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d3c-118">Um ponteiro para um valor que recebe o número de bytes de dados que foram gravados na impressora.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-118">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3d3c-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3d3c-119">Return value</span></span>

<span data-ttu-id="b3d3c-120">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-120">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b3d3c-121">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-121">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d3c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3d3c-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b3d3c-123">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b3d3c-124">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b3d3c-125">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b3d3c-126">A sequência para um trabalho de impressão é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3d3c-126">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="b3d3c-127">Para iniciar um trabalho de impressão, chame [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b3d3c-127">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="b3d3c-128">Para iniciar cada página, chame [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b3d3c-128">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="b3d3c-129">Para gravar dados em uma página, chame **WritePrinter**.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-129">To write data to a page, call **WritePrinter**.</span></span>
4.  <span data-ttu-id="b3d3c-130">Para encerrar cada página, chame [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b3d3c-130">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="b3d3c-131">Repita 2, 3 e 4 para quantas páginas forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-131">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="b3d3c-132">Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b3d3c-132">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="b3d3c-133">Quando um documento de alto nível (como um arquivo Adobe PDF ou Microsoft Word) ou outros dados de impressora (como PCL, PS ou HPGL) são enviados diretamente para uma impressora, as configurações de impressão definidas no documento têm precedentes sobre as configurações de impressão do Windows.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-133">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings.</span></span> <span data-ttu-id="b3d3c-134">Documentos de saída quando o valor do membro *pDatatype* da estrutura [**info do documento \_ \_ 1**](doc-info-1.md) que foi passado no parâmetro *pDocInfo* da chamada [**StartDocPrinter**](startdocprinter.md) é "RAW" deve descrever totalmente as configurações do trabalho de impressão estilo de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)no idioma compreendido pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-134">Documents output when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW" must fully describe the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="b3d3c-135">Em versões do Windows anteriores ao Windows XP, quando uma página em um arquivo em spool excede aproximadamente 350 MB, ela pode falhar ao imprimir e não enviar uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-135">In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="b3d3c-136">Por exemplo, isso pode ocorrer ao imprimir arquivos EMF grandes.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-136">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="b3d3c-137">O limite de tamanho de página nas versões do Windows anteriores ao Windows XP depende de muitos fatores, incluindo a quantidade de memória virtual disponível, a quantidade de memória alocada por processos de chamada e a quantidade de fragmentação no heap de processo.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-137">The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span> <span data-ttu-id="b3d3c-138">No Windows XP e versões posteriores do Windows, os arquivos EMF devem ter 2 GB ou menos de tamanho.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-138">In Windows XP and later versions of Windows, EMF files must be 2GB or less in size.</span></span> <span data-ttu-id="b3d3c-139">Se **WritePrinter** for usado para gravar dados não EMF, como a PDL pronta para impressão, o tamanho do arquivo será limitado apenas pelo espaço em disco disponível.</span><span class="sxs-lookup"><span data-stu-id="b3d3c-139">If **WritePrinter** is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="b3d3c-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3d3c-140">Examples</span></span>

<span data-ttu-id="b3d3c-141">Para obter um programa de exemplo que usa essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="b3d3c-141">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d3c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3d3c-142">Requirements</span></span>



| <span data-ttu-id="b3d3c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d3c-143">Requirement</span></span> | <span data-ttu-id="b3d3c-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b3d3c-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d3c-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3d3c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d3c-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3d3c-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b3d3c-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3d3c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d3c-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3d3c-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b3d3c-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3d3c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3d3c-150"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d3c-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b3d3c-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3d3c-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3d3c-152"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3d3c-152"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b3d3c-153">DLL</span><span class="sxs-lookup"><span data-stu-id="b3d3c-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3d3c-154"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3d3c-154"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="b3d3c-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3d3c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d3c-156">Impressão</span><span class="sxs-lookup"><span data-stu-id="b3d3c-156">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b3d3c-157">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="b3d3c-157">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b3d3c-158">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b3d3c-158">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="b3d3c-159">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b3d3c-159">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b3d3c-160">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b3d3c-160">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b3d3c-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b3d3c-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="b3d3c-162">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="b3d3c-162">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="b3d3c-163">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="b3d3c-163">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

