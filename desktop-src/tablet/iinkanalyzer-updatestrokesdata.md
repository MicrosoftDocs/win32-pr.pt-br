---
description: Atualiza os dados de pacote para os traços especificados.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Método IInkAnalyzer:: UpdateStrokesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762439"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a><span data-ttu-id="76753-103">Método IInkAnalyzer:: UpdateStrokesData</span><span class="sxs-lookup"><span data-stu-id="76753-103">IInkAnalyzer::UpdateStrokesData method</span></span>

<span data-ttu-id="76753-104">Atualiza os dados de pacote para os traços especificados.</span><span class="sxs-lookup"><span data-stu-id="76753-104">Updates the packet data for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="76753-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76753-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="76753-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76753-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76753-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76753-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76753-108">O número de traços a serem atualizados.</span><span class="sxs-lookup"><span data-stu-id="76753-108">The number of strokes to update.</span></span>

</dd> <dt>

<span data-ttu-id="76753-109">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76753-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76753-110">Uma matriz que contém os identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="76753-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="76753-111">*ulStrokePacketDescriptionCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76753-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76753-112">O número de propriedades em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="76753-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="76753-113">*pStrokePacketDescriptionGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76753-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76753-114">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="76753-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="76753-115">*pulPacketDataCountPerStroke* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76753-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76753-116">Uma matriz que contém o número de pacotes em cada traço.</span><span class="sxs-lookup"><span data-stu-id="76753-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="76753-117">*plStrokePacketData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76753-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76753-118">Uma matriz que contém os dados de pacote para os traços.</span><span class="sxs-lookup"><span data-stu-id="76753-118">An array containing the packet data for the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76753-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76753-119">Return value</span></span>

<span data-ttu-id="76753-120">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="76753-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="76753-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="76753-121">Remarks</span></span>

<span data-ttu-id="76753-122">o parâmetro *plStrokePacketData* contém dados de pacote para todos os traços.</span><span class="sxs-lookup"><span data-stu-id="76753-122">the *plStrokePacketData* parameter contains packet data for all of the strokes.</span></span> <span data-ttu-id="76753-123">O parâmetro *pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço.</span><span class="sxs-lookup"><span data-stu-id="76753-123">The *pStrokePacketDescriptionGuids* parameter contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="76753-124">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="76753-124">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="76753-125">Somente traços com as mesmas descrições de pacote podem ser atualizados em uma única chamada para o **método IInkAnalyzer:: UpdateStrokesData**.</span><span class="sxs-lookup"><span data-stu-id="76753-125">Only strokes with the same packet descriptions can be updated in a single call to **IInkAnalyzer::UpdateStrokesData Method**.</span></span>

<span data-ttu-id="76753-126">Esse método não atualiza a região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="76753-126">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="76753-127">Se um traço especificado não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.</span><span class="sxs-lookup"><span data-stu-id="76753-127">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="76753-128">Se nenhum dos traços especificados identificar um traço associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="76753-128">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="76753-129">Esse método retorna um código de erro quando *plStrokeIds* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="76753-129">This method returns an error code when *plStrokeIds* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="76753-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76753-130">Requirements</span></span>



| <span data-ttu-id="76753-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="76753-131">Requirement</span></span> | <span data-ttu-id="76753-132">Valor</span><span class="sxs-lookup"><span data-stu-id="76753-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76753-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76753-133">Minimum supported client</span></span><br/> | <span data-ttu-id="76753-134">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="76753-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="76753-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76753-135">Minimum supported server</span></span><br/> | <span data-ttu-id="76753-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="76753-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="76753-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76753-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="76753-138"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="76753-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="76753-139">DLL</span><span class="sxs-lookup"><span data-stu-id="76753-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76753-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76753-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="76753-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="76753-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76753-142">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="76753-142">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="76753-143">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="76753-143">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="76753-144">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="76753-144">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="76753-145">**Método IInkAnalyzer:: AddStrokeToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="76753-145">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="76753-146">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="76753-146">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="76753-147">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="76753-147">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="76753-148">**Método IInkAnalyzer:: AddStrokesToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="76753-148">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="76753-149">**Método IInkAnalyzer:: ClearStrokeData**</span><span class="sxs-lookup"><span data-stu-id="76753-149">**IInkAnalyzer::ClearStrokeData Method**</span></span>](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[<span data-ttu-id="76753-150">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="76753-150">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="76753-151">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="76753-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




