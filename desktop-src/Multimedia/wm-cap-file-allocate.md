---
title: Mensagem de WM_CAP_FILE_ALLOCATE (VFW. h)
description: A \_ mensagem de alocação de arquivo do WM Cap \_ \_ cria (prefixa) um arquivo de captura de um tamanho especificado. Você pode enviar essa mensagem explicitamente ou usando a macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_ALLOCATE
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454859"
---
# <a name="wm_cap_file_allocate-message"></a><span data-ttu-id="c9da6-105">\_Mensagem de \_ alocação de arquivo do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="c9da6-105">WM\_CAP\_FILE\_ALLOCATE message</span></span>

<span data-ttu-id="c9da6-106">A mensagem de **\_ \_ \_ alocação de arquivo do WM Cap** cria (prefixa) um arquivo de captura de um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="c9da6-106">The **WM\_CAP\_FILE\_ALLOCATE** message creates (preallocates) a capture file of a specified size.</span></span> <span data-ttu-id="c9da6-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .</span><span class="sxs-lookup"><span data-stu-id="c9da6-107">You can send this message explicitly or by using the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro.</span></span>


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a><span data-ttu-id="c9da6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9da6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9da6-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span><span class="sxs-lookup"><span data-stu-id="c9da6-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span></span>
</dt> <dd>

<span data-ttu-id="c9da6-110">Tamanho, em bytes, para criar o arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="c9da6-110">Size, in bytes, to create the capture file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9da6-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c9da6-111">Return Value</span></span>

<span data-ttu-id="c9da6-112">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c9da6-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="c9da6-113">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="c9da6-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9da6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9da6-114">Remarks</span></span>

<span data-ttu-id="c9da6-115">Você pode melhorar significativamente o desempenho da captura de fluxo ao alocar um arquivo de captura grande o suficiente para armazenar um clipe de vídeo inteiro e desfragmentar o arquivo de captura antes de capturar o clipe.</span><span class="sxs-lookup"><span data-stu-id="c9da6-115">You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9da6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9da6-116">Requirements</span></span>



| <span data-ttu-id="c9da6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9da6-117">Requirement</span></span> | <span data-ttu-id="c9da6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c9da6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9da6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9da6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9da6-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9da6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9da6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9da6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9da6-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9da6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9da6-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9da6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9da6-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9da6-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9da6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9da6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9da6-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c9da6-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c9da6-127">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c9da6-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





