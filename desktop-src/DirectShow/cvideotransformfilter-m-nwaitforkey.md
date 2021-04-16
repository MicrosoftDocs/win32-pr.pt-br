---
description: O número máximo atual de quadros Delta a serem descartados.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Membro CVideoTransformFilter:: m_nWaitForKey (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757631"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a><span data-ttu-id="ed813-103">Membro de CVideoTransformFilter:: m \_ nWaitForKey</span><span class="sxs-lookup"><span data-stu-id="ed813-103">CVideoTransformFilter::m\_nWaitForKey member</span></span>

<span data-ttu-id="ed813-104">O número máximo atual de quadros Delta a serem descartados.</span><span class="sxs-lookup"><span data-stu-id="ed813-104">The current maximum number of delta frames to drop.</span></span> <span data-ttu-id="ed813-105">Embora essa variável seja maior que zero, o filtro removerá os quadros até atingir um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="ed813-105">While this variable is greater than zero, the filter will drop frames until it reaches a key frame.</span></span> <span data-ttu-id="ed813-106">Para cada quadro descartado, o filtro decrementa essa variável por uma, o que impede que o filtro descarte um número excessivo de quadros.</span><span class="sxs-lookup"><span data-stu-id="ed813-106">For each frame that is dropped, the filter decrements this variable by one, which prevents the filter from dropping an excessive number of frames.</span></span> <span data-ttu-id="ed813-107">Depois de 30 quadros Delta em uma linha sem quadros-chave, o filtro começará a entregar quadros novamente.</span><span class="sxs-lookup"><span data-stu-id="ed813-107">After 30 delta frames in a row with no key frames, the filter will start delivering frames again.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed813-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed813-108">Syntax</span></span>


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a><span data-ttu-id="ed813-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed813-109">Requirements</span></span>



| <span data-ttu-id="ed813-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed813-110">Requirement</span></span> | <span data-ttu-id="ed813-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ed813-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed813-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed813-112">Header</span></span><br/>  | <dl> <span data-ttu-id="ed813-113"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed813-113"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ed813-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed813-114">Library</span></span><br/> | <dl> <span data-ttu-id="ed813-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ed813-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed813-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed813-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed813-117">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="ed813-117">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




