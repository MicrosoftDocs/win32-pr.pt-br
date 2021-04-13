---
title: Mensagem de WM_CAP_FILE_SAVEDIB (VFW. h)
description: A \_ mensagem do arquivo SAVEDIB do WM Cap \_ \_ copia o quadro atual para um arquivo DIB. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_SAVEDIB
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455927"
---
# <a name="wm_cap_file_savedib-message"></a><span data-ttu-id="0da5a-105">\_ \_ Mensagem SAVEDIB do arquivo do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="0da5a-105">WM\_CAP\_FILE\_SAVEDIB message</span></span>

<span data-ttu-id="0da5a-106">A mensagem do **\_ \_ arquivo \_ SAVEDIB do WM Cap** copia o quadro atual para um arquivo DIB.</span><span class="sxs-lookup"><span data-stu-id="0da5a-106">The **WM\_CAP\_FILE\_SAVEDIB** message copies the current frame to a DIB file.</span></span> <span data-ttu-id="0da5a-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .</span><span class="sxs-lookup"><span data-stu-id="0da5a-107">You can send this message explicitly or by using the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro.</span></span>


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="0da5a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0da5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da5a-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="0da5a-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="0da5a-110">Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo DIB de destino.</span><span class="sxs-lookup"><span data-stu-id="0da5a-110">Pointer to the null-terminated string that contains the name of the destination DIB file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da5a-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0da5a-111">Return Value</span></span>

<span data-ttu-id="0da5a-112">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0da5a-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="0da5a-113">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="0da5a-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="0da5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0da5a-114">Remarks</span></span>

<span data-ttu-id="0da5a-115">Se o driver de captura fornecer quadros em um formato compactado, essa chamada tentará descompactar o quadro antes de gravar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0da5a-115">If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da5a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0da5a-116">Requirements</span></span>



| <span data-ttu-id="0da5a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0da5a-117">Requirement</span></span> | <span data-ttu-id="0da5a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0da5a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0da5a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0da5a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0da5a-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0da5a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0da5a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0da5a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0da5a-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0da5a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0da5a-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0da5a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0da5a-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0da5a-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da5a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0da5a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da5a-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0da5a-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0da5a-127">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0da5a-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





