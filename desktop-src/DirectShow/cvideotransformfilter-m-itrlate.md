---
description: Indica o quão tarde os exemplos chegam ao renderizador, em unidades de tempo de referência. Sintaxe.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Membro CVideoTransformFilter:: m_itrLate (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748011"
---
# <a name="cvideotransformfilterm_itrlate-member"></a><span data-ttu-id="4f98b-104">Membro de CVideoTransformFilter:: m \_ itrLate</span><span class="sxs-lookup"><span data-stu-id="4f98b-104">CVideoTransformFilter::m\_itrLate member</span></span>

<span data-ttu-id="4f98b-105">Indica o quão tarde os exemplos chegam ao renderizador, em unidades de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="4f98b-105">Indicates how late the samples are arriving at the renderer, in reference time units.</span></span> <span data-ttu-id="4f98b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f98b-106">Syntax</span></span>

## <a name="syntax"></a><span data-ttu-id="4f98b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f98b-107">Syntax</span></span>


```C++
int m_itrLate;
```



## <a name="remarks"></a><span data-ttu-id="4f98b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f98b-108">Remarks</span></span>

<span data-ttu-id="4f98b-109">Quando o filtro recebe uma mensagem de qualidade do downstream, ele armazena o valor de atraso nessa variável.</span><span class="sxs-lookup"><span data-stu-id="4f98b-109">When the filter receives a quality message from downstream, it stores the lateness value in this variable.</span></span> <span data-ttu-id="4f98b-110">Como o filtro descarta os quadros, ele atualiza esse valor subtraindo a duração de cada quadro.</span><span class="sxs-lookup"><span data-stu-id="4f98b-110">As the filter drops frames, it updates this value by subtracting the duration of each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f98b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f98b-111">Requirements</span></span>



| <span data-ttu-id="4f98b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f98b-112">Requirement</span></span> | <span data-ttu-id="4f98b-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4f98b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f98b-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f98b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4f98b-115"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f98b-115"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4f98b-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f98b-116">Library</span></span><br/> | <dl> <span data-ttu-id="4f98b-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4f98b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f98b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f98b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f98b-119">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="4f98b-119">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




