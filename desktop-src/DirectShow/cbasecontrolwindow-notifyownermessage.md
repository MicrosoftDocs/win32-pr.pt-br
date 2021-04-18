---
description: O método NotifyOwnerMessage passa mensagens específicas para a janela de vídeo.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Método CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752306"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a><span data-ttu-id="b110f-103">Método CBaseControlWindow. NotifyOwnerMessage</span><span class="sxs-lookup"><span data-stu-id="b110f-103">CBaseControlWindow.NotifyOwnerMessage method</span></span>

<span data-ttu-id="b110f-104">O `NotifyOwnerMessage` método passa mensagens específicas para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b110f-104">The `NotifyOwnerMessage` method passes along specific messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b110f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b110f-105">Syntax</span></span>


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a><span data-ttu-id="b110f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b110f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b110f-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b110f-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b110f-108">Identificador para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b110f-108">Handle to the video window.</span></span>

</dd> <dt>

<span data-ttu-id="b110f-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="b110f-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b110f-110">Detalhes da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b110f-110">Message details.</span></span>

</dd> <dt>

<span data-ttu-id="b110f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b110f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b110f-112">Primeiro parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b110f-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b110f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b110f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b110f-114">Segundo parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b110f-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b110f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b110f-115">Return value</span></span>

<span data-ttu-id="b110f-116">Não retorna nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="b110f-116">Returns NO\_ERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b110f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b110f-117">Remarks</span></span>

<span data-ttu-id="b110f-118">Quando a janela de vídeo é um filho de outra janela, ela não recebe determinadas mensagens de janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="b110f-118">When the video window is a child of another window, it does not receive certain top-level window messages.</span></span> <span data-ttu-id="b110f-119">Essas mensagens podem ser valiosas para um processador, pois podem afetar seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="b110f-119">These messages can be valuable to a renderer, because they could affect its behavior.</span></span> <span data-ttu-id="b110f-120">`NotifyOwnerMessage` passa qualquer uma das mensagens a seguir para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b110f-120">`NotifyOwnerMessage` passes any of the following messages to the video window.</span></span>

-   <span data-ttu-id="b110f-121">ACTIVATEAPP do WM \_</span><span class="sxs-lookup"><span data-stu-id="b110f-121">WM\_ACTIVATEAPP</span></span>
-   <span data-ttu-id="b110f-122">DEVMODECHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="b110f-122">WM\_DEVMODECHANGE</span></span>
-   <span data-ttu-id="b110f-123">DISPLAYCHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="b110f-123">WM\_DISPLAYCHANGE</span></span>
-   <span data-ttu-id="b110f-124">paleta do WMchanged \_</span><span class="sxs-lookup"><span data-stu-id="b110f-124">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="b110f-125">PALETTEISCHANGING do WM \_</span><span class="sxs-lookup"><span data-stu-id="b110f-125">WM\_PALETTEISCHANGING</span></span>
-   <span data-ttu-id="b110f-126">QUERYNEWPALETTE do WM \_</span><span class="sxs-lookup"><span data-stu-id="b110f-126">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="b110f-127">SYSCOLORCHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="b110f-127">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="b110f-128">Você pode solicitar que o [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) de plug-in (PID) de um Windows faça uma janela se torne um filho de outra janela.</span><span class="sxs-lookup"><span data-stu-id="b110f-128">You can request that the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor (PID) make a window become a child of another window.</span></span> <span data-ttu-id="b110f-129">Quando isso ocorrer, o PID procurará determinadas mensagens que podem ser enviadas para a janela proprietária.</span><span class="sxs-lookup"><span data-stu-id="b110f-129">When this occurs, the PID will look for certain messages that might be sent to the owning window.</span></span> <span data-ttu-id="b110f-130">Em seguida, o PID encaminhará essas mensagens para a janela de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b110f-130">The PID will then forward those messages to the owned window.</span></span> <span data-ttu-id="b110f-131">O processamento padrão para as mensagens é enviá-las ao procedimento de janela de propriedade de forma síncrona chamando a função **SendMessage** do Win32.</span><span class="sxs-lookup"><span data-stu-id="b110f-131">The default processing for the messages is to send them to the owned window procedure synchronously by calling the Win32 **SendMessage** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b110f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b110f-132">Requirements</span></span>



| <span data-ttu-id="b110f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b110f-133">Requirement</span></span> | <span data-ttu-id="b110f-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b110f-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b110f-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b110f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b110f-136"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b110f-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b110f-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b110f-137">Library</span></span><br/> | <dl> <span data-ttu-id="b110f-138"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b110f-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b110f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b110f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b110f-140">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="b110f-140">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




