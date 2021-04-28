---
description: 'Método CTransformInputPin. QueryId – o método QueryId recupera um identificador para o PIN. Esse método implementa o método IPin:: QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Método CTransformInputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8407e649814fcb12f699c2362f0f89137e941d19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095003"
---
# <a name="ctransforminputpinqueryid-method"></a><span data-ttu-id="18b63-104">Método CTransformInputPin. QueryId</span><span class="sxs-lookup"><span data-stu-id="18b63-104">CTransformInputPin.QueryId method</span></span>

<span data-ttu-id="18b63-105">O `QueryId` método recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="18b63-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="18b63-106">Esse método implementa o método [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="18b63-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b63-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18b63-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="18b63-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18b63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b63-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="18b63-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="18b63-110">Recebe uma cadeia de caracteres que contém o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="18b63-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b63-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="18b63-111">Return value</span></span>

<span data-ttu-id="18b63-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="18b63-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="18b63-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="18b63-113">Return code</span></span>                                                                                   | <span data-ttu-id="18b63-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="18b63-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="18b63-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="18b63-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="18b63-116">Êxito</span><span class="sxs-lookup"><span data-stu-id="18b63-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="18b63-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="18b63-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="18b63-118">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="18b63-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="18b63-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="18b63-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="18b63-120">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="18b63-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18b63-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="18b63-121">Remarks</span></span>

<span data-ttu-id="18b63-122">O identificador de PIN é usado para persistência de gráfico.</span><span class="sxs-lookup"><span data-stu-id="18b63-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="18b63-123">O identificador de PIN para esta classe está em.</span><span class="sxs-lookup"><span data-stu-id="18b63-123">The pin identifier for this class is In.</span></span> <span data-ttu-id="18b63-124">Essa classe substitui o comportamento da classe [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="18b63-124">This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="18b63-125">Na classe **CBasePin** , o identificador de PIN é o mesmo que o nome do PIN, especificado no construtor da classe.</span><span class="sxs-lookup"><span data-stu-id="18b63-125">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="18b63-126">Na classe **CTransformInputPin** , o identificador de PIN e o nome do PIN não são iguais.</span><span class="sxs-lookup"><span data-stu-id="18b63-126">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b63-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18b63-127">Requirements</span></span>



| <span data-ttu-id="18b63-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="18b63-128">Requirement</span></span> | <span data-ttu-id="18b63-129">Valor</span><span class="sxs-lookup"><span data-stu-id="18b63-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b63-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18b63-130">Header</span></span><br/>  | <dl> <span data-ttu-id="18b63-131"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18b63-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="18b63-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18b63-132">Library</span></span><br/> | <dl> <span data-ttu-id="18b63-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="18b63-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




