---
description: Valor booliano que indica se o filtro está atualmente descartando quadros. Se esse valor for TRUE, o filtro continuará a descartar os quadros até atingir o próximo quadro-chave ou até receber 30 quadros Delta em uma linha sem um quadro-chave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Membro CVideoTransformFilter:: m_bSkipping (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747580"
---
# <a name="cvideotransformfilterm_bskipping-member"></a><span data-ttu-id="f20cc-104">Membro de CVideoTransformFilter:: m \_ bSkipping</span><span class="sxs-lookup"><span data-stu-id="f20cc-104">CVideoTransformFilter::m\_bSkipping member</span></span>

<span data-ttu-id="f20cc-105">Valor booliano que indica se o filtro está atualmente descartando quadros.</span><span class="sxs-lookup"><span data-stu-id="f20cc-105">Boolean value that indicates whether the filter is currently dropping frames.</span></span> <span data-ttu-id="f20cc-106">Se esse valor for **true**, o filtro continuará a descartar os quadros até atingir o próximo quadro-chave ou até receber 30 quadros Delta em uma linha sem um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="f20cc-106">If this value is **TRUE**, the filter continues to drop frames until it reaches the next key frame, or until it receives 30 delta frames in a row without a key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f20cc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f20cc-107">Syntax</span></span>


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a><span data-ttu-id="f20cc-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f20cc-108">Requirements</span></span>



| <span data-ttu-id="f20cc-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20cc-109">Requirement</span></span> | <span data-ttu-id="f20cc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f20cc-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f20cc-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f20cc-111">Header</span></span><br/>  | <dl> <span data-ttu-id="f20cc-112"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f20cc-112"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f20cc-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f20cc-113">Library</span></span><br/> | <dl> <span data-ttu-id="f20cc-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f20cc-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f20cc-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f20cc-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20cc-116">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="f20cc-116">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




