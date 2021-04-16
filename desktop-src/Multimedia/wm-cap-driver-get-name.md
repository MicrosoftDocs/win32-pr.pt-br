---
title: Mensagem de WM_CAP_DRIVER_GET_NAME (VFW. h)
description: A \_ \_ \_ mensagem obter nome do driver do WM Cap \_ retorna o nome do driver de captura conectado à janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_GET_NAME
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454860"
---
# <a name="wm_cap_driver_get_name-message"></a><span data-ttu-id="c7334-105">\_Mensagem de \_ \_ nome Get do driver do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="c7334-105">WM\_CAP\_DRIVER\_GET\_NAME message</span></span>

<span data-ttu-id="c7334-106">A **mensagem \_ \_ \_ obter \_ nome do driver do WM Cap** retorna o nome do driver de captura conectado à janela de captura.</span><span class="sxs-lookup"><span data-stu-id="c7334-106">The **WM\_CAP\_DRIVER\_GET\_NAME** message returns the name of the capture driver connected to the capture window.</span></span> <span data-ttu-id="c7334-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .</span><span class="sxs-lookup"><span data-stu-id="c7334-107">You can send this message explicitly or by using the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="c7334-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7334-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7334-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="c7334-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="c7334-110">Tamanho, em bytes, do buffer referenciado por **szName**.</span><span class="sxs-lookup"><span data-stu-id="c7334-110">Size, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="c7334-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="c7334-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="c7334-112">Ponteiro para um buffer definido pelo aplicativo usado para retornar o nome do dispositivo como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="c7334-112">Pointer to an application-defined buffer used to return the device name as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7334-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c7334-113">Return Value</span></span>

<span data-ttu-id="c7334-114">Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="c7334-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7334-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7334-115">Remarks</span></span>

<span data-ttu-id="c7334-116">O nome é uma cadeia de caracteres de texto recuperada da área de recursos do driver.</span><span class="sxs-lookup"><span data-stu-id="c7334-116">The name is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="c7334-117">Os aplicativos devem alocar aproximadamente 80 bytes para essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c7334-117">Applications should allocate approximately 80 bytes for this string.</span></span> <span data-ttu-id="c7334-118">Se o driver não contiver um recurso de nome, o nome de caminho completo do driver listado no registro ou no arquivo de SYSTEM.INI será retornado.</span><span class="sxs-lookup"><span data-stu-id="c7334-118">If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7334-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7334-119">Requirements</span></span>



| <span data-ttu-id="c7334-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7334-120">Requirement</span></span> | <span data-ttu-id="c7334-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c7334-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c7334-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7334-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7334-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7334-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c7334-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7334-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7334-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7334-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c7334-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7334-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7334-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7334-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7334-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7334-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7334-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c7334-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c7334-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c7334-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





