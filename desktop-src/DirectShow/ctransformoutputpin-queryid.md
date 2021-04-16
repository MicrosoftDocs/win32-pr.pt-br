---
description: 'O método QueryId recupera um identificador para o PIN. Esse método implementa o método IPin:: QueryId.'
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
ms.openlocfilehash: 3e8e5fbc4b4da7b38853df5b4dcf3580a8c198d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789651"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="ada12-104">Método CTransformOutputPin. QueryId</span><span class="sxs-lookup"><span data-stu-id="ada12-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="ada12-105">O `QueryId` método recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="ada12-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="ada12-106">Esse método implementa o método [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="ada12-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada12-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ada12-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="ada12-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ada12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada12-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="ada12-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="ada12-110">Recebe uma cadeia de caracteres que contém o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="ada12-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada12-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ada12-111">Return value</span></span>

<span data-ttu-id="ada12-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ada12-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ada12-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ada12-113">Return code</span></span>                                                                                   | <span data-ttu-id="ada12-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ada12-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="ada12-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ada12-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ada12-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="ada12-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="ada12-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ada12-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ada12-118">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="ada12-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="ada12-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ada12-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ada12-120">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="ada12-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ada12-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ada12-121">Remarks</span></span>

<span data-ttu-id="ada12-122">O identificador de PIN é usado para persistência de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ada12-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="ada12-123">O identificador de PIN para esta classe está fora. Essa classe substitui o comportamento da classe [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="ada12-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="ada12-124">Na classe **CBasePin** , o identificador de PIN é o mesmo que o nome do PIN, especificado no construtor da classe.</span><span class="sxs-lookup"><span data-stu-id="ada12-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="ada12-125">Na classe **CTransformInputPin** , o identificador de PIN e o nome do PIN não são iguais.</span><span class="sxs-lookup"><span data-stu-id="ada12-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="ada12-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ada12-126">Requirements</span></span>



| <span data-ttu-id="ada12-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada12-127">Requirement</span></span> | <span data-ttu-id="ada12-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ada12-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ada12-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ada12-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ada12-130"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ada12-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ada12-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ada12-131">Library</span></span><br/> | <dl> <span data-ttu-id="ada12-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ada12-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




