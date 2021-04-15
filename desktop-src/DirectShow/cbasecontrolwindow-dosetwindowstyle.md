---
description: O método DoSetWindowStyle altera os estilos de janela típicos ou estendidos.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Método CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747418"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="197b5-103">Método CBaseControlWindow. DoSetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="197b5-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="197b5-104">O `DoSetWindowStyle` método altera os estilos de janela típicos ou estendidos.</span><span class="sxs-lookup"><span data-stu-id="197b5-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="197b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="197b5-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="197b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="197b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="197b5-107">*Estilo*</span><span class="sxs-lookup"><span data-stu-id="197b5-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="197b5-108">Estilos de janela apropriados.</span><span class="sxs-lookup"><span data-stu-id="197b5-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="197b5-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="197b5-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="197b5-110">Valor que especifica quais estilos definir.</span><span class="sxs-lookup"><span data-stu-id="197b5-110">Value specifying which styles to set.</span></span> <span data-ttu-id="197b5-111">Deve ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="197b5-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="197b5-112">estilo de GWL \_</span><span class="sxs-lookup"><span data-stu-id="197b5-112">GWL\_STYLE</span></span>   | <span data-ttu-id="197b5-113">Recupere os estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="197b5-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="197b5-114">GWL \_ FILEstyle</span><span class="sxs-lookup"><span data-stu-id="197b5-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="197b5-115">Recupere os estilos de janela estendida.</span><span class="sxs-lookup"><span data-stu-id="197b5-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="197b5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="197b5-116">Return value</span></span>

<span data-ttu-id="197b5-117">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="197b5-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="197b5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="197b5-118">Remarks</span></span>

<span data-ttu-id="197b5-119">Essa função de membro chama a função **SetWindowLong** do Win32 para definir o estilo da janela e, em seguida, exibe novamente a janela na posição atual.</span><span class="sxs-lookup"><span data-stu-id="197b5-119">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="197b5-120">Essa função de membro é chamada pelas funções de membro [**CBaseControlWindow::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p UT \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="197b5-120">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="197b5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="197b5-121">Requirements</span></span>



| <span data-ttu-id="197b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="197b5-122">Requirement</span></span> | <span data-ttu-id="197b5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="197b5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197b5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="197b5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="197b5-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="197b5-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="197b5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="197b5-126">Library</span></span><br/> | <dl> <span data-ttu-id="197b5-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="197b5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197b5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="197b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197b5-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="197b5-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




