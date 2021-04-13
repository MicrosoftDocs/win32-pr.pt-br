---
description: Erros de renderização
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Erros de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456753"
---
# <a name="rendering-errors"></a><span data-ttu-id="095f9-103">Erros de renderização</span><span class="sxs-lookup"><span data-stu-id="095f9-103">Rendering Errors</span></span>

> [!Note]  
> <span data-ttu-id="095f9-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="095f9-104">\[Deprecated.</span></span> <span data-ttu-id="095f9-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="095f9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="095f9-106">O Microsoft® DirectShow® a edição de serviços (DES) define vários códigos de erro usados para registrar erros de renderização.</span><span class="sxs-lookup"><span data-stu-id="095f9-106">Microsoft® DirectShow® Editing Services (DES) defines various error codes used to log rendering errors.</span></span> <span data-ttu-id="095f9-107">Se um projeto não for renderizado corretamente, o mecanismo de renderização chamará o método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="095f9-107">If a project does not render correctly, the render engine calls the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="095f9-108">A tabela a seguir resume os parâmetros fornecidos para **LogError**:</span><span class="sxs-lookup"><span data-stu-id="095f9-108">The following table summarizes the parameters given to **LogError**:</span></span>

-   <span data-ttu-id="095f9-109">O código de erro está contido no parâmetro *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="095f9-109">The error code is contained in the *ErrorCode* parameter.</span></span>
-   <span data-ttu-id="095f9-110">A descrição está contida no parâmetro ErrorString.</span><span class="sxs-lookup"><span data-stu-id="095f9-110">The description is contained in the ErrorString parameter.</span></span>
-   <span data-ttu-id="095f9-111">A descrição está contida no parâmetro *ErrorString* .</span><span class="sxs-lookup"><span data-stu-id="095f9-111">The description is contained in the *ErrorString* parameter.</span></span>
-   <span data-ttu-id="095f9-112">Se houver informações adicionais, o tipo **Variant** estará contido no membro **VT** da **variante** apontada por *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="095f9-112">If there is extra information, the **VARIANT** type is contained in the **vt** member of the **VARIANT** pointed to by *pExtraInfo*.</span></span>

