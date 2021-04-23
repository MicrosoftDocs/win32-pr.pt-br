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
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909804"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="e6b41-103">Método CBaseControlWindow. DoSetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="e6b41-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="e6b41-104">O `DoSetWindowStyle` método altera os estilos de janela típicos ou estendidos.</span><span class="sxs-lookup"><span data-stu-id="e6b41-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6b41-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="e6b41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6b41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b41-107">*Estilo*</span><span class="sxs-lookup"><span data-stu-id="e6b41-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b41-108">Estilos de janela apropriados.</span><span class="sxs-lookup"><span data-stu-id="e6b41-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="e6b41-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="e6b41-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="e6b41-110">Valor que especifica quais estilos definir.</span><span class="sxs-lookup"><span data-stu-id="e6b41-110">Value specifying which styles to set.</span></span> <span data-ttu-id="e6b41-111">Deve ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="e6b41-111">Must be one of the following:</span></span>



| <span data-ttu-id="e6b41-112">Label</span><span class="sxs-lookup"><span data-stu-id="e6b41-112">Label</span></span> | <span data-ttu-id="e6b41-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e6b41-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="e6b41-114">estilo de GWL \_</span><span class="sxs-lookup"><span data-stu-id="e6b41-114">GWL\_STYLE</span></span>   | <span data-ttu-id="e6b41-115">Recupere os estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="e6b41-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="e6b41-116">GWL \_ FILEstyle</span><span class="sxs-lookup"><span data-stu-id="e6b41-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="e6b41-117">Recupere os estilos de janela estendida.</span><span class="sxs-lookup"><span data-stu-id="e6b41-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6b41-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6b41-118">Return value</span></span>

<span data-ttu-id="e6b41-119">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6b41-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6b41-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6b41-120">Remarks</span></span>

<span data-ttu-id="e6b41-121">Essa função de membro chama a função **SetWindowLong** do Win32 para definir o estilo da janela e, em seguida, exibe novamente a janela na posição atual.</span><span class="sxs-lookup"><span data-stu-id="e6b41-121">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="e6b41-122">Essa função de membro é chamada pelas funções de membro [**CBaseControlWindow::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p UT \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="e6b41-122">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b41-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6b41-123">Requirements</span></span>



| <span data-ttu-id="e6b41-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6b41-124">Requirement</span></span> | <span data-ttu-id="e6b41-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e6b41-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b41-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6b41-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e6b41-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b41-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6b41-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6b41-128">Library</span></span><br/> | <dl> <span data-ttu-id="e6b41-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e6b41-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b41-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6b41-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b41-131">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e6b41-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




