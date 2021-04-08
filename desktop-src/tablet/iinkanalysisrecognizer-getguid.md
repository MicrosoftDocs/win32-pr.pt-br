---
description: Recupera o identificador global exclusivo (GUID) do reconhecedor.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'Método IInkAnalysisRecognizer:: GetGuid (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827185"
---
# <a name="iinkanalysisrecognizergetguid-method"></a><span data-ttu-id="0abe7-103">Método IInkAnalysisRecognizer:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="0abe7-103">IInkAnalysisRecognizer::GetGuid method</span></span>

<span data-ttu-id="0abe7-104">Recupera o identificador global exclusivo (GUID) do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="0abe7-104">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0abe7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0abe7-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="0abe7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0abe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abe7-107">*pid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0abe7-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0abe7-108">O GUID que identifica este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="0abe7-108">The GUID that identifies this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0abe7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0abe7-109">Return value</span></span>

<span data-ttu-id="0abe7-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0abe7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0abe7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0abe7-111">Requirements</span></span>



| <span data-ttu-id="0abe7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0abe7-112">Requirement</span></span> | <span data-ttu-id="0abe7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="0abe7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0abe7-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0abe7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0abe7-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0abe7-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0abe7-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0abe7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0abe7-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0abe7-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0abe7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0abe7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0abe7-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0abe7-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0abe7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0abe7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0abe7-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0abe7-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0abe7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0abe7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abe7-123">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="0abe7-123">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="0abe7-124">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="0abe7-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




