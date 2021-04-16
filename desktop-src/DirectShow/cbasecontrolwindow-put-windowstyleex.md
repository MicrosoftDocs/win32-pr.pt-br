---
description: O \_ método Put WindowStyleEx define os estilos de janela estendidos.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Método de CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751277"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a><span data-ttu-id="bf96a-103">Método CBaseControlWindow. put \_ WindowStyleEx</span><span class="sxs-lookup"><span data-stu-id="bf96a-103">CBaseControlWindow.put\_WindowStyleEx method</span></span>

<span data-ttu-id="bf96a-104">O `put_WindowStyleEx` método define os estilos de janela estendidos.</span><span class="sxs-lookup"><span data-stu-id="bf96a-104">The `put_WindowStyleEx` method sets the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf96a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf96a-105">Syntax</span></span>


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="bf96a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf96a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf96a-107">*WindowStyleEx* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf96a-107">*WindowStyleEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf96a-108">Valor que especifica o estilo da janela de controle.</span><span class="sxs-lookup"><span data-stu-id="bf96a-108">Value that specifies the style of the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf96a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf96a-109">Return value</span></span>

<span data-ttu-id="bf96a-110">Retorna NOERROR.</span><span class="sxs-lookup"><span data-stu-id="bf96a-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf96a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf96a-111">Remarks</span></span>

<span data-ttu-id="bf96a-112">Esse método usa estilos de janela estendidos.</span><span class="sxs-lookup"><span data-stu-id="bf96a-112">This method uses extended window styles.</span></span> <span data-ttu-id="bf96a-113">Para obter uma lista completa de estilos de janela estendidos, consulte a função **CreateWindowEx** do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="bf96a-113">For a complete list of extended window styles, see the Microsoft Win32 **CreateWindowEx** function.</span></span> <span data-ttu-id="bf96a-114">Para alterar o estilo da janela, recupere o estilo da janela atual e, em seguida, adicione ou remova os campos de bits necessários.</span><span class="sxs-lookup"><span data-stu-id="bf96a-114">To change the window style, retrieve the current window style, and then add or remove the necessary bit fields.</span></span>

<span data-ttu-id="bf96a-115">Não use os estilos de janela a seguir porque eles não são validados.</span><span class="sxs-lookup"><span data-stu-id="bf96a-115">Do not use the following window styles because they are not validated.</span></span>

-   <span data-ttu-id="bf96a-116">WS \_ desabilitado</span><span class="sxs-lookup"><span data-stu-id="bf96a-116">WS\_DISABLED</span></span>
-   <span data-ttu-id="bf96a-117">WS \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="bf96a-117">WS\_HSCROLL</span></span>
-   <span data-ttu-id="bf96a-118">WS \_ icônico</span><span class="sxs-lookup"><span data-stu-id="bf96a-118">WS\_ICONIC</span></span>
-   <span data-ttu-id="bf96a-119">WS \_ maximize</span><span class="sxs-lookup"><span data-stu-id="bf96a-119">WS\_MAXIMIZE</span></span>
-   <span data-ttu-id="bf96a-120">\_minimizar WS</span><span class="sxs-lookup"><span data-stu-id="bf96a-120">WS\_MINIMIZE</span></span>
-   <span data-ttu-id="bf96a-121">WS \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="bf96a-121">WS\_VSCROLL</span></span>

<span data-ttu-id="bf96a-122">Com algumas exceções (anotadas aqui), os sinalizadores aceitáveis são os mesmos que os permitidos pela função **CreateWindow** do Win32.</span><span class="sxs-lookup"><span data-stu-id="bf96a-122">With some exceptions (noted here), the acceptable flags are the same as those allowed by the Win32 **CreateWindow** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf96a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf96a-123">Requirements</span></span>



| <span data-ttu-id="bf96a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf96a-124">Requirement</span></span> | <span data-ttu-id="bf96a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bf96a-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf96a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf96a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bf96a-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf96a-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf96a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf96a-128">Library</span></span><br/> | <dl> <span data-ttu-id="bf96a-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bf96a-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf96a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf96a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf96a-131">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="bf96a-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




