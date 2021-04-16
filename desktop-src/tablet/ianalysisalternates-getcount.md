---
description: Recupera o número de objetos IAnalysisAlternate contidos na coleção IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'Método IAnalysisAlternates:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794581"
---
# <a name="ianalysisalternatesgetcount-method"></a><span data-ttu-id="83dbe-103">Método IAnalysisAlternates:: GetCount</span><span class="sxs-lookup"><span data-stu-id="83dbe-103">IAnalysisAlternates::GetCount method</span></span>

<span data-ttu-id="83dbe-104">Recupera o número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contidos na coleção [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="83dbe-104">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="83dbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83dbe-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="83dbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83dbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83dbe-107">*pulCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="83dbe-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83dbe-108">Um inteiro de 32 bits não assinado que é definido como o número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contidos na coleção [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="83dbe-108">An unsigned 32-bit integer that is set to the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83dbe-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83dbe-109">Return value</span></span>

<span data-ttu-id="83dbe-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="83dbe-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83dbe-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83dbe-111">Requirements</span></span>



| <span data-ttu-id="83dbe-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="83dbe-112">Requirement</span></span> | <span data-ttu-id="83dbe-113">Valor</span><span class="sxs-lookup"><span data-stu-id="83dbe-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83dbe-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83dbe-114">Minimum supported client</span></span><br/> | <span data-ttu-id="83dbe-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="83dbe-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="83dbe-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83dbe-116">Minimum supported server</span></span><br/> | <span data-ttu-id="83dbe-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="83dbe-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="83dbe-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83dbe-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="83dbe-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="83dbe-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="83dbe-120">DLL</span><span class="sxs-lookup"><span data-stu-id="83dbe-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83dbe-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83dbe-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="83dbe-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="83dbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83dbe-123">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="83dbe-123">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="83dbe-124">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="83dbe-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




