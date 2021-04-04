---
title: Mensagem de WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: A mensagem do arquivo de captura do arquivo do WM \_ Cap \_ \_ \_ \_ retorna o nome do arquivo de captura atual. Você pode enviar essa mensagem explicitamente ou usando a macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_GET_CAPTURE_FILE
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824215"
---
# <a name="wm_cap_file_get_capture_file-message"></a><span data-ttu-id="cf553-105">\_Mensagem do \_ \_ arquivo de obtenção de \_ captura de arquivo \_ do WM Cap</span><span class="sxs-lookup"><span data-stu-id="cf553-105">WM\_CAP\_FILE\_GET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="cf553-106">A mensagem do arquivo de **\_ \_ \_ \_ captura \_** do arquivo do WM Cap retorna o nome do arquivo de captura atual.</span><span class="sxs-lookup"><span data-stu-id="cf553-106">The **WM\_CAP\_FILE\_GET\_CAPTURE\_FILE** message returns the name of the current capture file.</span></span> <span data-ttu-id="cf553-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="cf553-107">You can send this message explicitly or by using the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="cf553-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf553-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf553-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="cf553-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="cf553-110">Tamanho, em bytes, do buffer definido pelo aplicativo referenciado por **szName**.</span><span class="sxs-lookup"><span data-stu-id="cf553-110">Size, in bytes, of the application-defined buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="cf553-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="cf553-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="cf553-112">Ponteiro para um buffer definido pelo aplicativo usado para retornar o nome do arquivo de captura como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="cf553-112">Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf553-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cf553-113">Return Value</span></span>

<span data-ttu-id="cf553-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cf553-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf553-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf553-115">Remarks</span></span>

<span data-ttu-id="cf553-116">O nome de arquivo de captura padrão é C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="cf553-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf553-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf553-117">Requirements</span></span>



| <span data-ttu-id="cf553-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf553-118">Requirement</span></span> | <span data-ttu-id="cf553-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cf553-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cf553-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf553-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cf553-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf553-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cf553-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf553-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cf553-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf553-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cf553-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf553-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf553-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf553-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf553-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf553-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf553-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="cf553-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="cf553-128">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="cf553-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





