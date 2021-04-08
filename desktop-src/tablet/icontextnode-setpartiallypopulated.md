---
description: Modifica o valor que indica se este IContextNode está parcialmente ou totalmente preenchido.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'Método IContextNode:: SetPartiallyPopulated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010524"
---
# <a name="icontextnodesetpartiallypopulated-method"></a><span data-ttu-id="45105-103">Método IContextNode:: SetPartiallyPopulated</span><span class="sxs-lookup"><span data-stu-id="45105-103">IContextNode::SetPartiallyPopulated method</span></span>

<span data-ttu-id="45105-104">Modifica o valor que indica se este [**IContextNode**](icontextnode.md) está parcialmente ou totalmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="45105-104">Modifies the value that indicates whether this [**IContextNode**](icontextnode.md) is partially or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="45105-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45105-105">Syntax</span></span>


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="45105-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45105-107">*fPartiallyPopulated* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45105-107">*fPartiallyPopulated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45105-108">**Variante \_ TRUE** se este [**IContextNode**](icontextnode.md) for parcialmente preenchido; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="45105-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) is partially populated; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45105-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45105-109">Return value</span></span>

<span data-ttu-id="45105-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="45105-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="45105-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="45105-111">Remarks</span></span>

<span data-ttu-id="45105-112">Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="45105-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="45105-113">Para obter mais informações, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="45105-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="45105-114">Ao virtualizar sua árvore de documentos, certifique-se de definir o valor PropertyGuidsForContextNodes. RotatedBoundingBox (usando ContextNode. addpropertyvalue) em todos os objetos ContextNode.</span><span class="sxs-lookup"><span data-stu-id="45105-114">When virtualizing your document tree, be sure to set the PropertyGuidsForContextNodes.RotatedBoundingBox value (using ContextNode.AddPropertyValue) on all ContextNode objects.</span></span> <span data-ttu-id="45105-115">A propriedade RotatedBoundingBox é calculada pelo InkAnalyzer e, por padrão, deve estar em todos os ContextNodes de gravação.</span><span class="sxs-lookup"><span data-stu-id="45105-115">The RotatedBoundingBox property is calculated by the InkAnalyzer and by default should be on all writing ContextNodes.</span></span> <span data-ttu-id="45105-116">No entanto, se seu aplicativo virtualiza os resultados da análise definindo a propriedade PartiallyPopulated, ao manipular o evento PopulateContextNode, certifique-se de preencher a propriedade RotatedBoundingBox.</span><span class="sxs-lookup"><span data-stu-id="45105-116">However, if your application virtualizes the analysis results by setting the PartiallyPopulated property, when handling the PopulateContextNode event be sure to populate the RotatedBoundingBox property.</span></span> <span data-ttu-id="45105-117">Falha ao definir a propriedade RotatedBoundingBox resultará em potencialmente mais dados de documento sendo usados na operação de análise atual</span><span class="sxs-lookup"><span data-stu-id="45105-117">Failure to set the RotatedBoundingBox property will result in potentially more document data being used in the current analysis operation</span></span>

## <a name="requirements"></a><span data-ttu-id="45105-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45105-118">Requirements</span></span>



| <span data-ttu-id="45105-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="45105-119">Requirement</span></span> | <span data-ttu-id="45105-120">Valor</span><span class="sxs-lookup"><span data-stu-id="45105-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45105-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45105-121">Minimum supported client</span></span><br/> | <span data-ttu-id="45105-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="45105-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="45105-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45105-123">Minimum supported server</span></span><br/> | <span data-ttu-id="45105-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="45105-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="45105-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45105-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="45105-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="45105-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="45105-127">DLL</span><span class="sxs-lookup"><span data-stu-id="45105-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45105-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45105-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="45105-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="45105-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45105-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="45105-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="45105-131">**\_IAnalysisProxyEvents::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="45105-131">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="45105-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="45105-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="45105-133">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="45105-133">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="45105-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="45105-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




