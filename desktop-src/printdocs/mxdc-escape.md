---
description: A \_ função de escape de impressora de escape MXDC permite que os aplicativos gravem documentos em um arquivo ou em uma impressora no formato XPS (XML Paper Specification) por meio do MXDC (Microsoft XPS Document Converter).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: Função MXDC_ESCAPE (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751159"
---
# <a name="mxdc_escape-function"></a><span data-ttu-id="84faf-103">\_Função de escape MXDC</span><span class="sxs-lookup"><span data-stu-id="84faf-103">MXDC\_ESCAPE function</span></span>

<span data-ttu-id="84faf-104">A função de escape de impressora de **\_ escape MXDC** permite que os aplicativos gravem documentos em um arquivo ou em uma impressora no formato XPS (XML Paper Specification) por meio do MXDC (Microsoft XPS Document Converter).</span><span class="sxs-lookup"><span data-stu-id="84faf-104">The **MXDC\_ESCAPE** printer escape function enables applications to write documents to a file or to a printer in XML Paper Specification (XPS) format by means of the Microsoft XPS Document Converter (MXDC).</span></span>

<span data-ttu-id="84faf-105">Para executar essa operação, chame a função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="84faf-105">To perform this operation, call the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function with the following parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="84faf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84faf-106">Syntax</span></span>


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a><span data-ttu-id="84faf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84faf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84faf-108">*HDC*</span><span class="sxs-lookup"><span data-stu-id="84faf-108">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="84faf-109">Um identificador para o contexto do dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="84faf-109">A handle to the printer device context.</span></span>

</dd> <dt>

<span data-ttu-id="84faf-110">*cbInput*</span><span class="sxs-lookup"><span data-stu-id="84faf-110">*cbInput*</span></span> 
</dt> <dd>

<span data-ttu-id="84faf-111">O tamanho, em bytes, dos dados apontados pelo parâmetro *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="84faf-111">The size, in bytes, of the data pointed to by the *lpszInData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="84faf-112">*lpszInData*</span><span class="sxs-lookup"><span data-stu-id="84faf-112">*lpszInData*</span></span> 
</dt> <dd>

<span data-ttu-id="84faf-113">Um ponteiro para um buffer que contém os dados de entrada, que são sempre armazenados em uma das estruturas a seguir.</span><span class="sxs-lookup"><span data-stu-id="84faf-113">A pointer to a buffer containing the input data, which is always stored in one of the following structures.</span></span>

<dl> <dd><span data-ttu-id="84faf-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span><span class="sxs-lookup"><span data-stu-id="84faf-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span></span></dd> <dd><span data-ttu-id="84faf-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span><span class="sxs-lookup"><span data-stu-id="84faf-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span></span></dd> <dd><span data-ttu-id="84faf-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span><span class="sxs-lookup"><span data-stu-id="84faf-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span></span></dd> <dd><span data-ttu-id="84faf-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span><span class="sxs-lookup"><span data-stu-id="84faf-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span></span></dd> </dl>

<span data-ttu-id="84faf-118">Cada uma dessas estruturas tem um membro opcode que especifica o que o MXDC deve fazer.</span><span class="sxs-lookup"><span data-stu-id="84faf-118">Each of these structures has an opcode member that specifies what the MXDC is supposed to do.</span></span> <span data-ttu-id="84faf-119">Consulte MxdcEscapeHeader para comentários detalhados sobre esses códigos.</span><span class="sxs-lookup"><span data-stu-id="84faf-119">See MxdcEscapeHeader for detailed remarks about these codes.</span></span>



| <span data-ttu-id="84faf-120">Código de operações (opcode)</span><span class="sxs-lookup"><span data-stu-id="84faf-120">Operations code (opcode)</span></span>                                                                                                                                                                                                  | <span data-ttu-id="84faf-121">Ação</span><span class="sxs-lookup"><span data-stu-id="84faf-121">Action</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <span data-ttu-id="84faf-122"><dt>**MXDCOP \_ obter \_ nome de arquivo**</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-122"><dt>**MXDCOP\_GET\_FILENAME**</dt></span></span> </dl>                                          | <span data-ttu-id="84faf-123">Define o parâmetro *lpszOutData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) como, o caminho completo do arquivo de saída como uma cadeia de caracteres terminada em zero ou o tamanho dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="84faf-123">Sets the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function to, either the full path of the output file as a zero-terminated string or else the size of that string.</span></span><br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <span data-ttu-id="84faf-124"><dt>**\_Seq de \_ \_ Doc fixo \_ do MXDCOP PRINTTICKET**</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-124"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**</dt></span></span> </dl> | <span data-ttu-id="84faf-125">Associa um tíquete de impressão a uma sequência de documento fixa XPS.</span><span class="sxs-lookup"><span data-stu-id="84faf-125">Associates a print ticket with an XPS fixed document sequence.</span></span><br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <span data-ttu-id="84faf-126"><dt>**\_ \_ Doc fixo do MXDCOP PRINTTICKET \_**</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-126"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC**</dt></span></span> </dl>              | <span data-ttu-id="84faf-127">Associa um tíquete de impressão a um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="84faf-127">Associates a print ticket with an XPS document.</span></span><br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <span data-ttu-id="84faf-128"><dt>**\_ \_ página fixa do MXDCOP PRINTTICKET \_**</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-128"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_PAGE**</dt></span></span> </dl>           | <span data-ttu-id="84faf-129">Associa um tíquete de impressão a uma página XPS.</span><span class="sxs-lookup"><span data-stu-id="84faf-129">Associates a print ticket with an XPS page.</span></span><br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <span data-ttu-id="84faf-130"><dt>**MXDCOP \_ set \_ S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-130"><dt>**MXDCOP\_SET\_S0PAGE**</dt></span></span> </dl>                                                | <span data-ttu-id="84faf-131">Envia a marcação XPS da página atual para a saída.</span><span class="sxs-lookup"><span data-stu-id="84faf-131">Sends the XPS markup of the current page to the output.</span></span><br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <span data-ttu-id="84faf-132"><dt>**MXDCOP \_ definir \_ \_ recurso S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-132"><dt>**MXDCOP\_SET\_S0PAGE\_RESOURCE**</dt></span></span> </dl>                    | <span data-ttu-id="84faf-133">Envia um recurso na página, como uma imagem ou fonte, para a saída.</span><span class="sxs-lookup"><span data-stu-id="84faf-133">Sends a resource on the page, such as an image or font, to the output.</span></span><br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <span data-ttu-id="84faf-134"><dt>**MXDCOP \_ definir \_ \_ modo XPSPASSTHRU**</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-134"><dt>**MXDCOP\_SET\_XPSPASSTHRU\_MODE**</dt></span></span> </dl>                 | <span data-ttu-id="84faf-135">Coloca o MXDC em um estado de passagem, permitindo que um aplicativo grave o XPS diretamente no arquivo de saída sem nenhum processamento pelo MXDC.</span><span class="sxs-lookup"><span data-stu-id="84faf-135">Puts the MXDC into a pass through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="84faf-136">Um documento inteiro ou até mesmo uma sequência de documento pode ser escrito dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="84faf-136">An entire document or even document sequence can be written in this way.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84faf-137">*cbOutput*</span><span class="sxs-lookup"><span data-stu-id="84faf-137">*cbOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="84faf-138">O tamanho, em bytes, dos dados apontados pelo parâmetro *lpszOutData* .</span><span class="sxs-lookup"><span data-stu-id="84faf-138">The size, in bytes, of the data pointed to by the *lpszOutData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="84faf-139">*lpszOutData*</span><span class="sxs-lookup"><span data-stu-id="84faf-139">*lpszOutData*</span></span> 
</dt> <dd>

<span data-ttu-id="84faf-140">Um ponteiro para um buffer que contém os dados de saída.</span><span class="sxs-lookup"><span data-stu-id="84faf-140">A pointer to a buffer containing the output data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84faf-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84faf-141">Return value</span></span>

<span data-ttu-id="84faf-142">Se a função for realizada com sucesso, o valor de retorno será maior que zero.</span><span class="sxs-lookup"><span data-stu-id="84faf-142">If the function succeeds, the return value is greater than zero.</span></span> <span data-ttu-id="84faf-143">Se a função falhar ou não tiver suporte, o valor de retorno será menor ou igual a zero.</span><span class="sxs-lookup"><span data-stu-id="84faf-143">If the function fails or is not supported, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="84faf-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="84faf-144">Remarks</span></span>

<span data-ttu-id="84faf-145">Esse escape é suportado por MXDC e XPSDrv, mas não pela GDI.</span><span class="sxs-lookup"><span data-stu-id="84faf-145">This escape is supported by MXDC and XPSDrv, but not by GDI.</span></span>

<span data-ttu-id="84faf-146">Para determinar se o driver de impressora é o MXDC, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o escape [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="84faf-146">To determine if the printer driver is the MXDC, call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="84faf-147">Se o driver for o MXDC, o **ExtEscape** retornará a cadeia de caracteres com terminação zero, " http://schemas.microsoft.com/xps/2005/06 ".</span><span class="sxs-lookup"><span data-stu-id="84faf-147">If the driver is the MXDC, the **ExtEscape** will return the zero-terminated string, "http://schemas.microsoft.com/xps/2005/06".</span></span> <span data-ttu-id="84faf-148">Verifique se o buffer referenciado pelo parâmetro *lpszOutData* é grande o suficiente para conter essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="84faf-148">Be sure the buffer referenced by the *lpszOutData* parameter is large enough to hold this string.</span></span>

<span data-ttu-id="84faf-149">Para determinar se o driver de impressora é o driver do gravador de documentos XPS da Microsoft para Windows, confirme se o driver de impressora é o MXDC e, em seguida, determine se o nome do driver de impressora é "Microsoft XPS Document Writer".</span><span class="sxs-lookup"><span data-stu-id="84faf-149">To determine if the printer driver is the Windows in-box Microsoft XPS Document Writer driver, confirm that the printer driver is the MXDC, and then determine whether the name of the printer driver is "Microsoft XPS Document Writer".</span></span>

<span data-ttu-id="84faf-150">Para obter o nome do driver de impressora, use uma das técnicas a seguir.</span><span class="sxs-lookup"><span data-stu-id="84faf-150">To get the printer driver name, use one of the following techniques.</span></span> <dl> <span data-ttu-id="84faf-151">Chame [**GetPrinterDriver**](getprinterdriver.md) com o valor do parâmetro *Level* definido como 1.</span><span class="sxs-lookup"><span data-stu-id="84faf-151">Call [**GetPrinterDriver**](getprinterdriver.md) with the *Level* parameter value set to 1.</span></span> <span data-ttu-id="84faf-152">O nome do driver de impressora é retornado no membro **pname** da [**estrutura \_ info \_ do driver 1**](driver-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="84faf-152">The printer driver name is returned in the **pName** member of the [**DRIVER\_INFO\_1**](driver-info-1.md) structure.</span></span>  
<span data-ttu-id="84faf-153">ou</span><span class="sxs-lookup"><span data-stu-id="84faf-153">or</span></span>  
<span data-ttu-id="84faf-154">Chame [**Getprinter**](getprinter.md) com o valor do parâmetro *Level* definido como 2.</span><span class="sxs-lookup"><span data-stu-id="84faf-154">Call [**GetPrinter**](getprinter.md) with the *Level* parameter value set to 2.</span></span> <span data-ttu-id="84faf-155">O nome do driver de impressora é retornado no membro **pDriverName** da [**estrutura \_ info \_ 2 da impressora**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="84faf-155">The printer driver name is returned in the **pDriverName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>  
</dl>

<span data-ttu-id="84faf-156">A tabela a seguir mostra onde encontrar vários objetos no arquivo XPS que vários tipos de objetos serão gravados.</span><span class="sxs-lookup"><span data-stu-id="84faf-156">The following table shows where to find various objects in the XPS file various types of objects will be written.</span></span>



| <span data-ttu-id="84faf-157">Objeto</span><span class="sxs-lookup"><span data-stu-id="84faf-157">Object</span></span>       | <span data-ttu-id="84faf-158">Local no arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="84faf-158">Location in the output file</span></span>    |
|--------------|--------------------------------|
| <span data-ttu-id="84faf-159">Página fixa</span><span class="sxs-lookup"><span data-stu-id="84faf-159">Fixed Page</span></span>   | <span data-ttu-id="84faf-160">/Documents/1/Pages/Esc%d.fpage</span><span class="sxs-lookup"><span data-stu-id="84faf-160">/Documents/1/Pages/Esc%d.fpage</span></span> |
| <span data-ttu-id="84faf-161">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="84faf-161">Thumbnail</span></span>    | <span data-ttu-id="84faf-162">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="84faf-162">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="84faf-163">Tíquete de impressão</span><span class="sxs-lookup"><span data-stu-id="84faf-163">Print Ticket</span></span> | <span data-ttu-id="84faf-164">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="84faf-164">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="84faf-165">Fonte</span><span class="sxs-lookup"><span data-stu-id="84faf-165">Font</span></span>         | <span data-ttu-id="84faf-166">/Documents/1/Resources/Fonts</span><span class="sxs-lookup"><span data-stu-id="84faf-166">/Documents/1/Resources/Fonts</span></span>   |
| <span data-ttu-id="84faf-167">Imagem</span><span class="sxs-lookup"><span data-stu-id="84faf-167">Image</span></span>        | <span data-ttu-id="84faf-168">/Documents/1/Resources/Images</span><span class="sxs-lookup"><span data-stu-id="84faf-168">/Documents/1/Resources/Images</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="84faf-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84faf-169">Requirements</span></span>



| <span data-ttu-id="84faf-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="84faf-170">Requirement</span></span> | <span data-ttu-id="84faf-171">Valor</span><span class="sxs-lookup"><span data-stu-id="84faf-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="84faf-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84faf-172">Minimum supported client</span></span><br/> | <span data-ttu-id="84faf-173">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84faf-173">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="84faf-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84faf-174">Minimum supported server</span></span><br/> | <span data-ttu-id="84faf-175">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84faf-175">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="84faf-176">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84faf-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="84faf-177"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="84faf-177"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84faf-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="84faf-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84faf-179">Impressão</span><span class="sxs-lookup"><span data-stu-id="84faf-179">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

<span data-ttu-id="84faf-180">[Funções de escape de impressora](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84faf-180">[Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84faf-181">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="84faf-181">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

