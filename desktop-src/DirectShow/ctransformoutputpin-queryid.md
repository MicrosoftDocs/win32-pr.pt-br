---
description: 'Método CTransformOutputPin. QueryId – o método QueryId recupera um identificador para o PIN. Esse método implementa o método IPin:: QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Método CTransformOutputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094844"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="e7607-104">Método CTransformOutputPin. QueryId</span><span class="sxs-lookup"><span data-stu-id="e7607-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="e7607-105">O `QueryId` método recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="e7607-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="e7607-106">Esse método implementa o método [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="e7607-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7607-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7607-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="e7607-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7607-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7607-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="e7607-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="e7607-110">Recebe uma cadeia de caracteres que contém o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="e7607-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7607-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e7607-111">Return value</span></span>

<span data-ttu-id="e7607-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7607-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e7607-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e7607-113">Return code</span></span>                                                                                   | <span data-ttu-id="e7607-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7607-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="e7607-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7607-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e7607-116">Êxito</span><span class="sxs-lookup"><span data-stu-id="e7607-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="e7607-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e7607-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e7607-118">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="e7607-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="e7607-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e7607-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e7607-120">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="e7607-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7607-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7607-121">Remarks</span></span>

<span data-ttu-id="e7607-122">O identificador de PIN é usado para persistência de gráfico.</span><span class="sxs-lookup"><span data-stu-id="e7607-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="e7607-123">O identificador de PIN para esta classe está fora. Essa classe substitui o comportamento da classe [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="e7607-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="e7607-124">Na classe **CBasePin** , o identificador de PIN é o mesmo que o nome do PIN, especificado no construtor da classe.</span><span class="sxs-lookup"><span data-stu-id="e7607-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="e7607-125">Na classe **CTransformInputPin** , o identificador de PIN e o nome do PIN não são iguais.</span><span class="sxs-lookup"><span data-stu-id="e7607-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7607-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7607-126">Requirements</span></span>



| <span data-ttu-id="e7607-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7607-127">Requirement</span></span> | <span data-ttu-id="e7607-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e7607-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7607-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7607-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e7607-130"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7607-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e7607-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7607-131">Library</span></span><br/> | <dl> <span data-ttu-id="e7607-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e7607-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




