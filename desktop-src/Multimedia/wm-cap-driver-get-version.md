---
title: Mensagem de WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: A \_ \_ mensagem obter versão do driver do WM Cap \_ \_ retorna as informações de versão do driver de captura conectado a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_GET_VERSION
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755072"
---
# <a name="wm_cap_driver_get_version-message"></a><span data-ttu-id="d53b8-105">\_Mensagem de \_ obtenção \_ de \_ versão do driver do WM Cap</span><span class="sxs-lookup"><span data-stu-id="d53b8-105">WM\_CAP\_DRIVER\_GET\_VERSION message</span></span>

<span data-ttu-id="d53b8-106">A **mensagem \_ \_ \_ obter \_ versão do driver do WM Cap** retorna as informações de versão do driver de captura conectado a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="d53b8-106">The **WM\_CAP\_DRIVER\_GET\_VERSION** message returns the version information of the capture driver connected to a capture window.</span></span> <span data-ttu-id="d53b8-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .</span><span class="sxs-lookup"><span data-stu-id="d53b8-107">You can send this message explicitly or by using the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a><span data-ttu-id="d53b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d53b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d53b8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="d53b8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="d53b8-110">Tamanho, em bytes, do buffer definido pelo aplicativo referenciado por **szVer**.</span><span class="sxs-lookup"><span data-stu-id="d53b8-110">Size, in bytes, of the application-defined buffer referenced by **szVer**.</span></span>

</dd> <dt>

<span data-ttu-id="d53b8-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span><span class="sxs-lookup"><span data-stu-id="d53b8-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span></span>
</dt> <dd>

<span data-ttu-id="d53b8-112">Ponteiro para um buffer definido pelo aplicativo usado para retornar as informações de versão como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="d53b8-112">Pointer to an application-defined buffer used to return the version information as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d53b8-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d53b8-113">Return Value</span></span>

<span data-ttu-id="d53b8-114">Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="d53b8-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="d53b8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d53b8-115">Remarks</span></span>

<span data-ttu-id="d53b8-116">As informações de versão são uma cadeia de texto recuperada da área de recursos do driver.</span><span class="sxs-lookup"><span data-stu-id="d53b8-116">The version information is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="d53b8-117">Os aplicativos devem alocar aproximadamente 40 bytes para essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d53b8-117">Applications should allocate approximately 40 bytes for this string.</span></span> <span data-ttu-id="d53b8-118">Se as informações de versão não estiverem disponíveis, uma cadeia de caracteres **nula** será retornada.</span><span class="sxs-lookup"><span data-stu-id="d53b8-118">If version information is not available, a **NULL** string is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d53b8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d53b8-119">Requirements</span></span>



| <span data-ttu-id="d53b8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d53b8-120">Requirement</span></span> | <span data-ttu-id="d53b8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d53b8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d53b8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d53b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d53b8-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d53b8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d53b8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d53b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d53b8-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d53b8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d53b8-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d53b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d53b8-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d53b8-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d53b8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d53b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53b8-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d53b8-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d53b8-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d53b8-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





