---
title: Mensagem de WM_CAP_PAL_PASTE (VFW. h)
description: A mensagem do WM \_ Cap \_ PAL \_ Paste copia a paleta da área de transferência e a transmite para um driver de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- Multimídia do Windows de mensagem WM_CAP_PAL_PASTE
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918248"
---
# <a name="wm_cap_pal_paste-message"></a><span data-ttu-id="83be0-105">\_Mensagem de \_ colagem da PAL do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="83be0-105">WM\_CAP\_PAL\_PASTE message</span></span>

<span data-ttu-id="83be0-106">A mensagem do **WM \_ Cap \_ PAL \_ Paste** copia a paleta da área de transferência e a transmite para um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="83be0-106">The **WM\_CAP\_PAL\_PASTE** message copies the palette from the clipboard and passes it to a capture driver.</span></span> <span data-ttu-id="83be0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .</span><span class="sxs-lookup"><span data-stu-id="83be0-107">You can send this message explicitly or by using the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) macro.</span></span>


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="83be0-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="83be0-108">Return Value</span></span>

<span data-ttu-id="83be0-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="83be0-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="83be0-110">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="83be0-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="83be0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="83be0-111">Remarks</span></span>

<span data-ttu-id="83be0-112">Um driver de captura usa uma paleta quando exigido pelo formato de vídeo digitalizado especificado.</span><span class="sxs-lookup"><span data-stu-id="83be0-112">A capture driver uses a palette when required by the specified digitized video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="83be0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83be0-113">Requirements</span></span>



| <span data-ttu-id="83be0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="83be0-114">Requirement</span></span> | <span data-ttu-id="83be0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="83be0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="83be0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83be0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="83be0-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83be0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="83be0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83be0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="83be0-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83be0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="83be0-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="83be0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="83be0-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="83be0-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83be0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="83be0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83be0-123">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="83be0-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="83be0-124">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="83be0-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





