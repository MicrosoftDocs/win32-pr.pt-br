---
title: Mensagem de MCIWNDM_REALIZE (VFW. h)
description: A \_ mensagem MCIWNDM percebe que a paleta é usada atualmente pelo dispositivo MCI em uma janela MCIWnd. Essa macro é definida com a mensagem de MCIWNDM de \_ percepção. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- Multimídia do Windows de mensagem MCIWNDM_REALIZE
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918054"
---
# <a name="mciwndm_realize-message"></a><span data-ttu-id="7b4e1-106">MCIWNDM \_ perceber mensagem</span><span class="sxs-lookup"><span data-stu-id="7b4e1-106">MCIWNDM\_REALIZE message</span></span>

<span data-ttu-id="7b4e1-107">A mensagem **MCIWNDM \_ percebe** que a paleta é usada atualmente pelo dispositivo MCI em uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-107">The **MCIWNDM\_REALIZE** message realizes the palette currently used by the MCI device in an MCIWnd window.</span></span> <span data-ttu-id="7b4e1-108">Essa macro é definida com a mensagem de **MCIWNDM de \_ percepção** .</span><span class="sxs-lookup"><span data-stu-id="7b4e1-108">This macro is defined with the **MCIWNDM\_REALIZE** message.</span></span> <span data-ttu-id="7b4e1-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="7b4e1-109">You can send this message explicitly or by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span>


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="7b4e1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b4e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4e1-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span><span class="sxs-lookup"><span data-stu-id="7b4e1-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span></span>
</dt> <dd>

<span data-ttu-id="7b4e1-112">Sinalizador de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-112">Background flag.</span></span> <span data-ttu-id="7b4e1-113">Especifique **true** para este parâmetro se a janela for um aplicativo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-113">Specify **TRUE** for this parameter if the window is a background application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4e1-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7b4e1-114">Return Value</span></span>

<span data-ttu-id="7b4e1-115">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-115">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4e1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b4e1-116">Remarks</span></span>

<span data-ttu-id="7b4e1-117">**MCIWNDM \_ A CONCRETIZAção** usa a paleta do dispositivo MCI e chama a função [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) .</span><span class="sxs-lookup"><span data-stu-id="7b4e1-117">**MCIWNDM\_REALIZE** uses the palette of the MCI device and calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function.</span></span> <span data-ttu-id="7b4e1-118">Se seu aplicativo manipula explicitamente as mensagens da [**\_ paletachanged do WM**](/windows/desktop/gdi/wm-palettechanged) e do [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , você deve usar essa mensagem em seu aplicativo em vez de usar **RealizePalette**.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-118">If your application explicitly handles the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages, you should use this message in your application instead of using **RealizePalette**.</span></span> <span data-ttu-id="7b4e1-119">Se o corpo de um desses manipuladores de mensagens contiver apenas **RealizePalette**, encaminhe a mensagem para a janela MCIWnd, que irá perceber automaticamente a paleta.</span><span class="sxs-lookup"><span data-stu-id="7b4e1-119">If the body of one of these message handlers contains only **RealizePalette**, forward the message to the MCIWnd window, which will automatically realize the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4e1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b4e1-120">Requirements</span></span>



| <span data-ttu-id="7b4e1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b4e1-121">Requirement</span></span> | <span data-ttu-id="7b4e1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7b4e1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7b4e1-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b4e1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4e1-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b4e1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7b4e1-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b4e1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4e1-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b4e1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b4e1-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7b4e1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b4e1-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b4e1-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4e1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b4e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4e1-130">**MCIWndRealize**</span><span class="sxs-lookup"><span data-stu-id="7b4e1-130">**MCIWndRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[<span data-ttu-id="7b4e1-131">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="7b4e1-131">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="7b4e1-132">**paleta do WMchanged \_**</span><span class="sxs-lookup"><span data-stu-id="7b4e1-132">**WM\_PALETTECHANGED**</span></span>](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[<span data-ttu-id="7b4e1-133">**QUERYNEWPALETTE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7b4e1-133">**WM\_QUERYNEWPALETTE**</span></span>](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

