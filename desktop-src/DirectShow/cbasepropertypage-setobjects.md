---
description: 'O método SetObjects fornece ponteiros IUnknown para os objetos associados à página de propriedades. Esse método implementa o método IPropertyPage:: SetObjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Método CBasePropertyPage. SetObjects (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758244"
---
# <a name="cbasepropertypagesetobjects-method"></a><span data-ttu-id="63724-104">Método CBasePropertyPage. SetObjects</span><span class="sxs-lookup"><span data-stu-id="63724-104">CBasePropertyPage.SetObjects method</span></span>

<span data-ttu-id="63724-105">O `SetObjects` método fornece ponteiros **IUnknown** para os objetos associados à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="63724-105">The `SetObjects` method provides **IUnknown** pointers for the objects associated with the property page.</span></span> <span data-ttu-id="63724-106">Esse método implementa o método **IPropertyPage:: SetObjects** .</span><span class="sxs-lookup"><span data-stu-id="63724-106">This method implements the **IPropertyPage::SetObjects** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="63724-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63724-107">Syntax</span></span>


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a><span data-ttu-id="63724-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63724-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63724-109">*cObjects*</span><span class="sxs-lookup"><span data-stu-id="63724-109">*cObjects*</span></span> 
</dt> <dd>

<span data-ttu-id="63724-110">Especifica o número de ponteiros **IUnknown** na matriz especificada por *ppunk*.</span><span class="sxs-lookup"><span data-stu-id="63724-110">Specifies the number of **IUnknown** pointers in the array specified by *ppUnk*.</span></span>

</dd> <dt>

<span data-ttu-id="63724-111">*ppUnk*</span><span class="sxs-lookup"><span data-stu-id="63724-111">*ppUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="63724-112">Especifica uma matriz de ponteiros **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="63724-112">Specifies an array of **IUnknown** pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63724-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63724-113">Return value</span></span>

<span data-ttu-id="63724-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63724-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="63724-115">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="63724-115">Possible values include the following.</span></span>



| <span data-ttu-id="63724-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="63724-116">Return code</span></span>                                                                                  | <span data-ttu-id="63724-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="63724-117">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="63724-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63724-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="63724-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="63724-119">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="63724-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="63724-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="63724-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="63724-121">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="63724-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="63724-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="63724-123">Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="63724-123">Unexpected failure.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="63724-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="63724-124">Remarks</span></span>

<span data-ttu-id="63724-125">Embora *ppunk* especifique uma matriz de ponteiros **IUnknown** , a classe **CBasePropertyPage** é projetada apenas para dar suporte a um objeto associado.</span><span class="sxs-lookup"><span data-stu-id="63724-125">Although *ppUnk* specifies an array of **IUnknown** pointers, the **CBasePropertyPage** class is designed only to support one associated object.</span></span> <span data-ttu-id="63724-126">Se *CObjects* for maior que 1, o método retornará E será \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="63724-126">If *cObjects* is greater than 1, the method returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="63724-127">Se *CObjects* for igual a 1, esse método chamará o método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="63724-127">If *cObjects* equals 1, this method calls the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span> <span data-ttu-id="63724-128">Se *CObjects* for igual a 0, esse método chamará o método [**CBasePropertyPage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="63724-128">If *cObjects* equals 0, this method calls the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span> <span data-ttu-id="63724-129">A classe derivada deve substituir esses dois métodos; para obter detalhes, consulte os comentários para esses métodos.</span><span class="sxs-lookup"><span data-stu-id="63724-129">The derived class should override both of those methods; for details, see the remarks for those methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="63724-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63724-130">Requirements</span></span>



| <span data-ttu-id="63724-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="63724-131">Requirement</span></span> | <span data-ttu-id="63724-132">Valor</span><span class="sxs-lookup"><span data-stu-id="63724-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63724-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63724-133">Header</span></span><br/>  | <dl> <span data-ttu-id="63724-134"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63724-134"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="63724-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63724-135">Library</span></span><br/> | <dl> <span data-ttu-id="63724-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="63724-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63724-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="63724-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63724-138">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="63724-138">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




