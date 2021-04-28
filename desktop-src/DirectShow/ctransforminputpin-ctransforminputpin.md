---
description: Construtor de CTransformInputPin. CTransformInputPin-método de construtor.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Construtor CTransformInputPin. CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e893b4e1c7d4f396644a468d3d71fa3046fb712
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095044"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a><span data-ttu-id="00ca1-103">Construtor CTransformInputPin. CTransformInputPin</span><span class="sxs-lookup"><span data-stu-id="00ca1-103">CTransformInputPin.CTransformInputPin constructor</span></span>

<span data-ttu-id="00ca1-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="00ca1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ca1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00ca1-105">Syntax</span></span>


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="00ca1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00ca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ca1-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="00ca1-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="00ca1-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="00ca1-108">String containing the debug name of the object.</span></span> <span data-ttu-id="00ca1-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="00ca1-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="00ca1-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="00ca1-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="00ca1-111">Ponteiro para o filtro que criou esse PIN, que deve ser um objeto [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="00ca1-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="00ca1-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="00ca1-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="00ca1-113">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="00ca1-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="00ca1-114">Inicialize o valor para S \_ OK antes de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="00ca1-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="00ca1-115">O valor será alterado somente se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="00ca1-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="00ca1-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="00ca1-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="00ca1-117">Cadeia de caracteres largos contendo o nome do PIN.</span><span class="sxs-lookup"><span data-stu-id="00ca1-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00ca1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="00ca1-118">Remarks</span></span>

<span data-ttu-id="00ca1-119">O parâmetro *pname* especifica o nome do PIN, que é retornado pelo método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="00ca1-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="00ca1-120">No entanto, a cadeia de caracteres não é usada para o identificador de PIN.</span><span class="sxs-lookup"><span data-stu-id="00ca1-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="00ca1-121">O identificador de PIN para esta classe é sempre "in".</span><span class="sxs-lookup"><span data-stu-id="00ca1-121">The pin identifier for this class is always "In".</span></span> <span data-ttu-id="00ca1-122">Para obter mais informações, consulte [**QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="00ca1-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00ca1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00ca1-123">Requirements</span></span>



| <span data-ttu-id="00ca1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="00ca1-124">Requirement</span></span> | <span data-ttu-id="00ca1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="00ca1-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ca1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00ca1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="00ca1-127"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00ca1-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="00ca1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00ca1-128">Library</span></span><br/> | <dl> <span data-ttu-id="00ca1-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="00ca1-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




