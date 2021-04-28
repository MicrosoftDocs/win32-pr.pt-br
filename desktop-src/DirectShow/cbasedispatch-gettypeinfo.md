---
description: Método CBaseDispatch. GetTypeInfo – o método GetTypeInfo recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Método CBaseDispatch. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b1e21133b4fa561c743fefc6282c777b444e6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120114"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="55670-103">Método CBaseDispatch. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="55670-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="55670-104">O `GetTypeInfo` método recupera as informações de tipo para o objeto, que pode ser usado para obter as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="55670-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="55670-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55670-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="55670-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55670-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55670-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="55670-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="55670-108">Referência a um IID (identificador de interface) que especifica a interface.</span><span class="sxs-lookup"><span data-stu-id="55670-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="55670-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="55670-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="55670-110">Digite as informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="55670-110">Type information to return.</span></span> <span data-ttu-id="55670-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="55670-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="55670-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="55670-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="55670-113">Identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="55670-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="55670-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="55670-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="55670-115">Endereço de uma variável que recebe um ponteiro **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="55670-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55670-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="55670-116">Return value</span></span>

<span data-ttu-id="55670-117">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55670-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="55670-118">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="55670-118">Possible values include the following.</span></span>



| <span data-ttu-id="55670-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="55670-119">Return code</span></span>                                                                                             | <span data-ttu-id="55670-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="55670-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="55670-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55670-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="55670-122">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="55670-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="55670-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="55670-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="55670-124">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="55670-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="55670-125"><dt>**Digite \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="55670-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="55670-126">O parâmetro *itinfo* não é zero.</span><span class="sxs-lookup"><span data-stu-id="55670-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55670-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="55670-127">Remarks</span></span>

<span data-ttu-id="55670-128">Esse método se comporta como o método **IDispatch:: GetTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="55670-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="55670-129">No entanto, ele inclui um parâmetro adicional, *riid*, que especifica a interface para a qual recuperar informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="55670-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55670-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55670-130">Requirements</span></span>



| <span data-ttu-id="55670-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="55670-131">Requirement</span></span> | <span data-ttu-id="55670-132">Valor</span><span class="sxs-lookup"><span data-stu-id="55670-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55670-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55670-133">Header</span></span><br/>  | <dl> <span data-ttu-id="55670-134"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55670-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55670-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55670-135">Library</span></span><br/> | <dl> <span data-ttu-id="55670-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="55670-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55670-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="55670-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55670-138">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="55670-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




