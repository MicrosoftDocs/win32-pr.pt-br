---
title: Mensagem de WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: A mensagem do arquivo de captura do conjunto de arquivos do WM \_ Cap \_ \_ \_ \_ nomeia o arquivo usado para captura de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_SET_CAPTURE_FILE
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917967"
---
# <a name="wm_cap_file_set_capture_file-message"></a><span data-ttu-id="3c737-105">\_Mensagem do \_ \_ arquivo de captura do conjunto de arquivos do \_ WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="3c737-105">WM\_CAP\_FILE\_SET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="3c737-106">A mensagem do **arquivo de captura do conjunto de arquivos do WM \_ Cap \_ \_ \_ \_** nomeia o arquivo usado para captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3c737-106">The **WM\_CAP\_FILE\_SET\_CAPTURE\_FILE** message names the file used for video capture.</span></span> <span data-ttu-id="3c737-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="3c737-107">You can send this message explicitly or by using the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="3c737-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c737-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c737-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="3c737-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="3c737-110">Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo de captura a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3c737-110">Pointer to the null-terminated string that contains the name of the capture file to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c737-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3c737-111">Return Value</span></span>

<span data-ttu-id="3c737-112">Retornará **true** se for bem-sucedido ou **false** se o nome de arquivo for inválido ou se a captura de streaming ou de quadro único estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="3c737-112">Returns **TRUE** if successful or **FALSE** if the filename is invalid, or if streaming or single-frame capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c737-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c737-113">Remarks</span></span>

<span data-ttu-id="3c737-114">Essa mensagem armazena o nome de arquivo em uma estrutura interna.</span><span class="sxs-lookup"><span data-stu-id="3c737-114">This message stores the filename in an internal structure.</span></span> <span data-ttu-id="3c737-115">Ele não cria, aloca ou abre o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3c737-115">It does not create, allocate, or open the specified file.</span></span> <span data-ttu-id="3c737-116">O nome de arquivo de captura padrão é C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="3c737-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c737-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c737-117">Requirements</span></span>



| <span data-ttu-id="3c737-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c737-118">Requirement</span></span> | <span data-ttu-id="3c737-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3c737-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c737-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c737-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c737-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c737-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c737-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c737-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c737-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c737-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c737-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3c737-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c737-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c737-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c737-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c737-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c737-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3c737-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3c737-128">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3c737-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





