---
description: 'O método Unadvise remove uma solicitação de aviso pendente. Esse método implementa o método IReferenceClock:: Unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Método CBaseReferenceClock. Unadvise (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751906"
---
# <a name="cbasereferenceclockunadvise-method"></a><span data-ttu-id="d91b1-104">Método CBaseReferenceClock. Unadvise</span><span class="sxs-lookup"><span data-stu-id="d91b1-104">CBaseReferenceClock.Unadvise method</span></span>

<span data-ttu-id="d91b1-105">O `Unadvise` método remove uma solicitação de aviso pendente.</span><span class="sxs-lookup"><span data-stu-id="d91b1-105">The `Unadvise` method removes a pending advise request.</span></span> <span data-ttu-id="d91b1-106">Esse método implementa o método [**IReferenceClock:: Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .</span><span class="sxs-lookup"><span data-stu-id="d91b1-106">This method implements the [**IReferenceClock::Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91b1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d91b1-107">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="d91b1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d91b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d91b1-109">*dwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="d91b1-109">*dwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="d91b1-110">Identificador da solicitação a ser removida.</span><span class="sxs-lookup"><span data-stu-id="d91b1-110">Identifier of the request to remove.</span></span> <span data-ttu-id="d91b1-111">Use o valor retornado pelos métodos [**CBaseReferenceClock:: aconselhetime**](cbasereferenceclock-advisetime.md) ou [**CBaseReferenceClock:: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) no parâmetro *pdwAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="d91b1-111">Use the value returned by the [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) or [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) methods in the *pdwAdviseToken* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d91b1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d91b1-112">Return value</span></span>

<span data-ttu-id="d91b1-113">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d91b1-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d91b1-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d91b1-114">Return code</span></span>                                                                             | <span data-ttu-id="d91b1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d91b1-115">Description</span></span>           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="d91b1-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="d91b1-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d91b1-117">Não encontrado.</span><span class="sxs-lookup"><span data-stu-id="d91b1-117">Not found.</span></span><br/> |
| <dl> <span data-ttu-id="d91b1-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d91b1-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d91b1-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="d91b1-119">Success.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d91b1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d91b1-120">Requirements</span></span>



| <span data-ttu-id="d91b1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91b1-121">Requirement</span></span> | <span data-ttu-id="d91b1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d91b1-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91b1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d91b1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d91b1-124"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d91b1-124"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d91b1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d91b1-125">Library</span></span><br/> | <dl> <span data-ttu-id="d91b1-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d91b1-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d91b1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d91b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d91b1-128">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="d91b1-128">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




