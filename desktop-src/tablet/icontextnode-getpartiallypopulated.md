---
description: Recupera o valor que indica se um objeto IContextNode está parcialmente populado ou totalmente preenchido.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'Método IContextNode:: GetPartiallyPopulated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090547"
---
# <a name="icontextnodegetpartiallypopulated-method"></a><span data-ttu-id="d57a1-103">Método IContextNode:: GetPartiallyPopulated</span><span class="sxs-lookup"><span data-stu-id="d57a1-103">IContextNode::GetPartiallyPopulated method</span></span>

<span data-ttu-id="d57a1-104">Recupera o valor que indica se um objeto [**IContextNode**](icontextnode.md) está parcialmente populado ou totalmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="d57a1-104">Retrieves the value that indicates whether an [**IContextNode**](icontextnode.md) object is partially populated or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d57a1-105">Syntax</span></span>


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="d57a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d57a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57a1-107">*pfPartiallyPopulated* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d57a1-107">*pfPartiallyPopulated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d57a1-108">**Variante \_ TRUE** se este objeto [**IContextNode**](icontextnode.md) não contiver dados completos; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d57a1-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) object does not contain complete data; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57a1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d57a1-109">Return value</span></span>

<span data-ttu-id="d57a1-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d57a1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d57a1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d57a1-111">Remarks</span></span>

<span data-ttu-id="d57a1-112">Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="d57a1-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d57a1-113">Para obter mais informações, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d57a1-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d57a1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d57a1-114">Requirements</span></span>



| <span data-ttu-id="d57a1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d57a1-115">Requirement</span></span> | <span data-ttu-id="d57a1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d57a1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57a1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d57a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d57a1-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d57a1-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d57a1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d57a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d57a1-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d57a1-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d57a1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d57a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57a1-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d57a1-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d57a1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d57a1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d57a1-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d57a1-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d57a1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d57a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57a1-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d57a1-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d57a1-127">**IContextNode::SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="d57a1-127">**IContextNode::SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="d57a1-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="d57a1-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="d57a1-129">**\_IAnalysisProxyEvents::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="d57a1-129">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="d57a1-130">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="d57a1-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




