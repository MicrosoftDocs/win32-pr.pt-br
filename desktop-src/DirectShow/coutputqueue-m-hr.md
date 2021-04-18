---
description: Valor HRESULT que indica se o objeto aceitará amostras. Se o valor for S \_ OK, o objeto aceitará amostras. Caso contrário, ele rejeita amostras.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Membro COutputQueue:: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749247"
---
# <a name="coutputqueuem_hr-member"></a><span data-ttu-id="fb530-105">Membro de COutputQueue:: m \_ hr</span><span class="sxs-lookup"><span data-stu-id="fb530-105">COutputQueue::m\_hr member</span></span>

<span data-ttu-id="fb530-106">Valor **HRESULT** que indica se o objeto aceitará amostras.</span><span class="sxs-lookup"><span data-stu-id="fb530-106">**HRESULT** value that indicates whether the object will accept samples.</span></span> <span data-ttu-id="fb530-107">Se o valor for S \_ OK, o objeto aceitará amostras.</span><span class="sxs-lookup"><span data-stu-id="fb530-107">If the value is S\_OK, the object will accept samples.</span></span> <span data-ttu-id="fb530-108">Caso contrário, ele rejeita amostras.</span><span class="sxs-lookup"><span data-stu-id="fb530-108">Otherwise, it rejects samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb530-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb530-109">Syntax</span></span>


```C++
HRESULT m_hr;
```



## <a name="remarks"></a><span data-ttu-id="fb530-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb530-110">Remarks</span></span>

<span data-ttu-id="fb530-111">Essa variável de membro é usada para coordenar atividades entre threads.</span><span class="sxs-lookup"><span data-stu-id="fb530-111">This member variable is used to coordinate activities across threads.</span></span> <span data-ttu-id="fb530-112">Se o pino de entrada downstream rejeitar um exemplo ou se o objeto começar a ser liberado, o valor será definido como S \_ false ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="fb530-112">If the downstream input pin rejects a sample, or if the object begins flushing, the value is set to S\_FALSE or an error code.</span></span> <span data-ttu-id="fb530-113">O objeto não fornecerá mais amostras até que a liberação seja concluída ou até que o método [**COutputQueue:: Reset**](coutputqueue-reset.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="fb530-113">The object will not deliver any more samples until flushing is complete, or until the [**COutputQueue::Reset**](coutputqueue-reset.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb530-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb530-114">Requirements</span></span>



| <span data-ttu-id="fb530-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb530-115">Requirement</span></span> | <span data-ttu-id="fb530-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fb530-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb530-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb530-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fb530-118"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb530-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb530-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb530-119">Library</span></span><br/> | <dl> <span data-ttu-id="fb530-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fb530-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb530-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb530-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb530-122">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="fb530-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




