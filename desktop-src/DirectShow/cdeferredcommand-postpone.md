---
description: O método adiado especifica um novo tempo de apresentação para um comando anteriormente enfileirado.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Método CDeferredCommand. adie (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768666"
---
# <a name="cdeferredcommandpostpone-method"></a><span data-ttu-id="575e6-103">Método CDeferredCommand. adie</span><span class="sxs-lookup"><span data-stu-id="575e6-103">CDeferredCommand.Postpone method</span></span>

<span data-ttu-id="575e6-104">O `Postpone` método especifica um novo tempo de apresentação para um comando enfileirado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="575e6-104">The `Postpone` method specifies a new presentation time for a previously queued command.</span></span>

## <a name="syntax"></a><span data-ttu-id="575e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="575e6-105">Syntax</span></span>


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a><span data-ttu-id="575e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="575e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="575e6-107">*newtime*</span><span class="sxs-lookup"><span data-stu-id="575e6-107">*newtime*</span></span> 
</dt> <dd>

<span data-ttu-id="575e6-108">Nova hora da apresentação.</span><span class="sxs-lookup"><span data-stu-id="575e6-108">New presentation time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="575e6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="575e6-109">Return value</span></span>

<span data-ttu-id="575e6-110">Retornará VFW \_ E \_ hora \_ já \_ passado se *Newtime* já tiver passado.</span><span class="sxs-lookup"><span data-stu-id="575e6-110">Returns VFW\_E\_TIME\_ALREADY\_PASSED if *newtime* is already passed.</span></span> <span data-ttu-id="575e6-111">Caso contrário, retorna um **HRESULT** resultante de uma chamada para [**CCmdQueue:: Remove**](ccmdqueue-remove.md) (ao extrair da lista) ou [**CCmdQueue:: Insert**](ccmdqueue-insert.md) (ao reinserir com o tempo alterado).</span><span class="sxs-lookup"><span data-stu-id="575e6-111">Otherwise, returns an **HRESULT** resulting from a call to [**CCmdQueue::Remove**](ccmdqueue-remove.md) (when extracting from the list) or [**CCmdQueue::Insert**](ccmdqueue-insert.md) (when reinserting with the changed time).</span></span>

## <a name="remarks"></a><span data-ttu-id="575e6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="575e6-112">Remarks</span></span>

<span data-ttu-id="575e6-113">Essa função de membro implementa o método [**IDeferredCommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .</span><span class="sxs-lookup"><span data-stu-id="575e6-113">This member function implements the [**IDeferredCommand::Postpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="575e6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="575e6-114">Requirements</span></span>



| <span data-ttu-id="575e6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="575e6-115">Requirement</span></span> | <span data-ttu-id="575e6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="575e6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575e6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="575e6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="575e6-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="575e6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="575e6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="575e6-119">Library</span></span><br/> | <dl> <span data-ttu-id="575e6-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="575e6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575e6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="575e6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575e6-122">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="575e6-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




