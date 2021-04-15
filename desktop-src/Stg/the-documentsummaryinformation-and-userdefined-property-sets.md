---
title: Os conjuntos de propriedades DocumentSummaryInformation e UserDefined
description: Um conjunto de propriedades DocumentSummaryInformation e UserDefined é uma extensão para o conjunto de propriedades de informações resumidas. Os dois conjuntos de propriedades podem existir simultaneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Conjuntos de propriedades UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498688"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a><span data-ttu-id="5189a-106">Os conjuntos de propriedades DocumentSummaryInformation e UserDefined</span><span class="sxs-lookup"><span data-stu-id="5189a-106">The DocumentSummaryInformation and UserDefined Property Sets</span></span>

<span data-ttu-id="5189a-107">Um conjunto de propriedades **DocumentSummaryInformation** **e UserDefined** é uma extensão para [o conjunto de propriedades de informações resumidas](the-summary-information-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="5189a-107">A **DocumentSummaryInformation** and **UserDefined** property set is an extension to [the Summary Information property set](the-summary-information-property-set.md).</span></span> <span data-ttu-id="5189a-108">Os dois conjuntos de propriedades podem existir simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="5189a-108">Both property sets can exist simultaneously.</span></span>

<span data-ttu-id="5189a-109">O nome do fluxo que contém o conjunto de propriedades **DocumentSummaryInformation** é **" \\ 005DocumentSummaryInformation"**.</span><span class="sxs-lookup"><span data-stu-id="5189a-109">The name of the stream that contains the **DocumentSummaryInformation** property set is **"\\005DocumentSummaryInformation"**.</span></span> <span data-ttu-id="5189a-110">O identificador de formato (FMTID) para o conjunto de propriedades **DocumentSummaryInformation** é **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="5189a-110">The format identifier (FMTID) for the **DocumentSummaryInformation** property set is **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="5189a-111">A declaração para esse valor está disponível nos arquivos de cabeçalho fornecidos como **FMTID \_ DocSummaryInformation**.</span><span class="sxs-lookup"><span data-stu-id="5189a-111">The declaration for this value is available in the provided header files as **FMTID\_DocSummaryInformation**.</span></span> <span data-ttu-id="5189a-112">Para obter mais informações, consulte [nomes em IStorage](names-in-istorage.md), [o resumo de propriedades de informações de resumido](the-summary-information-property-set.md), [**IPropertySetStorage:: criar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [Formatar identificadores](format-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="5189a-112">For more information, see [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).</span></span>

<span data-ttu-id="5189a-113">Esse fluxo também tem uma seção separada para as propriedades definidas pelo usuário personalizado, como nos conjuntos de propriedades **DocumentSummaryInformation** **e UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="5189a-113">This stream also has a separate section for the custom-user-defined properties as in the **DocumentSummaryInformation** and **UserDefined** property sets.</span></span> <span data-ttu-id="5189a-114">Esta seção aparece na interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) como um conjunto de propriedades separado, com o seguinte FMTID (disponível como **FMTID \_ userdefineproperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="5189a-114">This section appears in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface as a separate property set, with the following FMTID (available as **FMTID\_UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="5189a-115">Esses dois conjuntos de propriedades são os únicos para os quais um único fluxo pode conter vários conjuntos de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5189a-115">These two property sets are the only ones for which a single stream can hold multiple property sets.</span></span> <span data-ttu-id="5189a-116">O fato de que esses dois conjuntos de propriedades estão em um único fluxo afeta o comportamento da interface **IPropertySetStorage** .</span><span class="sxs-lookup"><span data-stu-id="5189a-116">The fact that these two property sets are in a single stream affects the behavior of the **IPropertySetStorage** interface.</span></span> <span data-ttu-id="5189a-117">Para obter mais informações, consulte [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span><span class="sxs-lookup"><span data-stu-id="5189a-117">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

<span data-ttu-id="5189a-118">A tabela a seguir lista as propriedades adicionadas ao conjunto **de propriedades** **DocumentSummaryInformation** e UserDefined.</span><span class="sxs-lookup"><span data-stu-id="5189a-118">The following table lists the added properties to the **DocumentSummaryInformation** and **UserDefined** property set.</span></span> <span data-ttu-id="5189a-119">Como no conjunto de propriedades **SummaryInformation** , os nomes normalmente não são armazenados no conjunto de propriedades, mas são inferidos do identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5189a-119">As in the **SummaryInformation** property set, the names are not typically stored in the property set, but are inferred from the property identifier.</span></span>



| <span data-ttu-id="5189a-120">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="5189a-120">Property name</span></span>      | <span data-ttu-id="5189a-121">Identificador de propriedade</span><span class="sxs-lookup"><span data-stu-id="5189a-121">Property identifier</span></span>     | <span data-ttu-id="5189a-122">Valor do identificador de propriedade</span><span class="sxs-lookup"><span data-stu-id="5189a-122">Property identifier value</span></span> | <span data-ttu-id="5189a-123">Tipo de variante</span><span class="sxs-lookup"><span data-stu-id="5189a-123">VARIANT type</span></span>                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| <span data-ttu-id="5189a-124">Categoria</span><span class="sxs-lookup"><span data-stu-id="5189a-124">Category</span></span>           | <span data-ttu-id="5189a-125">**\_categoria PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="5189a-125">**PIDDSI\_CATEGORY**</span></span>    | <span data-ttu-id="5189a-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5189a-126">0x00000002</span></span>                | <span data-ttu-id="5189a-127">**a VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="5189a-127">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="5189a-128">PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="5189a-128">PresentationTarget</span></span> | <span data-ttu-id="5189a-129">**PIDDSI \_ PRESFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5189a-129">**PIDDSI\_PRESFORMAT**</span></span>  | <span data-ttu-id="5189a-130">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5189a-130">0x00000003</span></span>                | <span data-ttu-id="5189a-131">**a VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="5189a-131">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="5189a-132">Bytes</span><span class="sxs-lookup"><span data-stu-id="5189a-132">Bytes</span></span>              | <span data-ttu-id="5189a-133">**BYTECOUNT do PIDDSI \_**</span><span class="sxs-lookup"><span data-stu-id="5189a-133">**PIDDSI\_BYTECOUNT**</span></span>   | <span data-ttu-id="5189a-134">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5189a-134">0x00000004</span></span>                | <span data-ttu-id="5189a-135">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="5189a-135">**VT\_I4**</span></span>                        |
| <span data-ttu-id="5189a-136">Linhas</span><span class="sxs-lookup"><span data-stu-id="5189a-136">Lines</span></span>              | <span data-ttu-id="5189a-137">**PIDDSI \_ LINECOUNT**</span><span class="sxs-lookup"><span data-stu-id="5189a-137">**PIDDSI\_LINECOUNT**</span></span>   | <span data-ttu-id="5189a-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="5189a-138">0x00000005</span></span>                | <span data-ttu-id="5189a-139">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="5189a-139">**VT\_I4**</span></span>                        |
| <span data-ttu-id="5189a-140">Parágrafos</span><span class="sxs-lookup"><span data-stu-id="5189a-140">Paragraphs</span></span>         | <span data-ttu-id="5189a-141">**PIDDSI \_ PARCOUNT**</span><span class="sxs-lookup"><span data-stu-id="5189a-141">**PIDDSI\_PARCOUNT**</span></span>    | <span data-ttu-id="5189a-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="5189a-142">0x00000006</span></span>                | <span data-ttu-id="5189a-143">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="5189a-143">**VT\_I4**</span></span>                        |
| <span data-ttu-id="5189a-144">Slides</span><span class="sxs-lookup"><span data-stu-id="5189a-144">Slides</span></span>             | <span data-ttu-id="5189a-145">**PIDDSI \_ SLIDECOUNT**</span><span class="sxs-lookup"><span data-stu-id="5189a-145">**PIDDSI\_SLIDECOUNT**</span></span>  | <span data-ttu-id="5189a-146">0x00000007</span><span class="sxs-lookup"><span data-stu-id="5189a-146">0x00000007</span></span>                | <span data-ttu-id="5189a-147">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="5189a-147">**VT\_I4**</span></span>                        |
| <span data-ttu-id="5189a-148">Observações</span><span class="sxs-lookup"><span data-stu-id="5189a-148">Notes</span></span>              | <span data-ttu-id="5189a-149">**PIDDSI \_ NOTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="5189a-149">**PIDDSI\_NOTECOUNT**</span></span>   | <span data-ttu-id="5189a-150">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5189a-150">0x00000008</span></span>                | <span data-ttu-id="5189a-151">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="5189a-151">**VT\_I4**</span></span>                        |
| <span data-ttu-id="5189a-152">HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="5189a-152">HiddenSlides</span></span>       | <span data-ttu-id="5189a-153">**PIDDSI \_ HIDDENCOUNT**</span><span class="sxs-lookup"><span data-stu-id="5189a-153">**PIDDSI\_HIDDENCOUNT**</span></span> | <span data-ttu-id="5189a-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="5189a-154">0x00000009</span></span>                | <span data-ttu-id="5189a-155">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="5189a-155">**VT\_I4**</span></span>                        |
| <span data-ttu-id="5189a-156">MMClips</span><span class="sxs-lookup"><span data-stu-id="5189a-156">MMClips</span></span>            | <span data-ttu-id="5189a-157">**PIDDSI \_ MMCLIPCOUNT**</span><span class="sxs-lookup"><span data-stu-id="5189a-157">**PIDDSI\_MMCLIPCOUNT**</span></span> | <span data-ttu-id="5189a-158">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="5189a-158">0x0000000A</span></span>                | <span data-ttu-id="5189a-159">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="5189a-159">**VT\_I4**</span></span>                        |
| <span data-ttu-id="5189a-160">ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="5189a-160">ScaleCrop</span></span>          | <span data-ttu-id="5189a-161">**escala de PIDDSI \_**</span><span class="sxs-lookup"><span data-stu-id="5189a-161">**PIDDSI\_SCALE**</span></span>       | <span data-ttu-id="5189a-162">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="5189a-162">0x0000000B</span></span>                | <span data-ttu-id="5189a-163">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="5189a-163">**VT\_BOOL**</span></span>                      |
| <span data-ttu-id="5189a-164">HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="5189a-164">HeadingPairs</span></span>       | <span data-ttu-id="5189a-165">**PIDDSI \_ HEADINGPAIR**</span><span class="sxs-lookup"><span data-stu-id="5189a-165">**PIDDSI\_HEADINGPAIR**</span></span> | <span data-ttu-id="5189a-166">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="5189a-166">0x0000000C</span></span>                | <span data-ttu-id="5189a-167">**VT \_** \| **\_ vetor VT** de variante</span><span class="sxs-lookup"><span data-stu-id="5189a-167">**VT\_VARIANT** \| **VT\_VECTOR**</span></span> |
| <span data-ttu-id="5189a-168">TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="5189a-168">TitlesofParts</span></span>      | <span data-ttu-id="5189a-169">**PIDDSI \_ DOCPARTS**</span><span class="sxs-lookup"><span data-stu-id="5189a-169">**PIDDSI\_DOCPARTS**</span></span>    | <span data-ttu-id="5189a-170">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="5189a-170">0x0000000D</span></span>                | <span data-ttu-id="5189a-171">**VT \_** \| **\_ LPSTR** de vetor VT</span><span class="sxs-lookup"><span data-stu-id="5189a-171">**VT\_VECTOR** \| **VT\_LPSTR**</span></span>   |
| <span data-ttu-id="5189a-172">Gerente</span><span class="sxs-lookup"><span data-stu-id="5189a-172">Manager</span></span>            | <span data-ttu-id="5189a-173">**Gerenciador de PIDDSI \_**</span><span class="sxs-lookup"><span data-stu-id="5189a-173">**PIDDSI\_MANAGER**</span></span>     | <span data-ttu-id="5189a-174">0x0000000E</span><span class="sxs-lookup"><span data-stu-id="5189a-174">0x0000000E</span></span>                | <span data-ttu-id="5189a-175">**a VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="5189a-175">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="5189a-176">Empresa</span><span class="sxs-lookup"><span data-stu-id="5189a-176">Company</span></span>            | <span data-ttu-id="5189a-177">**\_empresa PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="5189a-177">**PIDDSI\_COMPANY**</span></span>     | <span data-ttu-id="5189a-178">0x0000000F</span><span class="sxs-lookup"><span data-stu-id="5189a-178">0x0000000F</span></span>                | <span data-ttu-id="5189a-179">**a VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="5189a-179">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="5189a-180">LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="5189a-180">LinksUpToDate</span></span>      | <span data-ttu-id="5189a-181">**PIDDSI \_ LINKSDIRTY**</span><span class="sxs-lookup"><span data-stu-id="5189a-181">**PIDDSI\_LINKSDIRTY**</span></span>  | <span data-ttu-id="5189a-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5189a-182">0x00000010</span></span>                | <span data-ttu-id="5189a-183">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="5189a-183">**VT\_BOOL**</span></span>                      |



 

<span data-ttu-id="5189a-184">Essas propriedades têm os seguintes usos:</span><span class="sxs-lookup"><span data-stu-id="5189a-184">These properties have the following uses:</span></span>

<dl> <dt>

<span data-ttu-id="5189a-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias</span><span class="sxs-lookup"><span data-stu-id="5189a-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="5189a-186">Uma cadeia de texto digitada pelo usuário que indica a qual categoria o arquivo pertence (memorando, proposta e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="5189a-186">A text string typed by the user that indicates what category the file belongs to (memo, proposal, and so on).</span></span> <span data-ttu-id="5189a-187">É útil para localizar arquivos do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="5189a-187">It is useful for finding files of same type.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="5189a-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span></span>
</dt> <dd>

<span data-ttu-id="5189a-189">Formato de destino para apresentação (35mm, impressora, vídeo e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="5189a-189">Target format for presentation (35mm, printer, video, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="5189a-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span><span class="sxs-lookup"><span data-stu-id="5189a-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span></span>
</dt> <dd>

<span data-ttu-id="5189a-191">Quantidade de bytes.</span><span class="sxs-lookup"><span data-stu-id="5189a-191">Number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Alinha</span><span class="sxs-lookup"><span data-stu-id="5189a-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Lines</span></span>
</dt> <dd>

<span data-ttu-id="5189a-193">Número de linhas.</span><span class="sxs-lookup"><span data-stu-id="5189a-193">Number of lines.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Parágrafos</span><span class="sxs-lookup"><span data-stu-id="5189a-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragraphs</span></span>
</dt> <dd>

<span data-ttu-id="5189a-195">Número de parágrafos.</span><span class="sxs-lookup"><span data-stu-id="5189a-195">Number of paragraphs.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span><span class="sxs-lookup"><span data-stu-id="5189a-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span></span>
</dt> <dd>

<span data-ttu-id="5189a-197">Número de slides.</span><span class="sxs-lookup"><span data-stu-id="5189a-197">Number of slides.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Registra</span><span class="sxs-lookup"><span data-stu-id="5189a-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span></span>
</dt> <dd>

<span data-ttu-id="5189a-199">Número de páginas que contêm anotações.</span><span class="sxs-lookup"><span data-stu-id="5189a-199">Number of pages that contain notes.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="5189a-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span></span>
</dt> <dd>

<span data-ttu-id="5189a-201">Número de slides ocultos.</span><span class="sxs-lookup"><span data-stu-id="5189a-201">Number of slides that are hidden.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span><span class="sxs-lookup"><span data-stu-id="5189a-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span></span>
</dt> <dd>

<span data-ttu-id="5189a-203">Número de clipes de som ou de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5189a-203">Number of sound or video clips.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="5189a-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span></span>
</dt> <dd>

<span data-ttu-id="5189a-205">Defina como true (-1) quando o dimensionamento da miniatura for desejado.</span><span class="sxs-lookup"><span data-stu-id="5189a-205">Set to True (-1) when scaling of the thumbnail is desired.</span></span> <span data-ttu-id="5189a-206">Se não estiver definido, o corte será desejado.</span><span class="sxs-lookup"><span data-stu-id="5189a-206">If not set, cropping is desired.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="5189a-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span></span>
</dt> <dd>

<span data-ttu-id="5189a-208">Propriedade usada internamente indicando o agrupamento de diferentes partes do documento e o número de itens em cada grupo.</span><span class="sxs-lookup"><span data-stu-id="5189a-208">Internally used property indicating the grouping of different document parts and the number of items in each group.</span></span> <span data-ttu-id="5189a-209">Os títulos das partes do documento são armazenados na propriedade **TitlesofParts** .</span><span class="sxs-lookup"><span data-stu-id="5189a-209">The titles of the document parts are stored in the **TitlesofParts** property.</span></span> <span data-ttu-id="5189a-210">A propriedade **HeadingPairs** é armazenada como um vetor de variantes, em pares de repetição de **VT \_ LPSTR** (ou **VT \_ LPWSTR**) e valores de **\_ i4 VT** .</span><span class="sxs-lookup"><span data-stu-id="5189a-210">The **HeadingPairs** property is stored as a vector of variants, in repeating pairs of **VT\_LPSTR** (or **VT\_LPWSTR**) and **VT\_I4** values.</span></span> <span data-ttu-id="5189a-211">O valor de ' **VT \_ LPSTR** ' representa um nome de título e o valor de **\_ i4 de VT** indica a contagem de partes de documento sob esse título.</span><span class="sxs-lookup"><span data-stu-id="5189a-211">The **VT\_LPSTR** value represents a heading name, and the **VT\_I4** value indicates the count of document parts under that heading.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="5189a-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span></span>
</dt> <dd>

<span data-ttu-id="5189a-213">Nomes de partes do documento.</span><span class="sxs-lookup"><span data-stu-id="5189a-213">Names of document parts.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span><span class="sxs-lookup"><span data-stu-id="5189a-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span></span>
</dt> <dd>

<span data-ttu-id="5189a-215">Gerente do projeto.</span><span class="sxs-lookup"><span data-stu-id="5189a-215">Manager of the project.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Corporativa</span><span class="sxs-lookup"><span data-stu-id="5189a-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="5189a-217">Nome da empresa.</span><span class="sxs-lookup"><span data-stu-id="5189a-217">Company name.</span></span>

</dd> <dt>

<span data-ttu-id="5189a-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="5189a-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span></span>
</dt> <dd>

<span data-ttu-id="5189a-219">Valor booliano para indicar se os links personalizados são dificultados por ruído excessivo, para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5189a-219">Boolean value to indicate whether the custom links are hampered by excessive noise, for all applications.</span></span>

> [!Note]  
> <span data-ttu-id="5189a-220">Conforme descrito em 12,3.</span><span class="sxs-lookup"><span data-stu-id="5189a-220">As described in 12.3.</span></span> <span data-ttu-id="5189a-221">Formato serializado para conjuntos de propriedades da especificação de design de OLE 2,0, os elementos de vetor nas propriedades **HeadingPairs** e **TitlesofParts** devem ser alinhados em limites de bit 32 dentro do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5189a-221">Serialized Format for Property Sets of the OLE 2.0 Design Specification, vector elements in the **HeadingPairs** and **TitlesofParts** properties should be aligned on 32 bit boundaries within the property set.</span></span> <span data-ttu-id="5189a-222">No entanto, nos conjuntos de propriedades **DocumentSummaryInformation** **e UserDefined** , quando a página de código do conjunto de propriedades não é Unicode, esses elementos devem ser empacotados.</span><span class="sxs-lookup"><span data-stu-id="5189a-222">However, in the **DocumentSummaryInformation** and **UserDefined** property sets, when the code page of the property set is not Unicode, these elements must be packed.</span></span>

 

</dd> </dl>

<span data-ttu-id="5189a-223">O conjunto de propriedades **UserDefined** pode ser usado para manter qualquer propriedade.</span><span class="sxs-lookup"><span data-stu-id="5189a-223">The **UserDefined** property set can be used to hold any properties.</span></span> <span data-ttu-id="5189a-224">Normalmente, ele é usado para armazenar as propriedades nomeadas criadas por um usuário.</span><span class="sxs-lookup"><span data-stu-id="5189a-224">Typically, it is used to store named properties created by a user.</span></span>

 

 




