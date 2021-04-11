---
description: Recupera o tipo do traço especificado.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Método IInkAnalyzer:: getstroketype (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164536"
---
# <a name="iinkanalyzergetstroketype-method"></a><span data-ttu-id="20b46-103">Método IInkAnalyzer:: getstroketype</span><span class="sxs-lookup"><span data-stu-id="20b46-103">IInkAnalyzer::GetStrokeType method</span></span>

<span data-ttu-id="20b46-104">Recupera o tipo do traço especificado.</span><span class="sxs-lookup"><span data-stu-id="20b46-104">Retrieves the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b46-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20b46-105">Syntax</span></span>


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="20b46-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20b46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20b46-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20b46-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20b46-108">O identificador de traço.</span><span class="sxs-lookup"><span data-stu-id="20b46-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="20b46-109">*pStrokeType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="20b46-109">*pStrokeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20b46-110">A classificação do traço especificado.</span><span class="sxs-lookup"><span data-stu-id="20b46-110">The classification of the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20b46-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20b46-111">Return value</span></span>

<span data-ttu-id="20b46-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="20b46-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20b46-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="20b46-113">Remarks</span></span>

<span data-ttu-id="20b46-114">Se o tipo do traço for o [**valor de StrokeType**](stroketype.md) como não \_ classificado, o [**IInkAnalyzer**](iinkanalyzer.md) classificará o traço durante a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="20b46-114">If the stroke's type is the [**StrokeType**](stroketype.md) value StrokeType\_Unclassified, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="20b46-115">Caso contrário, o **IInkAnalyzer** usará o tipo definido no traço.</span><span class="sxs-lookup"><span data-stu-id="20b46-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="20b46-116">O [**IInkAnalyzer**](iinkanalyzer.md) não define o valor do tipo Stroke como parte da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="20b46-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="20b46-117">Para especificar ou alterar o tipo de traço, use o método [**IInkAnalyzer:: Setstroketype**](iinkanalyzer-setstroketype.md) ou [**IInkAnalyzer:: setstrokestype**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="20b46-117">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20b46-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20b46-118">Requirements</span></span>



| <span data-ttu-id="20b46-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="20b46-119">Requirement</span></span> | <span data-ttu-id="20b46-120">Valor</span><span class="sxs-lookup"><span data-stu-id="20b46-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b46-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20b46-121">Minimum supported client</span></span><br/> | <span data-ttu-id="20b46-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="20b46-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20b46-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20b46-123">Minimum supported server</span></span><br/> | <span data-ttu-id="20b46-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20b46-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="20b46-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20b46-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="20b46-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="20b46-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="20b46-127">DLL</span><span class="sxs-lookup"><span data-stu-id="20b46-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b46-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b46-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="20b46-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="20b46-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b46-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="20b46-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="20b46-131">**Método IInkAnalyzer:: setstroketype**</span><span class="sxs-lookup"><span data-stu-id="20b46-131">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="20b46-132">**Método IInkAnalyzer:: setstrokestype**</span><span class="sxs-lookup"><span data-stu-id="20b46-132">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="20b46-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="20b46-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




