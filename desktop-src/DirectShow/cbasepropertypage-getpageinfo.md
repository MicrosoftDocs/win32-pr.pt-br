---
description: 'O método GetPageInfo recupera informações sobre a página de propriedades. Esse método implementa o método IPropertyPage:: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Método CBasePropertyPage. GetPageInfo (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757040"
---
# <a name="cbasepropertypagegetpageinfo-method"></a><span data-ttu-id="43ab8-104">Método CBasePropertyPage. GetPageInfo</span><span class="sxs-lookup"><span data-stu-id="43ab8-104">CBasePropertyPage.GetPageInfo method</span></span>

<span data-ttu-id="43ab8-105">O `GetPageInfo` método recupera informações sobre a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="43ab8-105">The `GetPageInfo` method retrieves information about the property page.</span></span> <span data-ttu-id="43ab8-106">Esse método implementa o método **IPropertyPage:: GetPageInfo** .</span><span class="sxs-lookup"><span data-stu-id="43ab8-106">This method implements the **IPropertyPage::GetPageInfo** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ab8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43ab8-107">Syntax</span></span>


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a><span data-ttu-id="43ab8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ab8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ab8-109">*pPageInfo*</span><span class="sxs-lookup"><span data-stu-id="43ab8-109">*pPageInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="43ab8-110">Ponteiro para uma estrutura **PROPPAGEINFO** alocada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="43ab8-110">Pointer to a caller-allocated **PROPPAGEINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ab8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43ab8-111">Return value</span></span>

<span data-ttu-id="43ab8-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43ab8-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="43ab8-113">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="43ab8-113">Possible values include the following.</span></span>



| <span data-ttu-id="43ab8-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="43ab8-114">Return code</span></span>                                                                                   | <span data-ttu-id="43ab8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="43ab8-115">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="43ab8-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43ab8-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="43ab8-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="43ab8-117">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="43ab8-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="43ab8-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="43ab8-119">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="43ab8-119">Insufficient memory.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43ab8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43ab8-120">Requirements</span></span>



| <span data-ttu-id="43ab8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43ab8-121">Requirement</span></span> | <span data-ttu-id="43ab8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="43ab8-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43ab8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43ab8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="43ab8-124"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43ab8-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="43ab8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43ab8-125">Library</span></span><br/> | <dl> <span data-ttu-id="43ab8-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="43ab8-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43ab8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="43ab8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ab8-128">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="43ab8-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




