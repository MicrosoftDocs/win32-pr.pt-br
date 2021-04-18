---
description: 'O método SetPageSite Inicializa a página de propriedades e fornece um ponteiro para a interface IPropertyPageSite do quadro de propriedades. Esse método implementa o método IPropertyPage:: SetPageSite.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Método CBasePropertyPage. SetPageSite (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755606"
---
# <a name="cbasepropertypagesetpagesite-method"></a><span data-ttu-id="1147c-104">Método CBasePropertyPage. SetPageSite</span><span class="sxs-lookup"><span data-stu-id="1147c-104">CBasePropertyPage.SetPageSite method</span></span>

<span data-ttu-id="1147c-105">O `SetPageSite` método inicializa a página de propriedades e fornece um ponteiro para a interface **IPropertyPageSite** do quadro de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1147c-105">The `SetPageSite` method initializes the property page and provides a pointer to the property frame's **IPropertyPageSite** interface.</span></span> <span data-ttu-id="1147c-106">Esse método implementa o método **IPropertyPage:: SetPageSite** .</span><span class="sxs-lookup"><span data-stu-id="1147c-106">This method implements the **IPropertyPage::SetPageSite** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1147c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1147c-107">Syntax</span></span>


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a><span data-ttu-id="1147c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1147c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1147c-109">*pPageSite*</span><span class="sxs-lookup"><span data-stu-id="1147c-109">*pPageSite*</span></span> 
</dt> <dd>

<span data-ttu-id="1147c-110">Ponteiro para a interface **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="1147c-110">Pointer to the **IPropertyPageSite** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1147c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1147c-111">Return value</span></span>

<span data-ttu-id="1147c-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1147c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1147c-113">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="1147c-113">Possible values include the following.</span></span>



| <span data-ttu-id="1147c-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1147c-114">Return code</span></span>                                                                                  | <span data-ttu-id="1147c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1147c-115">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1147c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1147c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1147c-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="1147c-117">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="1147c-118"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="1147c-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="1147c-119">Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="1147c-119">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1147c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1147c-120">Remarks</span></span>

<span data-ttu-id="1147c-121">O método armazena o ponteiro *pPageSite* na variável de membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .</span><span class="sxs-lookup"><span data-stu-id="1147c-121">The method stores the *pPageSite* pointer in the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1147c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1147c-122">Requirements</span></span>



| <span data-ttu-id="1147c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1147c-123">Requirement</span></span> | <span data-ttu-id="1147c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1147c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1147c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1147c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1147c-126"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1147c-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1147c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1147c-127">Library</span></span><br/> | <dl> <span data-ttu-id="1147c-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1147c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1147c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1147c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1147c-130">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="1147c-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




