---
description: Determina se o IAnalysisRegion especificado contém o mesmo valor que o objeto IAnalysisRegion atual.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Método IAnalysisRegion:: EqualsRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090558"
---
# <a name="ianalysisregionequalsregion-method"></a><span data-ttu-id="de416-103">Método IAnalysisRegion:: EqualsRegion</span><span class="sxs-lookup"><span data-stu-id="de416-103">IAnalysisRegion::EqualsRegion method</span></span>

<span data-ttu-id="de416-104">Determina se o [**IAnalysisRegion**](ianalysisregion.md) especificado contém o mesmo valor que o objeto **IAnalysisRegion** atual.</span><span class="sxs-lookup"><span data-stu-id="de416-104">Determines whether the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current **IAnalysisRegion** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="de416-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de416-105">Syntax</span></span>


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a><span data-ttu-id="de416-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de416-107">*pOtherRegion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de416-107">*pOtherRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de416-108">O objeto [**IAnalysisRegion**](ianalysisregion.md) a ser comparado com o **IAnalysisRegion** atual.</span><span class="sxs-lookup"><span data-stu-id="de416-108">The [**IAnalysisRegion**](ianalysisregion.md) object to compare with the current **IAnalysisRegion**.</span></span>

</dd> <dt>

<span data-ttu-id="de416-109">*pfRegionsEqual* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="de416-109">*pfRegionsEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de416-110">**Variante \_ TRUE** se o [**IAnalysisRegion**](ianalysisregion.md) especificado contiver o mesmo valor que o IAnalysisRegion atual; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="de416-110">**VARIANT\_TRUE** if the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current IAnalysisRegion; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de416-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de416-111">Return value</span></span>

<span data-ttu-id="de416-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="de416-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de416-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de416-113">Requirements</span></span>



| <span data-ttu-id="de416-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de416-114">Requirement</span></span> | <span data-ttu-id="de416-115">Valor</span><span class="sxs-lookup"><span data-stu-id="de416-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de416-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de416-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de416-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="de416-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="de416-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de416-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de416-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="de416-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="de416-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de416-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de416-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="de416-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="de416-122">DLL</span><span class="sxs-lookup"><span data-stu-id="de416-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de416-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de416-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="de416-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="de416-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de416-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="de416-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> </dl>

 

 




