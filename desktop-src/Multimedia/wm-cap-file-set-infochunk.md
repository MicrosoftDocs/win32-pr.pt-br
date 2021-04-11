---
title: Mensagem de WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: O arquivo do WM \_ Cap \_ \_ set \_ INFOCHUNK Message define e limpa as partes de informações.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_SET_INFOCHUNK
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008894"
---
# <a name="wm_cap_file_set_infochunk-message"></a><span data-ttu-id="b3097-104">\_Mensagem de \_ INFOCHUNK do conjunto de arquivos \_ \_ do WM Cap</span><span class="sxs-lookup"><span data-stu-id="b3097-104">WM\_CAP\_FILE\_SET\_INFOCHUNK message</span></span>

<span data-ttu-id="b3097-105">O **arquivo do WM \_ Cap \_ \_ set \_ INFOCHUNK** Message define e limpa as partes de informações.</span><span class="sxs-lookup"><span data-stu-id="b3097-105">The **WM\_CAP\_FILE\_SET\_INFOCHUNK** message sets and clears information chunks.</span></span> <span data-ttu-id="b3097-106">As partes de informações podem ser inseridas em um arquivo AVI durante a captura para inserir cadeias de caracteres de texto ou dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="b3097-106">Information chunks can be inserted in an AVI file during capture to embed text strings or custom data.</span></span> <span data-ttu-id="b3097-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="b3097-107">You can send this message explicitly or by using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a><span data-ttu-id="b3097-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3097-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3097-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span><span class="sxs-lookup"><span data-stu-id="b3097-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span></span>
</dt> <dd>

<span data-ttu-id="b3097-110">Ponteiro para uma estrutura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) que define a parte das informações a ser criada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="b3097-110">Pointer to a [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure defining the information chunk to be created or deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3097-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b3097-111">Return Value</span></span>

<span data-ttu-id="b3097-112">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b3097-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="b3097-113">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="b3097-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3097-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3097-114">Remarks</span></span>

<span data-ttu-id="b3097-115">Várias partes de informações registradas podem ser adicionadas a um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="b3097-115">Multiple registered information chunks can be added to an AVI file.</span></span> <span data-ttu-id="b3097-116">Depois que uma parte de informações é definida, ela continua a ser adicionada aos arquivos de captura subsequentes até que a entrada seja desmarcada ou todas as entradas de partes de informações sejam limpas.</span><span class="sxs-lookup"><span data-stu-id="b3097-116">After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared.</span></span> <span data-ttu-id="b3097-117">Para limpar uma única entrada, especifique a parte das informações no membro **fccInfoID** e **NULL** no membro **lpData** da estrutura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="b3097-117">To clear a single entry, specify the information chunk in the **fccInfoID** member and **NULL** in the **lpData** member of the [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure.</span></span> <span data-ttu-id="b3097-118">Para limpar todas as entradas, especifique **NULL** em **fccInfoID**.</span><span class="sxs-lookup"><span data-stu-id="b3097-118">To clear all entries, specify **NULL** in **fccInfoID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3097-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3097-119">Requirements</span></span>



| <span data-ttu-id="b3097-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3097-120">Requirement</span></span> | <span data-ttu-id="b3097-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b3097-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b3097-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3097-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3097-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3097-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b3097-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3097-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3097-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3097-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b3097-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3097-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3097-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3097-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3097-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3097-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3097-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b3097-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b3097-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b3097-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





