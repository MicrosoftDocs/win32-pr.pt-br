---
title: Mensagem de WM_CAP_PAL_OPEN (VFW. h)
description: A mensagem do WM \_ Cap \_ PAL \_ Open carrega uma nova paleta de um arquivo de paleta e a transmite para um driver de captura.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- Multimídia do Windows de mensagem WM_CAP_PAL_OPEN
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770371"
---
# <a name="wm_cap_pal_open-message"></a><span data-ttu-id="800b3-104">\_Mensagem de \_ abertura da PAL do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="800b3-104">WM\_CAP\_PAL\_OPEN message</span></span>

<span data-ttu-id="800b3-105">A mensagem do **WM \_ Cap \_ PAL \_ Open** carrega uma nova paleta de um arquivo de paleta e a transmite para um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="800b3-105">The **WM\_CAP\_PAL\_OPEN** message loads a new palette from a palette file and passes it to a capture driver.</span></span> <span data-ttu-id="800b3-106">Os arquivos de paleta normalmente usam a extensão de nome de arquivo. Amigo.</span><span class="sxs-lookup"><span data-stu-id="800b3-106">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="800b3-107">Um driver de captura usa uma paleta quando exigido pelo formato de imagem digitalizada especificado.</span><span class="sxs-lookup"><span data-stu-id="800b3-107">A capture driver uses a palette when required by the specified digitized image format.</span></span> <span data-ttu-id="800b3-108">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .</span><span class="sxs-lookup"><span data-stu-id="800b3-108">You can send this message explicitly or by using the [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro.</span></span>


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="800b3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="800b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="800b3-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="800b3-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="800b3-111">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome de arquivo da paleta.</span><span class="sxs-lookup"><span data-stu-id="800b3-111">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="800b3-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="800b3-112">Return Value</span></span>

<span data-ttu-id="800b3-113">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="800b3-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="800b3-114">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="800b3-114">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="800b3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="800b3-115">Requirements</span></span>



| <span data-ttu-id="800b3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="800b3-116">Requirement</span></span> | <span data-ttu-id="800b3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="800b3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="800b3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="800b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="800b3-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="800b3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="800b3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="800b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="800b3-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="800b3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="800b3-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="800b3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="800b3-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="800b3-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800b3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="800b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800b3-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="800b3-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="800b3-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="800b3-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





