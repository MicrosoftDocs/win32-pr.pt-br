---
title: Mensagem de WM_CAP_DRIVER_CONNECT (VFW. h)
description: A mensagem de conexão do driver do WM \_ Cap \_ \_ conecta uma janela de captura a um driver de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_CONNECT
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369522"
---
# <a name="wm_cap_driver_connect-message"></a><span data-ttu-id="ba6f2-105">\_Mensagem de \_ conexão de driver do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="ba6f2-105">WM\_CAP\_DRIVER\_CONNECT message</span></span>

<span data-ttu-id="ba6f2-106">A mensagem de **\_ conexão do \_ Driver \_ do WM Cap** conecta uma janela de captura a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="ba6f2-106">The **WM\_CAP\_DRIVER\_CONNECT** message connects a capture window to a capture driver.</span></span> <span data-ttu-id="ba6f2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .</span><span class="sxs-lookup"><span data-stu-id="ba6f2-107">You can send this message explicitly or by using the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="ba6f2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba6f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba6f2-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="ba6f2-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="ba6f2-110">Índice do driver de captura.</span><span class="sxs-lookup"><span data-stu-id="ba6f2-110">Index of the capture driver.</span></span> <span data-ttu-id="ba6f2-111">O índice pode variar de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="ba6f2-111">The index can range from 0 through 9.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba6f2-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ba6f2-112">Return Value</span></span>

<span data-ttu-id="ba6f2-113">Retornará **true** se for bem-sucedido ou **false** se o driver de captura especificado não puder ser conectado à janela de captura.</span><span class="sxs-lookup"><span data-stu-id="ba6f2-113">Returns **TRUE** if successful or **FALSE** if the specified capture driver cannot be connected to the capture window.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba6f2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba6f2-114">Remarks</span></span>

<span data-ttu-id="ba6f2-115">Conectar um driver de captura a uma janela de captura desconecta automaticamente qualquer driver de captura conectado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba6f2-115">Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba6f2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba6f2-116">Requirements</span></span>



| <span data-ttu-id="ba6f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba6f2-117">Requirement</span></span> | <span data-ttu-id="ba6f2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ba6f2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ba6f2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba6f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba6f2-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba6f2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ba6f2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba6f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba6f2-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba6f2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ba6f2-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba6f2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba6f2-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba6f2-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba6f2-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ba6f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba6f2-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ba6f2-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ba6f2-127">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ba6f2-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