> [!Note]  
> <span data-ttu-id="095f9-113">Os códigos de erro descritos aqui não são valores de **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="095f9-113">The error codes described here are not **HRESULT** values.</span></span> <span data-ttu-id="095f9-114">Para obter uma lista de valores de retorno de **HRESULT** específicos do des, consulte [códigos de erro e êxito](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="095f9-114">For a list of **HRESULT** return values specific to DES, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="095f9-115">Código do erro</span><span class="sxs-lookup"><span data-stu-id="095f9-115">Error code</span></span></th>
<th><span data-ttu-id="095f9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="095f9-116">Description</span></span></th>
<th><span data-ttu-id="095f9-117">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="095f9-117">Extra information</span></span></th>
<th><span data-ttu-id="095f9-118">Tipo de variante</span><span class="sxs-lookup"><span data-stu-id="095f9-118">Variant type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="095f9-119">DEX_IDS_BAD_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="095f9-119">DEX_IDS_BAD_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="095f9-120">O nome do arquivo não existe ou o DirectShow não reconhece a extensão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="095f9-120">File name doesn't exist, or DirectShow doesn't recognize the file extension.</span></span></td>
<td><span data-ttu-id="095f9-121">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="095f9-121">File name</span></span></td>
<td><span data-ttu-id="095f9-122"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-122"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-123">DEX_IDS_BAD_SOURCE_NAME2</span><span class="sxs-lookup"><span data-stu-id="095f9-123">DEX_IDS_BAD_SOURCE_NAME2</span></span></td>
<td><span data-ttu-id="095f9-124">O tipo de arquivo não corresponde à extensão do arquivo ou o arquivo está corrompido.</span><span class="sxs-lookup"><span data-stu-id="095f9-124">File type does not match the file extension or the file is corrupt.</span></span></td>
<td><span data-ttu-id="095f9-125">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="095f9-125">File name</span></span></td>
<td><span data-ttu-id="095f9-126"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-126"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-127">DEX_IDS_MISSING_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="095f9-127">DEX_IDS_MISSING_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="095f9-128">O nome do arquivo era necessário, mas não foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="095f9-128">File name was required, but wasn't given.</span></span></td>
<td><span data-ttu-id="095f9-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-129">None</span></span></td>
<td><span data-ttu-id="095f9-130">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-130">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-131">DEX_IDS_UNKNOWN_SOURCE</span><span class="sxs-lookup"><span data-stu-id="095f9-131">DEX_IDS_UNKNOWN_SOURCE</span></span></td>
<td><span data-ttu-id="095f9-132">Não é possível analisar a fonte de dados fornecida por essa fonte.</span><span class="sxs-lookup"><span data-stu-id="095f9-132">Cannot parse data source provided by this source.</span></span></td>
<td><span data-ttu-id="095f9-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-133">None</span></span></td>
<td><span data-ttu-id="095f9-134">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-134">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-135">DEX_IDS_INSTALL_PROBLEM</span><span class="sxs-lookup"><span data-stu-id="095f9-135">DEX_IDS_INSTALL_PROBLEM</span></span></td>
<td><span data-ttu-id="095f9-136">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="095f9-136">Unexpected error.</span></span> <span data-ttu-id="095f9-137">Algum componente do DirectShow não está instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="095f9-137">Some DirectShow component is not installed properly.</span></span></td>
<td><span data-ttu-id="095f9-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-138">None</span></span></td>
<td><span data-ttu-id="095f9-139">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-139">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-140">DEX_IDS_NO_SOURCE_NAMES</span><span class="sxs-lookup"><span data-stu-id="095f9-140">DEX_IDS_NO_SOURCE_NAMES</span></span></td>
<td><span data-ttu-id="095f9-141">O filtro de origem não aceita nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="095f9-141">Source filter does not accept file names.</span></span></td>
<td><span data-ttu-id="095f9-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-142">None</span></span></td>
<td><span data-ttu-id="095f9-143">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-143">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-144">DEX_IDS_BAD_MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="095f9-144">DEX_IDS_BAD_MEDIATYPE</span></span></td>
<td><span data-ttu-id="095f9-145">Não há suporte para o tipo de mídia do grupo.</span><span class="sxs-lookup"><span data-stu-id="095f9-145">Group's media type is not supported.</span></span></td>
<td><span data-ttu-id="095f9-146">Número do grupo</span><span class="sxs-lookup"><span data-stu-id="095f9-146">Group number</span></span></td>
<td><span data-ttu-id="095f9-147"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-147"><strong>int</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-148">DEX_IDS_STREAM_NUMBER</span><span class="sxs-lookup"><span data-stu-id="095f9-148">DEX_IDS_STREAM_NUMBER</span></span></td>
<td><span data-ttu-id="095f9-149">Número de fluxo inválido para esta fonte.</span><span class="sxs-lookup"><span data-stu-id="095f9-149">Invalid stream number for this source.</span></span></td>
<td><span data-ttu-id="095f9-150">Número do fluxo</span><span class="sxs-lookup"><span data-stu-id="095f9-150">Stream number</span></span></td>
<td><span data-ttu-id="095f9-151"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-151"><strong>int</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-152">DEX_IDS_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="095f9-152">DEX_IDS_OUTOFMEMORY</span></span></td>
<td><span data-ttu-id="095f9-153">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="095f9-153">Out of memory.</span></span></td>
<td><span data-ttu-id="095f9-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-154">None</span></span></td>
<td><span data-ttu-id="095f9-155">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-155">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-156">DEX_IDS_DIBSEQ_NOTALLSAME</span><span class="sxs-lookup"><span data-stu-id="095f9-156">DEX_IDS_DIBSEQ_NOTALLSAME</span></span></td>
<td><span data-ttu-id="095f9-157">Um bitmap na sequência não era o mesmo tipo que os outros.</span><span class="sxs-lookup"><span data-stu-id="095f9-157">One bitmap in the sequence was not the same type as the others.</span></span></td>
<td><span data-ttu-id="095f9-158">Nome do bitmap</span><span class="sxs-lookup"><span data-stu-id="095f9-158">Bitmap name</span></span></td>
<td><span data-ttu-id="095f9-159"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-159"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-160">DEX_IDS_CLIPTOOSHORT</span><span class="sxs-lookup"><span data-stu-id="095f9-160">DEX_IDS_CLIPTOOSHORT</span></span></td>
<td><span data-ttu-id="095f9-161">Os horários de mídia do clipe são inválidos ou a sequência de DIB (bitmap independente de dispositivo) é muito curta.</span><span class="sxs-lookup"><span data-stu-id="095f9-161">Clip's media times are invalid, or the device-independent bitmap (DIB) sequence is too short.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="095f9-162">Se outros erros de renderização ocorrerem, esse erro poderá ocorrer mesmo que os horários de mídia sejam válidos.</span><span class="sxs-lookup"><span data-stu-id="095f9-162">If other rendering errors occur, this error might occur even though the media times are valid.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="095f9-163">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-163">None</span></span></td>
<td><span data-ttu-id="095f9-164">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-164">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-165">DEX_IDS_INVALID_DXT</span><span class="sxs-lookup"><span data-stu-id="095f9-165">DEX_IDS_INVALID_DXT</span></span></td>
<td><span data-ttu-id="095f9-166">O CLSID (identificador de classe) do efeito ou da transição não é válido.</span><span class="sxs-lookup"><span data-stu-id="095f9-166">Class identifier (CLSID) of the effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="095f9-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="095f9-167">CLSID</span></span></td>
<td><span data-ttu-id="095f9-168"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-168"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-169">DEX_IDS_INVALID_DEFAULT_DXT</span><span class="sxs-lookup"><span data-stu-id="095f9-169">DEX_IDS_INVALID_DEFAULT_DXT</span></span></td>
<td><span data-ttu-id="095f9-170">O CLSID do efeito ou da transição padrão não é válido.</span><span class="sxs-lookup"><span data-stu-id="095f9-170">The CLSID of the default effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="095f9-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="095f9-171">CLSID</span></span></td>
<td><span data-ttu-id="095f9-172"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-172"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-173">DEX_IDS_NO_3D</span><span class="sxs-lookup"><span data-stu-id="095f9-173">DEX_IDS_NO_3D</span></span></td>
<td><span data-ttu-id="095f9-174">Sua versão do DirectX não oferece suporte a transições tridimensionais.</span><span class="sxs-lookup"><span data-stu-id="095f9-174">Your version of DirectX does not support three-dimensional transitions.</span></span></td>
<td><span data-ttu-id="095f9-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="095f9-175">CLSID</span></span></td>
<td><span data-ttu-id="095f9-176"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-176"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-177">DEX_IDS_BROKEN_DXT</span><span class="sxs-lookup"><span data-stu-id="095f9-177">DEX_IDS_BROKEN_DXT</span></span></td>
<td><span data-ttu-id="095f9-178">Esse efeito não é o tipo correto ou está quebrado.</span><span class="sxs-lookup"><span data-stu-id="095f9-178">This effect is not the right kind, or is broken.</span></span></td>
<td><span data-ttu-id="095f9-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="095f9-179">CLSID</span></span></td>
<td><span data-ttu-id="095f9-180"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-180"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-181">DEX_IDS_NO_SUCH_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="095f9-181">DEX_IDS_NO_SUCH_PROPERTY</span></span></td>
<td><span data-ttu-id="095f9-182">Essa propriedade não existe no objeto.</span><span class="sxs-lookup"><span data-stu-id="095f9-182">No such property exists on the object.</span></span></td>
<td><span data-ttu-id="095f9-183">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="095f9-183">Property name</span></span></td>
<td><span data-ttu-id="095f9-184"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-184"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span><span class="sxs-lookup"><span data-stu-id="095f9-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span></span></td>
<td><span data-ttu-id="095f9-186">Valor ilegal para esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="095f9-186">Illegal value for this property.</span></span></td>
<td><span data-ttu-id="095f9-187">Valor especificado</span><span class="sxs-lookup"><span data-stu-id="095f9-187">Value specified</span></span></td>
<td><span data-ttu-id="095f9-188"><strong>VARIANTE</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-188"><strong>VARIANT</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-189">DEX_IDS_INVALID_XML</span><span class="sxs-lookup"><span data-stu-id="095f9-189">DEX_IDS_INVALID_XML</span></span></td>
<td><span data-ttu-id="095f9-190">Erro de sintaxe no arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="095f9-190">Syntax error in XML file.</span></span></td>
<td><span data-ttu-id="095f9-191">Line number</span><span class="sxs-lookup"><span data-stu-id="095f9-191">Line number</span></span></td>
<td><span data-ttu-id="095f9-192">VT_I4 (inteiro de 4 bytes)</span><span class="sxs-lookup"><span data-stu-id="095f9-192">VT_I4 (4-byte integer)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-193">DEX_IDS_CANT_FIND_FILTER</span><span class="sxs-lookup"><span data-stu-id="095f9-193">DEX_IDS_CANT_FIND_FILTER</span></span></td>
<td><span data-ttu-id="095f9-194">Não é possível encontrar o filtro especificado em XML por categoria e instância.</span><span class="sxs-lookup"><span data-stu-id="095f9-194">Cannot find filter specified in XML by category and instance.</span></span></td>
<td><span data-ttu-id="095f9-195">Nome amigável (instância)</span><span class="sxs-lookup"><span data-stu-id="095f9-195">Friendly name (instance)</span></span></td>
<td><span data-ttu-id="095f9-196"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-196"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-197">DEX_IDS_DISK_WRITE_ERROR</span><span class="sxs-lookup"><span data-stu-id="095f9-197">DEX_IDS_DISK_WRITE_ERROR</span></span></td>
<td><span data-ttu-id="095f9-198">Erro ao gravar arquivo XML em disco.</span><span class="sxs-lookup"><span data-stu-id="095f9-198">Error writing XML file to disk.</span></span></td>
<td><span data-ttu-id="095f9-199">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-199">None</span></span></td>
<td><span data-ttu-id="095f9-200">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-200">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="095f9-201">DEX_IDS_INVALID_AUDIO_FX</span><span class="sxs-lookup"><span data-stu-id="095f9-201">DEX_IDS_INVALID_AUDIO_FX</span></span></td>
<td><span data-ttu-id="095f9-202">CLSID não é um filtro de efeito de áudio do DirectShow válido.</span><span class="sxs-lookup"><span data-stu-id="095f9-202">CLSID not a valid DirectShow audio effect filter.</span></span></td>
<td><span data-ttu-id="095f9-203">CLSID</span><span class="sxs-lookup"><span data-stu-id="095f9-203">CLSID</span></span></td>
<td><span data-ttu-id="095f9-204"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-204"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="095f9-205">DEX_IDS_CANT_FIND_COMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="095f9-205">DEX_IDS_CANT_FIND_COMPRESSOR</span></span></td>
<td><span data-ttu-id="095f9-206">Não é possível encontrar um compressor para produzir o formato de compactação especificado.</span><span class="sxs-lookup"><span data-stu-id="095f9-206">Cannot find a compressor to produce the specified compression format.</span></span></td>
<td><span data-ttu-id="095f9-207">Nenhum</span><span class="sxs-lookup"><span data-stu-id="095f9-207">None</span></span></td>
<td><span data-ttu-id="095f9-208">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="095f9-208">Not applicable</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="095f9-209">Os erros a seguir nunca devem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="095f9-209">The following errors should never occur.</span></span> <span data-ttu-id="095f9-210">Se você encontrar um desses erros, envie um relatório de bugs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="095f9-210">If you encounter one of these errors, please send a bug report to Microsoft.</span></span>



| <span data-ttu-id="095f9-211">Código do erro</span><span class="sxs-lookup"><span data-stu-id="095f9-211">Error code</span></span>                 | <span data-ttu-id="095f9-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="095f9-212">Description</span></span>                                 |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="095f9-213">DEX \_ IDs de \_ linha do tempo \_ análise</span><span class="sxs-lookup"><span data-stu-id="095f9-213">DEX\_IDS\_TIMELINE\_PARSE</span></span>  | <span data-ttu-id="095f9-214">Erro inesperado ao analisar a linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="095f9-214">Unexpected error parsing the timeline.</span></span>      |
| <span data-ttu-id="095f9-215">\_erro de \_ grafo de IDs Dex \_</span><span class="sxs-lookup"><span data-stu-id="095f9-215">DEX\_IDS\_GRAPH\_ERROR</span></span>     | <span data-ttu-id="095f9-216">Erro inesperado ao criar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="095f9-216">Unexpected error building the filter graph.</span></span> |
| <span data-ttu-id="095f9-217">\_erro de \_ grade de IDs Dex \_</span><span class="sxs-lookup"><span data-stu-id="095f9-217">DEX\_IDS\_GRID\_ERROR</span></span>      | <span data-ttu-id="095f9-218">Erro inesperado com a grade interna.</span><span class="sxs-lookup"><span data-stu-id="095f9-218">Unexpected error with the internal grid.</span></span>    |
| <span data-ttu-id="095f9-219">\_erro de \_ interface de IDs Dex \_</span><span class="sxs-lookup"><span data-stu-id="095f9-219">DEX\_IDS\_INTERFACE\_ERROR</span></span> | <span data-ttu-id="095f9-220">Erro inesperado ao obter uma interface.</span><span class="sxs-lookup"><span data-stu-id="095f9-220">Unexpected error getting an interface.</span></span>      |



 

 

 




