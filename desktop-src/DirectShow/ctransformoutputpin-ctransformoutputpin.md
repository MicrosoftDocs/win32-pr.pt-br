---
description: Método de construtor.
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Construtor CTransformOutputPin. CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 730149ae67abb2924174954bb8b620a02cfae2b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757636"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a><span data-ttu-id="39739-103">Construtor CTransformOutputPin. CTransformOutputPin</span><span class="sxs-lookup"><span data-stu-id="39739-103">CTransformOutputPin.CTransformOutputPin constructor</span></span>

<span data-ttu-id="39739-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="39739-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39739-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39739-105">Syntax</span></span>


```C++
CTransformOutputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="39739-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39739-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39739-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="39739-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="39739-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="39739-108">String containing the debug name of the object.</span></span> <span data-ttu-id="39739-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="39739-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="39739-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="39739-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="39739-111">Ponteiro para o filtro que criou esse PIN, que deve ser um objeto [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="39739-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="39739-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="39739-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="39739-113">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="39739-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="39739-114">Inicialize o valor para S \_ OK antes de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="39739-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="39739-115">O valor será alterado somente se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="39739-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="39739-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="39739-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="39739-117">Cadeia de caracteres largos contendo o nome do PIN.</span><span class="sxs-lookup"><span data-stu-id="39739-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39739-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="39739-118">Remarks</span></span>

<span data-ttu-id="39739-119">O parâmetro *pname* especifica o nome do PIN, que é retornado pelo método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="39739-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="39739-120">No entanto, a cadeia de caracteres não é usada para o identificador de PIN.</span><span class="sxs-lookup"><span data-stu-id="39739-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="39739-121">O identificador de PIN para esta classe é sempre "out".</span><span class="sxs-lookup"><span data-stu-id="39739-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="39739-122">Para obter mais informações, consulte [**QueryId**](ctransformoutputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="39739-122">For more information, see [**QueryId**](ctransformoutputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39739-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39739-123">Requirements</span></span>



| <span data-ttu-id="39739-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="39739-124">Requirement</span></span> | <span data-ttu-id="39739-125">Valor</span><span class="sxs-lookup"><span data-stu-id="39739-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39739-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39739-126">Header</span></span><br/>  | <dl> <span data-ttu-id="39739-127"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39739-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39739-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39739-128">Library</span></span><br/> | <dl> <span data-ttu-id="39739-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="39739-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




