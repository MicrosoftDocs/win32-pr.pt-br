---
title: Mensagem de WM_CAP_FILE_SAVEAS (VFW. h)
description: A \_ \_ mensagem arquivo de salvamento da Cap do WM \_ copia o conteúdo do arquivo de captura para outro arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_SAVEAS
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369416"
---
# <a name="wm_cap_file_saveas-message"></a><span data-ttu-id="c3289-105">\_Mensagem de \_ salvamento de arquivo do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="c3289-105">WM\_CAP\_FILE\_SAVEAS message</span></span>

<span data-ttu-id="c3289-106">A **mensagem \_ \_ arquivo de \_ salvamento da Cap do WM** copia o conteúdo do arquivo de captura para outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="c3289-106">The **WM\_CAP\_FILE\_SAVEAS** message copies the contents of the capture file to another file.</span></span> <span data-ttu-id="c3289-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .</span><span class="sxs-lookup"><span data-stu-id="c3289-107">You can send this message explicitly or by using the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro.</span></span>


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="c3289-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3289-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3289-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="c3289-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="c3289-110">Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo de destino usado para copiar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c3289-110">Pointer to the null-terminated string that contains the name of the destination file used to copy the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3289-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c3289-111">Return Value</span></span>

<span data-ttu-id="c3289-112">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c3289-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="c3289-113">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="c3289-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3289-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3289-114">Remarks</span></span>

<span data-ttu-id="c3289-115">Essa mensagem não altera o nome ou o conteúdo do arquivo de captura atual.</span><span class="sxs-lookup"><span data-stu-id="c3289-115">This message does not change the name or contents of the current capture file.</span></span>

<span data-ttu-id="c3289-116">Se a operação de cópia não for bem-sucedida devido a um erro de disco cheio, o arquivo de destino será excluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c3289-116">If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.</span></span>

<span data-ttu-id="c3289-117">Normalmente, um arquivo de captura é pré-alocado para o maior segmento de captura previsto e apenas uma parte dele pode ser usada para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="c3289-117">Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="c3289-118">Essa mensagem copia apenas a parte do arquivo que contém os dados de captura.</span><span class="sxs-lookup"><span data-stu-id="c3289-118">This message copies only the portion of the file containing the capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3289-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3289-119">Requirements</span></span>



| <span data-ttu-id="c3289-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3289-120">Requirement</span></span> | <span data-ttu-id="c3289-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c3289-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c3289-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3289-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3289-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3289-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c3289-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3289-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3289-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3289-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c3289-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c3289-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3289-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3289-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3289-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3289-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3289-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c3289-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c3289-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c3289-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





