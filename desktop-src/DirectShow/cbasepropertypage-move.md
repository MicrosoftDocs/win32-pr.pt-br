---
description: 'O método move posiciona e redimensiona a caixa de diálogo. Esse método implementa o método IPropertyPage:: move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Método CBasePropertyPage. Move (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750697"
---
# <a name="cbasepropertypagemove-method"></a><span data-ttu-id="5537b-104">Método CBasePropertyPage. move</span><span class="sxs-lookup"><span data-stu-id="5537b-104">CBasePropertyPage.Move method</span></span>

<span data-ttu-id="5537b-105">O `Move` método posiciona e redimensiona a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5537b-105">The `Move` method positions and resizes the dialog box.</span></span> <span data-ttu-id="5537b-106">Esse método implementa o método **IPropertyPage:: move** .</span><span class="sxs-lookup"><span data-stu-id="5537b-106">This method implements the **IPropertyPage::Move** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5537b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5537b-107">Syntax</span></span>


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a><span data-ttu-id="5537b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5537b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5537b-109">*prect*</span><span class="sxs-lookup"><span data-stu-id="5537b-109">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="5537b-110">Ponteiro para uma estrutura **Rect** que contém as informações de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="5537b-110">Pointer to a **RECT** structure containing the positioning information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5537b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5537b-111">Return value</span></span>

<span data-ttu-id="5537b-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5537b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5537b-113">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="5537b-113">Possible values include the following.</span></span>



| <span data-ttu-id="5537b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5537b-114">Return code</span></span>                                                                                  | <span data-ttu-id="5537b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5537b-115">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5537b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5537b-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5537b-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5537b-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="5537b-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5537b-118"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="5537b-119">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5537b-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="5537b-120"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="5537b-120"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="5537b-121">Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="5537b-121">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="5537b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5537b-122">Requirements</span></span>



| <span data-ttu-id="5537b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5537b-123">Requirement</span></span> | <span data-ttu-id="5537b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5537b-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5537b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5537b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5537b-126"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5537b-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5537b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5537b-127">Library</span></span><br/> | <dl> <span data-ttu-id="5537b-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5537b-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5537b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5537b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5537b-130">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="5537b-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




