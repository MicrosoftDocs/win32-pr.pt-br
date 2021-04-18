---
description: O método Unadvise remove uma solicitação de aviso.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Método CAMSchedule. Unadvise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752115"
---
# <a name="camscheduleunadvise-method"></a><span data-ttu-id="01aac-103">Método CAMSchedule. Unadvise</span><span class="sxs-lookup"><span data-stu-id="01aac-103">CAMSchedule.Unadvise method</span></span>

<span data-ttu-id="01aac-104">O `Unadvise` método remove uma solicitação de aviso.</span><span class="sxs-lookup"><span data-stu-id="01aac-104">The `Unadvise` method removes an advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="01aac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01aac-105">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="01aac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01aac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01aac-107">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="01aac-107">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="01aac-108">Identificador da solicitação de aviso, retornado pelo método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="01aac-108">Identifier of the advise request, returned by the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01aac-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01aac-109">Return value</span></span>

<span data-ttu-id="01aac-110">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01aac-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="01aac-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01aac-111">Return code</span></span>                                                                             | <span data-ttu-id="01aac-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="01aac-112">Description</span></span>          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="01aac-113"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="01aac-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="01aac-114">Não encontrado</span><span class="sxs-lookup"><span data-stu-id="01aac-114">Not found</span></span><br/> |
| <dl> <span data-ttu-id="01aac-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01aac-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="01aac-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="01aac-116">Success</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="01aac-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01aac-117">Requirements</span></span>



| <span data-ttu-id="01aac-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="01aac-118">Requirement</span></span> | <span data-ttu-id="01aac-119">Valor</span><span class="sxs-lookup"><span data-stu-id="01aac-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01aac-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01aac-120">Header</span></span><br/>  | <dl> <span data-ttu-id="01aac-121"><dt>Dsschedule. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01aac-121"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="01aac-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01aac-122">Library</span></span><br/> | <dl> <span data-ttu-id="01aac-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="01aac-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01aac-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="01aac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01aac-125">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="01aac-125">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




