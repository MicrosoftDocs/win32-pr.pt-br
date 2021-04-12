---
description: Define os valores que especificam as propriedades de uma alternativa de reconhecimento. A API (interface de programação de aplicativo) do Tablet PC usa identificadores globais exclusivos (GUIDs) para identificar Propriedades de pacote, que na automação são cadeias de caracteres constantes.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Constantes rerecognitionproperty (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297376"
---
# <a name="recognitionproperty-constants"></a><span data-ttu-id="1a391-104">Constantes rerecognitionproperty</span><span class="sxs-lookup"><span data-stu-id="1a391-104">RecognitionProperty Constants</span></span>

<span data-ttu-id="1a391-105">Define os valores que especificam as propriedades de uma alternativa de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="1a391-105">Defines values that specify the properties of a recognition alternate.</span></span> <span data-ttu-id="1a391-106">A API (interface de programação de aplicativo) do Tablet PC usa identificadores globais exclusivos (GUIDs) para identificar Propriedades de pacote, que na automação são cadeias de caracteres constantes.</span><span class="sxs-lookup"><span data-stu-id="1a391-106">The Tablet PC application programming interface (API) uses globally unique identifiers (GUIDs) to identify packet properties, which in Automation are constant strings.</span></span>

<span data-ttu-id="1a391-107">A tabela a seguir lista os campos GUID (identificador global exclusivo) da propriedade alternativa de reconhecimento disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1a391-107">The following table lists the available recognition alternate property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="1a391-108">Use esses GUIDs para acessar as propriedades de um objeto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) chamando o método [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .</span><span class="sxs-lookup"><span data-stu-id="1a391-108">Use these GUIDs to access properties of an [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object by calling the [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) method.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1a391-109">Nome da constante</span><span class="sxs-lookup"><span data-stu-id="1a391-109">Constant Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1a391-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a391-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <span data-ttu-id="1a391-111"><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1a391-111"><dt> <strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1a391-112">O GUID que identifica a propriedade para o número de linha do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a391-112">The GUID that identifies the property for the line number of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="1a391-113">LineNumber especifica as alternativas com um número de linha específico.</span><span class="sxs-lookup"><span data-stu-id="1a391-113">LineNumber specifies the alternates with a particular line number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a391-114">Este campo não tem suporte para reconhecedores de caracteres do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="1a391-114">This field is not supported for recognizers of East Asian characters.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <span data-ttu-id="1a391-115"><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1a391-115"><dt> <strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1a391-116">O GUID que identifica a propriedade para a segmentação do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a391-116">The GUID that identifies the property for the segmentation of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="1a391-117">Segmentação especifica o fragmento de tinta básico ou a unidade que o reconhecedor usa para produzir um resultado de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="1a391-117">Segmentation specifies the basic ink fragment or unit that the recognizer uses to produce a recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a391-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="1a391-118">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <span data-ttu-id="1a391-119"><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1a391-119"><dt> <strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1a391-120">O GUID que identifica a propriedade para o ponto de acesso de reconhecimento do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a391-120">The GUID that identifies the property for the recognition hot point of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <span data-ttu-id="1a391-121"><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1a391-121"><dt> <strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1a391-122">O GUID que identifica a propriedade para a contagem máxima de traços do resultado de reconhecimento do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a391-122">The GUID that identifies the property for the maximum stroke count of the recognition result for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a391-123">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="1a391-123">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <span data-ttu-id="1a391-124"><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1a391-124"><dt> <strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1a391-125">O GUID que identifica a propriedade para a métrica de pontos por polegada do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a391-125">The GUID that identifies the property for the points-per-inch metric of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a391-126">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="1a391-126">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <span data-ttu-id="1a391-127"><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1a391-127"><dt> <strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1a391-128">O GUID que identifica a propriedade para o nível de confiança que o reconhecedor tem no resultado do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="1a391-128">The GUID that identifies the property for the level of confidence that the recognizer has in the recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a391-129">A avaliação de confiança está disponível apenas para o Estados Unidos Inglês e todos os reconhecedores de gestos no Microsoft Windows XP Tablet PC Edition e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1a391-129">Confidence evaluation is available only for United States English and all gesture recognizers in Microsoft Windows XP Tablet PC Edition and Windows Vista.</span></span> <span data-ttu-id="1a391-130">Métodos que fornecem a propriedade de confiança para qualquer outro reconhecedor retornam E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="1a391-130">Methods that provide the confidence property for any other recognizer return E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <span data-ttu-id="1a391-131"><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1a391-131"><dt> <strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1a391-132">O GUID que identifica a propriedade para as métricas de linha do objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> , que é a linha para a qual as métricas serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="1a391-132">The GUID that identifies the property for the line metrics of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object, which is the line for which to retrieve metrics.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="1a391-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a391-133">Remarks</span></span>

<span data-ttu-id="1a391-134">Em C++, você pode acessar essas constantes no arquivo de cabeçalho Msinkaut. h, que está localizado no <systemdrive> diretório: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ include se você instalou o SDK no local padrão.</span><span class="sxs-lookup"><span data-stu-id="1a391-134">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="1a391-135">Em C++, essas constantes são WCHARs, não BSTRs.</span><span class="sxs-lookup"><span data-stu-id="1a391-135">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="1a391-136">Converta-os em BSTRs antes de usar.</span><span class="sxs-lookup"><span data-stu-id="1a391-136">Convert them into BSTRs before use.</span></span> <span data-ttu-id="1a391-137">Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="1a391-137">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a391-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a391-138">Requirements</span></span>



| <span data-ttu-id="1a391-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a391-139">Requirement</span></span> | <span data-ttu-id="1a391-140">Valor</span><span class="sxs-lookup"><span data-stu-id="1a391-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a391-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a391-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1a391-142">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1a391-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1a391-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a391-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1a391-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1a391-144">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1a391-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a391-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a391-146"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1a391-146"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a391-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a391-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a391-148">**Método AlternatesWithConstantPropertyValues**</span><span class="sxs-lookup"><span data-stu-id="1a391-148">**AlternatesWithConstantPropertyValues Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[<span data-ttu-id="1a391-149">**Propriedade ConfidenceAlternates**</span><span class="sxs-lookup"><span data-stu-id="1a391-149">**ConfidenceAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[<span data-ttu-id="1a391-150">**Propriedade LineAlternates**</span><span class="sxs-lookup"><span data-stu-id="1a391-150">**LineAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[<span data-ttu-id="1a391-151">**Interface IInkRecognitionAlternates**</span><span class="sxs-lookup"><span data-stu-id="1a391-151">**IInkRecognitionAlternates Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




