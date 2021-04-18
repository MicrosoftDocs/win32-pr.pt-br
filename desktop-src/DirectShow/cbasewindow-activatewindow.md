---
description: O método ActivateWindow dimensiona a janela de acordo com os requisitos da classe derivada.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Método CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779561"
---
# <a name="cbasewindowactivatewindow-method"></a><span data-ttu-id="0a496-103">Método CBaseWindow. ActivateWindow</span><span class="sxs-lookup"><span data-stu-id="0a496-103">CBaseWindow.ActivateWindow method</span></span>

<span data-ttu-id="0a496-104">O `ActivateWindow` método dimensiona a janela de acordo com os requisitos da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="0a496-104">The `ActivateWindow` method sizes the window according to the requirements of the derived class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a496-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a496-105">Syntax</span></span>


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="0a496-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a496-106">Parameters</span></span>

<span data-ttu-id="0a496-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0a496-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a496-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a496-108">Return value</span></span>

<span data-ttu-id="0a496-109">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a496-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0a496-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0a496-110">Return code</span></span>                                                                             | <span data-ttu-id="0a496-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a496-111">Description</span></span>                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="0a496-112"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="0a496-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0a496-113">A janela já foi ativada.</span><span class="sxs-lookup"><span data-stu-id="0a496-113">Window was already activated.</span></span><br/> |
| <dl> <span data-ttu-id="0a496-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a496-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0a496-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0a496-115">Success.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="0a496-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a496-116">Remarks</span></span>

<span data-ttu-id="0a496-117">Esses métodos chamam o método [**CBaseWindow:: GetDefaultRect**](cbasewindow-getdefaultrect.md) para determinar o tamanho da janela.</span><span class="sxs-lookup"><span data-stu-id="0a496-117">This methods calls the [**CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) method to determine the window size.</span></span> <span data-ttu-id="0a496-118">A classe derivada deve substituir **GetDefaultRect** para retornar o tamanho das imagens que serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="0a496-118">The derived class should override **GetDefaultRect** to return the size of the images that will be displayed.</span></span>

<span data-ttu-id="0a496-119">Se a janela já estiver ativa, chamar `ActivateWindow` move a janela para a parte superior da ordem Z, mas não redimensiona a janela.</span><span class="sxs-lookup"><span data-stu-id="0a496-119">If the window is already active, calling `ActivateWindow` moves the window to the top of the Z order, but does not resize the window.</span></span> <span data-ttu-id="0a496-120">O mesmo será verdadeiro se a janela tiver um pai.</span><span class="sxs-lookup"><span data-stu-id="0a496-120">The same is true if the window has a parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a496-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a496-121">Requirements</span></span>



| <span data-ttu-id="0a496-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a496-122">Requirement</span></span> | <span data-ttu-id="0a496-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0a496-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a496-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a496-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0a496-125"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a496-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a496-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a496-126">Library</span></span><br/> | <dl> <span data-ttu-id="0a496-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0a496-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a496-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a496-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a496-129">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="0a496-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




