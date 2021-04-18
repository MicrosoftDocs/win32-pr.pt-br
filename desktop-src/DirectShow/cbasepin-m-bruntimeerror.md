---
description: Sinalizador que indica se ocorreu um erro em tempo de execução.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Membro CBasePin:: m_bRunTimeError (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752903"
---
# <a name="cbasepinm_bruntimeerror-member"></a><span data-ttu-id="88ca0-103">Membro de CBasePin:: m \_ bRunTimeError</span><span class="sxs-lookup"><span data-stu-id="88ca0-103">CBasePin::m\_bRunTimeError member</span></span>

<span data-ttu-id="88ca0-104">Sinalizador que indica se ocorreu um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="88ca0-104">Flag that indicates whether a run-time error has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ca0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88ca0-105">Syntax</span></span>


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a><span data-ttu-id="88ca0-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="88ca0-106">Remarks</span></span>

<span data-ttu-id="88ca0-107">Esse sinalizador assume como padrão **false**.</span><span class="sxs-lookup"><span data-stu-id="88ca0-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="88ca0-108">Defina o sinalizador como **verdadeiro** se ocorrer um erro em tempo de execução durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="88ca0-108">Set the flag to **TRUE** if a run-time error occurs during streaming.</span></span> <span data-ttu-id="88ca0-109">O método [**CBasePin:: Inactive**](cbasepin-inactive.md) redefine o sinalizador como **false**.</span><span class="sxs-lookup"><span data-stu-id="88ca0-109">The [**CBasePin::Inactive**](cbasepin-inactive.md) method resets the flag to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ca0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88ca0-110">Requirements</span></span>



| <span data-ttu-id="88ca0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ca0-111">Requirement</span></span> | <span data-ttu-id="88ca0-112">Valor</span><span class="sxs-lookup"><span data-stu-id="88ca0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ca0-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88ca0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="88ca0-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88ca0-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88ca0-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88ca0-115">Library</span></span><br/> | <dl> <span data-ttu-id="88ca0-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="88ca0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ca0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="88ca0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ca0-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="88ca0-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




