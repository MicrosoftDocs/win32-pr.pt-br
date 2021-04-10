---
description: Essas constantes definem valores que especificam o tipo de objetos IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Tipos de nó de contexto (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089704"
---
# <a name="context-node-types"></a><span data-ttu-id="78000-103">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="78000-103">Context Node Types</span></span>

<span data-ttu-id="78000-104">Essas constantes definem valores que especificam o tipo de objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="78000-104">These constants define values that specify the type of [**IContextNode**](icontextnode.md) objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="78000-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="78000-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="78000-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="78000-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <span data-ttu-id="78000-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(ANALYSISHINT)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-108">Representa um nó que contém informações adicionais de contexto para uma região que o <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> usa para melhorar sua análise.</span><span class="sxs-lookup"><span data-stu-id="78000-108">Represents a node that contains additional context information for a region that the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> uses to improve its analysis.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <span data-ttu-id="78000-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CUSTOMRECOGNIZER)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CustomRecognizer)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-110">Representa um nó usado para uma única operação de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="78000-110">Represents a node used for a single recognition operation.</span></span><br/> <span data-ttu-id="78000-111">Todos os traços e nós que estão dentro de um nó de reconhecedor personalizado são reconhecidos por uma operação de reconhecimento independente e não são analisados pelo <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="78000-111">All strokes and nodes that are within a custom recognizer node are recognized by an independent recognition operation and are not analyzed by the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span></span><br/> <span data-ttu-id="78000-112">Um nó de reconhecedor personalizado deve ser o filho direto do nó raiz do analisador de tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-112">A custom recognizer node must be the direct child of ink analyzer's root node.</span></span><br/> <span data-ttu-id="78000-113">Um nó de reconhecedor personalizado pode conter os seguintes tipos de elementos filho:</span><span class="sxs-lookup"><span data-stu-id="78000-113">A custom recognizer node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="78000-114">Qualquer número de nós UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="78000-114">Any number of UnclassifiedInk nodes.</span></span></li>
<li><span data-ttu-id="78000-115">Qualquer número de nós de objeto.</span><span class="sxs-lookup"><span data-stu-id="78000-115">Any number of Object nodes.</span></span></li>
<li><span data-ttu-id="78000-116">Qualquer número de nós de linha.</span><span class="sxs-lookup"><span data-stu-id="78000-116">Any number of Line nodes.</span></span></li>
<li><span data-ttu-id="78000-117">Qualquer número de nós InkWord.</span><span class="sxs-lookup"><span data-stu-id="78000-117">Any number of InkWord nodes.</span></span></li>
<li><span data-ttu-id="78000-118">Qualquer número de nós com um valor de GUID desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78000-118">Any number of nodes with an unknown Guid value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <span data-ttu-id="78000-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(imagem)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Image)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-120">Representa um nó para uma região bidimensional em que qualquer imagem que não seja de tinta pode existir no documento.</span><span class="sxs-lookup"><span data-stu-id="78000-120">Represents a node for a two-dimensional region where any non-ink images can exist in the document.</span></span><br/> <span data-ttu-id="78000-121">O <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> não produz nós de imagem.</span><span class="sxs-lookup"><span data-stu-id="78000-121">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce image nodes.</span></span> <span data-ttu-id="78000-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para adicionar um nó de imagem à árvore de nós de contexto.</span><span class="sxs-lookup"><span data-stu-id="78000-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add an image node to the context node tree.</span></span> <span data-ttu-id="78000-123">Em seguida, o <strong>IInkAnalyzer</strong> usa as regiões definidas pelo nó de imagem para determinar se alguma tinta anota a imagem que não é de tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-123">The <strong>IInkAnalyzer</strong> then uses the regions defined by the image node to determine if any ink annotates the non-ink image.</span></span><br/> <span data-ttu-id="78000-124">Um nó de imagem não pode ter nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="78000-124">An image node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <span data-ttu-id="78000-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(INKBULLET)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-126">O InkBullet ContextNodeType representa uma coleção de traços que compõem um marcador em uma lista com marcadores.</span><span class="sxs-lookup"><span data-stu-id="78000-126">The InkBullet ContextNodeType represents a collection of strokes that make up a bullet in a bulleted list.</span></span><br/> <span data-ttu-id="78000-127">Um ContextNode do tipo InkBullet não pode ter filhos.</span><span class="sxs-lookup"><span data-stu-id="78000-127">A ContextNode of type InkBullet cannot have any children.</span></span> <span data-ttu-id="78000-128">Só pode ser um filho de um parágrafo ContextNode.</span><span class="sxs-lookup"><span data-stu-id="78000-128">It can only be a child of a Paragraph ContextNode.</span></span> <span data-ttu-id="78000-129">Somente um InkBullet pode aparecer em um único parágrafo ContextNode.</span><span class="sxs-lookup"><span data-stu-id="78000-129">Only one InkBullet can appear in a single Paragraph ContextNode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <span data-ttu-id="78000-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(INKDRAWING)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-131">Representa um nó para uma coleção de traços que constitui um desenho.</span><span class="sxs-lookup"><span data-stu-id="78000-131">Represents a node for a collection of strokes that constitutes a drawing.</span></span><br/> <span data-ttu-id="78000-132">Os desenhos são traços que são determinados como formas ou esboços abstratos.</span><span class="sxs-lookup"><span data-stu-id="78000-132">Drawings are strokes that are determined to be shapes or abstract sketches.</span></span> <span data-ttu-id="78000-133">Geralmente, eles são traços que não são classificados como traços de escrita.</span><span class="sxs-lookup"><span data-stu-id="78000-133">They are generally any strokes that are not classified as writing strokes.</span></span><br/> <span data-ttu-id="78000-134">Um nó de desenho de tinta não pode ter nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="78000-134">An ink drawing node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <span data-ttu-id="78000-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(INKWORD)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-136">Representa um nó para uma coleção de traços que constitui um agrupamento lógico para formar uma palavra reconhecível.</span><span class="sxs-lookup"><span data-stu-id="78000-136">Represents a node for a collection of strokes that constitutes a logical grouping to form a recognizable word.</span></span><br/> <span data-ttu-id="78000-137">Um nó de palavra à tinta não pode conter nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="78000-137">An ink word node cannot contain any child elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <span data-ttu-id="78000-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(linha)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Line)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-139">Representa um nó para uma linha de palavras.</span><span class="sxs-lookup"><span data-stu-id="78000-139">Represents a node for a line of words.</span></span><br/> <span data-ttu-id="78000-140">Um nó de linha pode conter os seguintes tipos de elementos filho:</span><span class="sxs-lookup"><span data-stu-id="78000-140">A line node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="78000-141">Qualquer número de nós de palavras de tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-141">Any number of ink word nodes.</span></span></li>
<li><span data-ttu-id="78000-142">Qualquer número de nós da palavra de texto.</span><span class="sxs-lookup"><span data-stu-id="78000-142">Any number of text word nodes.</span></span></li>
<li><span data-ttu-id="78000-143">Qualquer número de nós com um valor de <strong>GUID</strong> desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78000-143">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <span data-ttu-id="78000-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(objeto)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Object)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-145">Representa um nó para um objeto que é retornado de um &quot; &quot; reconhecedor personalizado de objeto.</span><span class="sxs-lookup"><span data-stu-id="78000-145">Represents a node for an object that is returned from an &quot;object&quot; custom recognizer.</span></span><br/> <span data-ttu-id="78000-146">Um nó de objeto não pode conter nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="78000-146">An object node cannot contain any child elements.</span></span><br/> <span data-ttu-id="78000-147">Somente nós de reconhecedor personalizados podem conter nós de objeto.</span><span class="sxs-lookup"><span data-stu-id="78000-147">Only custom recognizer nodes can contain object nodes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <span data-ttu-id="78000-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(parágrafo)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Paragraph)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-149">Representa um nó para uma coleção de nós que constitui um agrupamento lógico de linhas.</span><span class="sxs-lookup"><span data-stu-id="78000-149">Represents a node for a collection of nodes that constitutes a logical grouping of lines.</span></span><br/> <span data-ttu-id="78000-150">A definição exata de um parágrafo é determinada pelos mecanismos de análise.</span><span class="sxs-lookup"><span data-stu-id="78000-150">The exact definition of a paragraph is determined by the analyzing engines.</span></span> <span data-ttu-id="78000-151">Em geral, um parágrafo contém grupos de linhas que podem fluir juntos se a caixa que contém as linhas fosse redimensionada.</span><span class="sxs-lookup"><span data-stu-id="78000-151">In general, a paragraph contains groups of lines that would reflow together if the box that contains the lines were resized.</span></span><br/> <span data-ttu-id="78000-152">Um nó de parágrafo pode conter os seguintes tipos de elementos filho:</span><span class="sxs-lookup"><span data-stu-id="78000-152">A paragraph node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="78000-153">Qualquer número de nós de marcador de tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-153">Any number of ink bullet nodes.</span></span></li>
<li><span data-ttu-id="78000-154">Qualquer número de nós de linha.</span><span class="sxs-lookup"><span data-stu-id="78000-154">Any number of line nodes.</span></span></li>
<li><span data-ttu-id="78000-155">Qualquer número de nós com um valor de <strong>GUID</strong> desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78000-155">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <span data-ttu-id="78000-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(raiz)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(Root)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-157">Representa um nó para o nó superior de uma árvore de nós que descreve os resultados da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-157">Represents a node for the top node of a tree of nodes that describe the results of ink analysis.</span></span><br/> <span data-ttu-id="78000-158">Nós raiz geralmente são obtidos do método de <a href="iinkanalyzer-getrootnode.md"><strong>método IInkAnalyzer:: GetRootNode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="78000-158">Root nodes are generally obtained from the <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode Method</strong></a> method.</span></span><br/> <span data-ttu-id="78000-159">Um nó raiz pode conter os seguintes tipos de elementos filho:</span><span class="sxs-lookup"><span data-stu-id="78000-159">A root node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="78000-160">Qualquer número de nós de dica de análise.</span><span class="sxs-lookup"><span data-stu-id="78000-160">Any number of analysis hint nodes.</span></span></li>
<li><span data-ttu-id="78000-161">Qualquer número de nós de reconhecedor personalizados.</span><span class="sxs-lookup"><span data-stu-id="78000-161">Any number of custom recognizer nodes.</span></span></li>
<li><span data-ttu-id="78000-162">Qualquer número de nós de imagem.</span><span class="sxs-lookup"><span data-stu-id="78000-162">Any number of image nodes.</span></span></li>
<li><span data-ttu-id="78000-163">Qualquer número de nós de desenho de tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-163">Any number of ink drawing nodes.</span></span></li>
<li><span data-ttu-id="78000-164">Qualquer número de nós de região de gravação.</span><span class="sxs-lookup"><span data-stu-id="78000-164">Any number of writing region nodes.</span></span></li>
<li><span data-ttu-id="78000-165">Qualquer número de nós de tinta não classificados.</span><span class="sxs-lookup"><span data-stu-id="78000-165">Any number of unclassified ink nodes.</span></span></li>
<li><span data-ttu-id="78000-166">Qualquer número de nós com um valor de <strong>GUID</strong> desconhecido.</span><span class="sxs-lookup"><span data-stu-id="78000-166">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <span data-ttu-id="78000-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(textword)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TextWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-168">Representa um nó para a região bidimensional em que qualquer texto que não seja de tinta pode existir no documento.</span><span class="sxs-lookup"><span data-stu-id="78000-168">Represents a node for the two-dimensional region where any non-ink text can exist in the document.</span></span><br/> <span data-ttu-id="78000-169">O <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> não produz os nós da palavra de texto.</span><span class="sxs-lookup"><span data-stu-id="78000-169">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce text word nodes.</span></span> <span data-ttu-id="78000-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para adicionar um nó de texto da palavra à árvore de nós de contexto.</span><span class="sxs-lookup"><span data-stu-id="78000-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add a text word node to the context node tree.</span></span> <span data-ttu-id="78000-171">Em seguida, o <strong>IInkAnalyzer</strong> usa as regiões definidas pelo nó texto da palavra para determinar se alguma tinta anota o texto não-à tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-171">The <strong>IInkAnalyzer</strong> then uses the regions defined by the text word node to determine if any ink annotates the non-ink text.</span></span><br/> <span data-ttu-id="78000-172">Os reconhecedores futuros podem usar a região definida por um nó de palavra de texto para determinar se alguma tinta anota a palavra que não é de tinta.</span><span class="sxs-lookup"><span data-stu-id="78000-172">Future recognizers may use the region defined by a text word node to determine if any ink annotates the non-ink word.</span></span><br/> <span data-ttu-id="78000-173">Um nó de palavra de texto não pode ter nenhum elemento filho</span><span class="sxs-lookup"><span data-stu-id="78000-173">A text word node cannot have any child elements</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <span data-ttu-id="78000-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span><span class="sxs-lookup"><span data-stu-id="78000-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78000-175">Representa um nó para todos os traços que ainda não foram classificados ou reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="78000-175">Represents a node for any strokes that have not yet been classified or recognized.</span></span><br/> <span data-ttu-id="78000-176">Um nó de tinta não classificado não pode ter nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="78000-176">An unclassified ink node cannot have any child elements.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="78000-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="78000-177">Remarks</span></span>

<span data-ttu-id="78000-178">Para obter mais informações sobre os diferentes tipos de nó de contexto, consulte [visão geral da análise de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="78000-178">For more information about the different context node types, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78000-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78000-179">Requirements</span></span>



| <span data-ttu-id="78000-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="78000-180">Requirement</span></span> | <span data-ttu-id="78000-181">Valor</span><span class="sxs-lookup"><span data-stu-id="78000-181">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78000-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78000-182">Minimum supported client</span></span><br/> | <span data-ttu-id="78000-183">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="78000-183">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="78000-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78000-184">Minimum supported server</span></span><br/> | <span data-ttu-id="78000-185">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="78000-185">None supported</span></span><br/>                                                           |
| <span data-ttu-id="78000-186">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78000-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="78000-187"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="78000-187"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78000-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="78000-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78000-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="78000-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="78000-190">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="78000-190">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="78000-191">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="78000-191">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="78000-192">**Método IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="78000-192">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="78000-193">**Método IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="78000-193">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="78000-194">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="78000-194">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="78000-195">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="78000-195">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="78000-196">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="78000-196">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="78000-197">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="78000-197">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




