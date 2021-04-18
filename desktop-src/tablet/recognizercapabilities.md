---
description: Especifica os atributos de um IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Enumeração RecognizerCapabilities (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786285"
---
# <a name="recognizercapabilities-enumeration"></a><span data-ttu-id="50bf6-103">Enumeração RecognizerCapabilities</span><span class="sxs-lookup"><span data-stu-id="50bf6-103">RecognizerCapabilities enumeration</span></span>

<span data-ttu-id="50bf6-104">Especifica os atributos de um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="50bf6-104">Specifies the attributes of an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50bf6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50bf6-105">Syntax</span></span>


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a><span data-ttu-id="50bf6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="50bf6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="50bf6-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="50bf6-107"><span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC\_None**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-108">Nenhum recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="50bf6-108">No capabilities specified.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**\_DONOTCARE RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-109"><span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC\_DoNotCare**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-110">Ignora todos os outros sinalizadores que estão definidos.</span><span class="sxs-lookup"><span data-stu-id="50bf6-110">Ignores all other flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**\_Objeto RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-111"><span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC\_Object**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-112">Dá suporte ao reconhecimento de objeto; caso contrário, o só reconhecerá o texto.</span><span class="sxs-lookup"><span data-stu-id="50bf6-112">Supports object recognition; otherwise, recognizes only text.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**\_FREEINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-113"><span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC\_FreeInput**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-114">Dá suporte à entrada gratuita, em que a tinta é inserida sem o uso de um guia de reconhecimento, como uma linha ou uma caixa.</span><span class="sxs-lookup"><span data-stu-id="50bf6-114">Supports free input, where ink is entered without the use of a recognition guide, such as a line or a box.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**\_LINEDINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-115"><span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC\_LinedInput**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-116">Dá suporte à entrada em linha, que é semelhante à escrita em papel embutido.</span><span class="sxs-lookup"><span data-stu-id="50bf6-116">Supports lined input, which is similar to writing on lined paper.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**\_BOXEDINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-117"><span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC\_BoxedInput**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-118">Dá suporte à entrada em caixa, em que cada caractere ou palavra é inserida em um box.</span><span class="sxs-lookup"><span data-stu-id="50bf6-118">Supports boxed input, where each character or word is entered in a box.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**\_CHARACTERAUTOCOMPLETIONINPUT RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-119"><span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC\_CharacterAutoCompletionInput**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-120">Dá suporte ao preenchimento automático de caracteres.</span><span class="sxs-lookup"><span data-stu-id="50bf6-120">Supports character Autocomplete.</span></span> <span data-ttu-id="50bf6-121">Os reconhecedores que dão suporte ao preenchimento automático de caracteres exigem entrada em caixa.</span><span class="sxs-lookup"><span data-stu-id="50bf6-121">Recognizers that support character Autocomplete require boxed input.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**\_RIGHTANDDOWN RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-122"><span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC\_RightAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-123">Dá suporte à entrada de manuscrito na ordem direita e abaixo, como em idiomas ocidentais e em alguns idiomas do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="50bf6-123">Supports handwriting input in right and down order, such as in western languages and some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**\_LEFTANDDOWN RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-124"><span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC\_LeftAndDown**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-125">Dá suporte à entrada de manuscrito em ordem esquerda e abaixo, como em idiomas hebraico e árabe.</span><span class="sxs-lookup"><span data-stu-id="50bf6-125">Supports handwriting input in left and down order, such as in Hebrew and Arabic languages.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**\_DOWNANDLEFT RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-126"><span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC\_DownAndLeft**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-127">Dá suporte à entrada de manuscrito na ordem inferior e esquerda, como em alguns idiomas do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="50bf6-127">Supports handwriting input in down and left order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**\_DOWNANDRIGHT RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-128"><span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC\_DownAndRight**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-129">Dá suporte à entrada de manuscrito na ordem inferior e direita, como em alguns idiomas do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="50bf6-129">Supports handwriting input in down and right order, such as in some East Asian languages.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**\_ARBITRARYANGLE RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-130"><span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC\_ArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-131">Dá suporte a texto escrito em ângulos arbitrários.</span><span class="sxs-lookup"><span data-stu-id="50bf6-131">Supports text written at arbitrary angles.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**\_Malha RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-132"><span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC\_Lattice**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-133">Dá suporte ao retorno de um malha como uma cadeia de caracteres alternativa para resultados de reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="50bf6-133">Supports returning a lattice as an alternative a string for handwriting recognition results.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**\_ADVISEINKCHANGE RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-134"><span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC\_AdviseInkChange**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-135">Dá suporte à interrupção do reconhecimento em segundo plano, como quando a tinta foi alterada.</span><span class="sxs-lookup"><span data-stu-id="50bf6-135">Supports interrupting background recognition, such as when the ink has changed.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**\_STROKEREORDER RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-136"><span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC\_StrokeReorder**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-137">Dá suporte a essa ordem de traço, espacial e temporal, é tratada como parte da operação de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="50bf6-137">Supports that stroke order, spatial and temporal, is handled as part of the recognition operation.</span></span> <span data-ttu-id="50bf6-138">O [**IInkAnalyzer**](iinkanalyzer.md) não reordena os traços antes de enviar tinta para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="50bf6-138">The [**IInkAnalyzer**](iinkanalyzer.md) does not reorder strokes before sending ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**A versão RC é \_ personalizável**</span><span class="sxs-lookup"><span data-stu-id="50bf6-139"><span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC\_Personalizable**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-140">Dá suporte a manuscrito personalizado, onde o reconhecedor melhora o reconhecimento quando exposto ao mesmo manuscrito ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="50bf6-140">Supports personalized handwriting, where the recognizer improves recognition when exposed to the same handwriting over time.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**\_PREFERSARBITRARYANGLE RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-141"><span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC\_PrefersArbitraryAngle**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-142">O [**IInkAnalyzer**](iinkanalyzer.md) não precisa girar o manuscrito para uma orientação horizontal antes de enviar a tinta para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="50bf6-142">The [**IInkAnalyzer**](iinkanalyzer.md) need not rotate the handwriting to a horizontal orientation before sending the ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**\_PREFERSPARAGRAPHBREAKING RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-143"><span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC\_PrefersParagraphBreaking**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-144">O [**IInkAnalyzer**](iinkanalyzer.md) deve enviar parágrafos inteiros de tinta para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), permitindo que o **IInkAnalysisRecognizer** faça a quebra de linha e a palavra (ou caractere).</span><span class="sxs-lookup"><span data-stu-id="50bf6-144">The [**IInkAnalyzer**](iinkanalyzer.md) should send entire paragraphs of ink to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), allowing the **IInkAnalysisRecognizer** to do the line breaking and word (or character) breaking.</span></span>

</dd> <dt>

<span data-ttu-id="50bf6-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**\_PREFERSSEGMENTATIONRECOGNITION RC**</span><span class="sxs-lookup"><span data-stu-id="50bf6-145"><span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC\_PrefersSegmentationRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="50bf6-146">Reconhece apenas uma palavra ou um caractere por operação de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="50bf6-146">Recognizes only one word or character per recognition operation.</span></span> <span data-ttu-id="50bf6-147">O [**IInkAnalyzer**](iinkanalyzer.md) executa segmentação no manuscrito e envia apenas um segmento de cada vez para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="50bf6-147">The [**IInkAnalyzer**](iinkanalyzer.md) performs segmentation on the handwriting and sends only one segment at a time to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50bf6-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="50bf6-148">Remarks</span></span>

<span data-ttu-id="50bf6-149">Essa enumeração permite uma combinação de bit a bit de seus valores de membro.</span><span class="sxs-lookup"><span data-stu-id="50bf6-149">This enumeration allows a bitwise combination of its member values.</span></span> <span data-ttu-id="50bf6-150">Use essa enumeração para localizar um reconhecedor de tinta instalado que dê suporte aos atributos necessários.</span><span class="sxs-lookup"><span data-stu-id="50bf6-150">Use this enumeration to find an installed ink recognizer that supports the attributes you need.</span></span>

## <a name="requirements"></a><span data-ttu-id="50bf6-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50bf6-151">Requirements</span></span>



| <span data-ttu-id="50bf6-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="50bf6-152">Requirement</span></span> | <span data-ttu-id="50bf6-153">Valor</span><span class="sxs-lookup"><span data-stu-id="50bf6-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50bf6-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50bf6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="50bf6-155">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="50bf6-155">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="50bf6-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50bf6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="50bf6-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="50bf6-157">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="50bf6-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50bf6-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="50bf6-159"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="50bf6-159"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50bf6-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="50bf6-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50bf6-161">**IInkAnalysisRecognizer:: GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="50bf6-161">**IInkAnalysisRecognizer::GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[<span data-ttu-id="50bf6-162">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="50bf6-162">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




