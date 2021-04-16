---
description: Sinalizador que indica se a qualidade foi alterada.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Membro CTransformFilter:: m_bQualityChanged (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759263"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a><span data-ttu-id="b3d7a-103">Membro de CTransformFilter:: m \_ bQualityChanged</span><span class="sxs-lookup"><span data-stu-id="b3d7a-103">CTransformFilter::m\_bQualityChanged member</span></span>

<span data-ttu-id="b3d7a-104">Sinalizador que indica se a qualidade foi alterada.</span><span class="sxs-lookup"><span data-stu-id="b3d7a-104">Flag that indicates whether the quality has changed.</span></span> <span data-ttu-id="b3d7a-105">Na primeira vez que o filtro descartar um exemplo, ele enviará um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro e definirá esse sinalizador como **true**.</span><span class="sxs-lookup"><span data-stu-id="b3d7a-105">The first time that the filter drops a sample, it sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager and sets this flag to **TRUE**.</span></span> <span data-ttu-id="b3d7a-106">Ele não envia esse evento novamente até que o filtro seja interrompido e reiniciado, mesmo que ele continue a descartar amostras enquanto isso.</span><span class="sxs-lookup"><span data-stu-id="b3d7a-106">It does not send this event again until the filter stops and restarts, even if it continues to drop samples in the meantime.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d7a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d7a-107">Syntax</span></span>


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a><span data-ttu-id="b3d7a-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3d7a-108">Requirements</span></span>



| <span data-ttu-id="b3d7a-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d7a-109">Requirement</span></span> | <span data-ttu-id="b3d7a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b3d7a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d7a-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3d7a-111">Header</span></span><br/>  | <dl> <span data-ttu-id="b3d7a-112"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d7a-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b3d7a-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3d7a-113">Library</span></span><br/> | <dl> <span data-ttu-id="b3d7a-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d7a-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3d7a-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3d7a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d7a-116">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="b3d7a-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




