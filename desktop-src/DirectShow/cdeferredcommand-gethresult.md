---
description: O método gethresult recupera o valor HRESULT do comando invocado.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Método CDeferredCommand. gethresult (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811745"
---
# <a name="cdeferredcommandgethresult-method"></a><span data-ttu-id="1b170-103">Método CDeferredCommand. gethresult</span><span class="sxs-lookup"><span data-stu-id="1b170-103">CDeferredCommand.GetHResult method</span></span>

<span data-ttu-id="1b170-104">O `GetHResult` método recupera o valor **HRESULT** do comando chamado.</span><span class="sxs-lookup"><span data-stu-id="1b170-104">The `GetHResult` method retrieves the **HRESULT** value from the invoked command.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b170-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b170-105">Syntax</span></span>


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a><span data-ttu-id="1b170-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b170-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b170-107">*phrResult*</span><span class="sxs-lookup"><span data-stu-id="1b170-107">*phrResult*</span></span> 
</dt> <dd>

<span data-ttu-id="1b170-108">Ponteiro para o valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b170-108">Pointer to the **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b170-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b170-109">Return value</span></span>

<span data-ttu-id="1b170-110">Retorna E \_ Abort se **m \_ pQueue** for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1b170-110">Returns E\_ABORT if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="1b170-111">Caso contrário, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1b170-111">Otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b170-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b170-112">Remarks</span></span>

<span data-ttu-id="1b170-113">Essa função de membro implementa o método [**IDeferredCommand:: gethresult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .</span><span class="sxs-lookup"><span data-stu-id="1b170-113">This member function implements the [**IDeferredCommand::GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b170-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b170-114">Requirements</span></span>



| <span data-ttu-id="1b170-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b170-115">Requirement</span></span> | <span data-ttu-id="1b170-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1b170-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b170-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b170-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1b170-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b170-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1b170-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b170-119">Library</span></span><br/> | <dl> <span data-ttu-id="1b170-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1b170-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b170-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b170-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b170-122">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="1b170-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




