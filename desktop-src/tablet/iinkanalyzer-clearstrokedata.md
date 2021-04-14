---
description: Limpa os dados de pacote de traço do IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'Método IInkAnalyzer:: ClearStrokeData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461150"
---
# <a name="iinkanalyzerclearstrokedata-method"></a><span data-ttu-id="20aca-103">Método IInkAnalyzer:: ClearStrokeData</span><span class="sxs-lookup"><span data-stu-id="20aca-103">IInkAnalyzer::ClearStrokeData method</span></span>

<span data-ttu-id="20aca-104">Limpa os dados de pacote de traço do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="20aca-104">Clears stroke packet data from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="20aca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20aca-105">Syntax</span></span>


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="20aca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20aca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20aca-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20aca-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20aca-108">O identificador do traço para o qual os dados do pacote são apagados.</span><span class="sxs-lookup"><span data-stu-id="20aca-108">The identifier of the stroke for which the packet data is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20aca-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20aca-109">Return value</span></span>

<span data-ttu-id="20aca-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="20aca-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20aca-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="20aca-111">Remarks</span></span>

<span data-ttu-id="20aca-112">Use esse método quando os dados de pacote de um traço forem alterados, como quando um traço é movido ou transformado de outra maneira.</span><span class="sxs-lookup"><span data-stu-id="20aca-112">Use this method when packet data for a stroke changes, such as when a stroke is moved or otherwise transformed.</span></span> <span data-ttu-id="20aca-113">O [**IInkAnalyzer**](iinkanalyzer.md) gera o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) quando precisa traçar dados de pacote de um traço para o qual os dados do pacote foram limpos.</span><span class="sxs-lookup"><span data-stu-id="20aca-113">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event when it needs stroke packet data from a stroke for which the packet data has been cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="20aca-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20aca-114">Requirements</span></span>



| <span data-ttu-id="20aca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="20aca-115">Requirement</span></span> | <span data-ttu-id="20aca-116">Valor</span><span class="sxs-lookup"><span data-stu-id="20aca-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20aca-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20aca-117">Minimum supported client</span></span><br/> | <span data-ttu-id="20aca-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="20aca-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20aca-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20aca-119">Minimum supported server</span></span><br/> | <span data-ttu-id="20aca-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20aca-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="20aca-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20aca-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="20aca-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="20aca-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="20aca-123">DLL</span><span class="sxs-lookup"><span data-stu-id="20aca-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20aca-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20aca-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="20aca-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="20aca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20aca-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="20aca-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="20aca-127">**Método IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="20aca-127">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="20aca-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="20aca-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




