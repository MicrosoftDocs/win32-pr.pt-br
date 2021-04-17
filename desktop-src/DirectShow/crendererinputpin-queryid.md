---
description: 'O método QueryId recupera o identificador do PIN. Esse método substitui o método CBasePin:: QueryId.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Método CRendererInputPin. QueryId (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749242"
---
# <a name="crendererinputpinqueryid-method"></a><span data-ttu-id="34935-104">Método CRendererInputPin. QueryId</span><span class="sxs-lookup"><span data-stu-id="34935-104">CRendererInputPin.QueryId method</span></span>

<span data-ttu-id="34935-105">O `QueryId` método recupera o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="34935-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="34935-106">Esse método substitui o método [**CBasePin:: QueryId**](cbasepin-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="34935-106">This method overrides the [**CBasePin::QueryId**](cbasepin-queryid.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34935-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34935-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="34935-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34935-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34935-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="34935-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="34935-110">Recebe uma cadeia de caracteres que contém o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="34935-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34935-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34935-111">Return value</span></span>

<span data-ttu-id="34935-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="34935-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="34935-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="34935-113">Return code</span></span>                                                                                   | <span data-ttu-id="34935-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="34935-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="34935-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34935-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="34935-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="34935-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="34935-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="34935-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="34935-118">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="34935-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="34935-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="34935-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="34935-120">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="34935-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34935-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="34935-121">Remarks</span></span>

<span data-ttu-id="34935-122">Esse método aloca a cadeia de caracteres largos "em" e a atribui ao parâmetro *ID* .</span><span class="sxs-lookup"><span data-stu-id="34935-122">This method allocates the wide-character string "In" and assigns it to the *Id* parameter.</span></span> <span data-ttu-id="34935-123">O chamador deve liberar a memória alocada, usando a função **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="34935-123">The caller must free the allocated memory, using the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34935-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34935-124">Requirements</span></span>



| <span data-ttu-id="34935-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="34935-125">Requirement</span></span> | <span data-ttu-id="34935-126">Valor</span><span class="sxs-lookup"><span data-stu-id="34935-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34935-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34935-127">Header</span></span><br/>  | <dl> <span data-ttu-id="34935-128"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34935-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34935-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34935-129">Library</span></span><br/> | <dl> <span data-ttu-id="34935-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="34935-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34935-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="34935-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34935-132">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="34935-132">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




