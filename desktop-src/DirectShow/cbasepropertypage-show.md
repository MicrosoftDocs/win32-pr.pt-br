---
description: 'O método Show mostra ou oculta a caixa de diálogo. Esse método implementa o método IPropertyPage:: show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Método CBasePropertyPage. show (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754557"
---
# <a name="cbasepropertypageshow-method"></a><span data-ttu-id="c3705-104">Método CBasePropertyPage. show</span><span class="sxs-lookup"><span data-stu-id="c3705-104">CBasePropertyPage.Show method</span></span>

<span data-ttu-id="c3705-105">O `Show` método mostra ou oculta a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c3705-105">The `Show` method shows or hides the dialog box.</span></span> <span data-ttu-id="c3705-106">Esse método implementa o método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="c3705-106">This method implements the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3705-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3705-107">Syntax</span></span>

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a><span data-ttu-id="c3705-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3705-108">Parameters</span></span>

<span data-ttu-id="c3705-109">*nCmdShow*</span><span class="sxs-lookup"><span data-stu-id="c3705-109">*nCmdShow*</span></span>

<span data-ttu-id="c3705-110">Tipo: **[uint](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3705-110">Type: **[UINT](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3705-111">Valor que especifica se a janela deve ser mostrada ou ocultada.</span><span class="sxs-lookup"><span data-stu-id="c3705-111">Value that specifies whether to show or hide the window.</span></span> <span data-ttu-id="c3705-112">Para obter mais informações, consulte o método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="c3705-112">For more information, see the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3705-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3705-113">Return value</span></span>

<span data-ttu-id="c3705-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3705-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c3705-115">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="c3705-115">Possible values include the following.</span></span>

| <span data-ttu-id="c3705-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c3705-116">Return code</span></span>                                                                                  | <span data-ttu-id="c3705-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3705-117">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c3705-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c3705-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c3705-119">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="c3705-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c3705-121">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="c3705-121">Invalid argument.</span></span><br/>   |
| <dl> <span data-ttu-id="c3705-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c3705-123">Falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="c3705-123">Unexpected failure.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="c3705-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3705-124">Requirements</span></span>

| <span data-ttu-id="c3705-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3705-125">Requirement</span></span> | <span data-ttu-id="c3705-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c3705-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3705-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3705-127">Header</span></span>  | <dl> <span data-ttu-id="c3705-128"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-128"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c3705-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3705-129">Library</span></span> | <dl> <span data-ttu-id="c3705-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="c3705-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3705-131">See also</span></span>

[<span data-ttu-id="c3705-132">Classe CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="c3705-132">CBasePropertyPage Class</span></span>](cbasepropertypage.md)
