---
description: Recupera a região do documento que corresponde às alterações feitas na árvore de nós de contexto do objeto IInkAnalyzer como resultado da análise de tinta.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Método IAnalysisStatus:: GetAppliedChangesRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501820"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a><span data-ttu-id="943f3-103">Método IAnalysisStatus:: GetAppliedChangesRegion</span><span class="sxs-lookup"><span data-stu-id="943f3-103">IAnalysisStatus::GetAppliedChangesRegion method</span></span>

<span data-ttu-id="943f3-104">Recupera a região do documento que corresponde às alterações feitas na árvore de nós de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) como resultado da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="943f3-104">Retrieves the region of the document that corresponds to changes that were made in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree as a result of ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="943f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="943f3-105">Syntax</span></span>


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a><span data-ttu-id="943f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="943f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="943f3-107">*pAppliedChangesRegion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="943f3-107">*pAppliedChangesRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="943f3-108">Um ponteiro para a [**IAnalysisRegion**](ianalysisregion.md) do documento em que foram feitas alterações.</span><span class="sxs-lookup"><span data-stu-id="943f3-108">A pointer to the [**IAnalysisRegion**](ianalysisregion.md) of the document where changes were made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="943f3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="943f3-109">Return value</span></span>

<span data-ttu-id="943f3-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="943f3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="943f3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="943f3-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="943f3-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pAppliedChangesRegion* quando você não precisar mais usar a região de análise.</span><span class="sxs-lookup"><span data-stu-id="943f3-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAppliedChangesRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="943f3-113">Esse método é usado com mais frequência quando o aplicativo recebe informações para fins de depuração e precisa invalidar a área onde as alterações podem ocorrer para que as informações de depuração sejam pintadas.</span><span class="sxs-lookup"><span data-stu-id="943f3-113">This method is most frequently used when the application receives information for debugging purposes and needs to invalidate the area where changes might occur so that the debugging information is painted.</span></span>

## <a name="requirements"></a><span data-ttu-id="943f3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="943f3-114">Requirements</span></span>



| <span data-ttu-id="943f3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="943f3-115">Requirement</span></span> | <span data-ttu-id="943f3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="943f3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943f3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="943f3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="943f3-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="943f3-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="943f3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="943f3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="943f3-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="943f3-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="943f3-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="943f3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="943f3-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="943f3-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="943f3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="943f3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="943f3-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="943f3-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="943f3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="943f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943f3-126">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="943f3-126">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="943f3-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="943f3-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="943f3-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="943f3-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

