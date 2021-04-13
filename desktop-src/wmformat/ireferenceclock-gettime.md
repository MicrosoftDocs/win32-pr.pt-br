---
title: Método getTime IReferenceClock
description: O método getTime recupera o tempo de referência atual.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Método getTime Windows Media Format
- Método getTime Windows Media Format, interface IReferenceClock
- IReferenceClock Interface formato Windows Media, método getTime
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365035"
---
# <a name="ireferenceclockgettime-method"></a><span data-ttu-id="de8e9-106">Método IReferenceClock:: getTime</span><span class="sxs-lookup"><span data-stu-id="de8e9-106">IReferenceClock::GetTime method</span></span>

<span data-ttu-id="de8e9-107">O método **getTime** recupera o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="de8e9-107">The **GetTime** method retrieves the current reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8e9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de8e9-108">Syntax</span></span>


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="de8e9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de8e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de8e9-110">*pTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="de8e9-110">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de8e9-111">Ponteiro para uma variável que recebe a hora atual, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="de8e9-111">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de8e9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de8e9-112">Return value</span></span>

<span data-ttu-id="de8e9-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="de8e9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="de8e9-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="de8e9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="de8e9-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="de8e9-115">Return code</span></span>                                                                               | <span data-ttu-id="de8e9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="de8e9-116">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="de8e9-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de8e9-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="de8e9-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="de8e9-118">The method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="de8e9-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="de8e9-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="de8e9-120">O parâmetro *pTime* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="de8e9-120">The *pTime* parameter is **NULL**.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="de8e9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="de8e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8e9-122">**Interface IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="de8e9-122">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





