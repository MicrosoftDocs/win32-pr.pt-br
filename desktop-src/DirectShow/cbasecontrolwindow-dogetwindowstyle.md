---
description: O método DoGetWindowStyle recupera os estilos de janela normais ou estendidos atuais.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778648"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="a6bf1-103">Método CBaseControlWindow. DoGetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="a6bf1-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="a6bf1-104">O `DoGetWindowStyle` método recupera os estilos de janela normal ou estendida atuais.</span><span class="sxs-lookup"><span data-stu-id="a6bf1-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bf1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6bf1-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="a6bf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6bf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bf1-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="a6bf1-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bf1-108">Ponteiro para uma variável que recebe as informações de estilo.</span><span class="sxs-lookup"><span data-stu-id="a6bf1-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="a6bf1-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="a6bf1-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bf1-110">Valor que especifica quais estilos recuperar.</span><span class="sxs-lookup"><span data-stu-id="a6bf1-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="a6bf1-111">Deve ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="a6bf1-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="a6bf1-112">estilo de GWL \_</span><span class="sxs-lookup"><span data-stu-id="a6bf1-112">GWL\_STYLE</span></span>   | <span data-ttu-id="a6bf1-113">Recupere os estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="a6bf1-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="a6bf1-114">GWL \_ FILEstyle</span><span class="sxs-lookup"><span data-stu-id="a6bf1-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="a6bf1-115">Recupere os estilos de janela estendida.</span><span class="sxs-lookup"><span data-stu-id="a6bf1-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bf1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6bf1-116">Return value</span></span>

<span data-ttu-id="a6bf1-117">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6bf1-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6bf1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6bf1-118">Remarks</span></span>

<span data-ttu-id="a6bf1-119">Essa função de membro chama a função **GetWindowLong** do Win32 para recuperar o estilo da janela.</span><span class="sxs-lookup"><span data-stu-id="a6bf1-119">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="a6bf1-120">Ele é chamado pelas funções membro [**CBaseControlWindow:: get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow:: get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="a6bf1-120">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6bf1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6bf1-121">Requirements</span></span>



| <span data-ttu-id="a6bf1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6bf1-122">Requirement</span></span> | <span data-ttu-id="a6bf1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a6bf1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bf1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6bf1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a6bf1-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6bf1-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a6bf1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6bf1-126">Library</span></span><br/> | <dl> <span data-ttu-id="a6bf1-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a6bf1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6bf1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6bf1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bf1-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="a6bf1-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




