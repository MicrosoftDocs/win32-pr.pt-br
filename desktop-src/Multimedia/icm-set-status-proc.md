---
title: Mensagem de ICM_SET_STATUS_PROC (VFW. h)
description: A \_ mensagem ICM Set \_ status \_ proc fornece uma função de retorno de chamada de status com o status de uma operação demorada.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- Multimídia do Windows de mensagem ICM_SET_STATUS_PROC
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456037"
---
# <a name="icm_set_status_proc-message"></a><span data-ttu-id="06b6e-104">\_Mensagem de \_ procedimento de status de configuração ICM \_</span><span class="sxs-lookup"><span data-stu-id="06b6e-104">ICM\_SET\_STATUS\_PROC message</span></span>

<span data-ttu-id="06b6e-105">A mensagem **ICM \_ set \_ status \_ proc** fornece uma função de retorno de chamada de status com o status de uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="06b6e-105">The **ICM\_SET\_STATUS\_PROC** message provides a status callback function with the status of a lengthy operation.</span></span>


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a><span data-ttu-id="06b6e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06b6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b6e-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span><span class="sxs-lookup"><span data-stu-id="06b6e-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span></span>
</dt> <dd>

<span data-ttu-id="06b6e-108">Ponteiro para uma estrutura [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .</span><span class="sxs-lookup"><span data-stu-id="06b6e-108">Pointer to an [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="06b6e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="06b6e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="06b6e-110">Tamanho, em bytes, de **ICSETSTATUSPROC**.</span><span class="sxs-lookup"><span data-stu-id="06b6e-110">Size, in bytes, of **ICSETSTATUSPROC**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b6e-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="06b6e-111">Return Value</span></span>

<span data-ttu-id="06b6e-112">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="06b6e-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="06b6e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="06b6e-113">Remarks</span></span>

<span data-ttu-id="06b6e-114">O suporte a essa mensagem é opcional, mas é altamente recomendável se a compactação ou descompactação demorar mais do que aproximadamente um décimo de segundo.</span><span class="sxs-lookup"><span data-stu-id="06b6e-114">Support of this message is optional but strongly recommended if compression or decompression takes longer than approximately one-tenth of a second.</span></span>

<span data-ttu-id="06b6e-115">Um aplicativo pode enviar essa mensagem periodicamente para uma função de retorno de chamada de status durante operações demoradas.</span><span class="sxs-lookup"><span data-stu-id="06b6e-115">An application can send this message periodically to a status callback function during lengthy operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b6e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06b6e-116">Requirements</span></span>



| <span data-ttu-id="06b6e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b6e-117">Requirement</span></span> | <span data-ttu-id="06b6e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="06b6e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="06b6e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06b6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06b6e-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06b6e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="06b6e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06b6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06b6e-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06b6e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="06b6e-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06b6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06b6e-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="06b6e-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b6e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="06b6e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b6e-126">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="06b6e-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="06b6e-127">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="06b6e-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





