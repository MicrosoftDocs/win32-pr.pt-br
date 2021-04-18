---
title: Mensagem de WM_CAP_PAL_SAVE (VFW. h)
description: A \_ mensagem de salvamento da PAL Cap do WM \_ \_ salva a paleta atual em um arquivo de paleta. Os arquivos de paleta normalmente usam a extensão de nome de arquivo. Amigo. Você pode enviar essa mensagem explicitamente ou usando a macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- Multimídia do Windows de mensagem WM_CAP_PAL_SAVE
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758946"
---
# <a name="wm_cap_pal_save-message"></a><span data-ttu-id="503e2-106">\_Mensagem de \_ salvamento da PAL Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="503e2-106">WM\_CAP\_PAL\_SAVE message</span></span>

<span data-ttu-id="503e2-107">A mensagem de **\_ \_ \_ salvamento da PAL Cap do WM** salva a paleta atual em um arquivo de paleta.</span><span class="sxs-lookup"><span data-stu-id="503e2-107">The **WM\_CAP\_PAL\_SAVE** message saves the current palette to a palette file.</span></span> <span data-ttu-id="503e2-108">Os arquivos de paleta normalmente usam a extensão de nome de arquivo. Amigo.</span><span class="sxs-lookup"><span data-stu-id="503e2-108">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="503e2-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .</span><span class="sxs-lookup"><span data-stu-id="503e2-109">You can send this message explicitly or by using the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro.</span></span>


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="503e2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="503e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="503e2-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="503e2-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="503e2-112">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome de arquivo da paleta.</span><span class="sxs-lookup"><span data-stu-id="503e2-112">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="503e2-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="503e2-113">Return Value</span></span>

<span data-ttu-id="503e2-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="503e2-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="503e2-115">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="503e2-115">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="503e2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="503e2-116">Requirements</span></span>



| <span data-ttu-id="503e2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="503e2-117">Requirement</span></span> | <span data-ttu-id="503e2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="503e2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="503e2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="503e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="503e2-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="503e2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="503e2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="503e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="503e2-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="503e2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="503e2-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="503e2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="503e2-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="503e2-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="503e2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="503e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503e2-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="503e2-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="503e2-127">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="503e2-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





