---
title: Mensagem de ICM_DRAW_GETTIME (VFW. h)
description: A \_ mensagem ICM Draw \_ getTime solicita um driver de renderização que controla o tempo dos quadros de desenho para retornar o valor atual de seu relógio interno. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_GETTIME
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754330"
---
# <a name="icm_draw_gettime-message"></a><span data-ttu-id="2a5b1-105">\_ \_ Mensagem getTime do ICM Draw</span><span class="sxs-lookup"><span data-stu-id="2a5b1-105">ICM\_DRAW\_GETTIME message</span></span>

<span data-ttu-id="2a5b1-106">A mensagem **ICM \_ draw \_ getTime** solicita um driver de renderização que controla o tempo dos quadros de desenho para retornar o valor atual de seu relógio interno.</span><span class="sxs-lookup"><span data-stu-id="2a5b1-106">The **ICM\_DRAW\_GETTIME** message requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock.</span></span> <span data-ttu-id="2a5b1-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .</span><span class="sxs-lookup"><span data-stu-id="2a5b1-107">You can send this message explicitly or by using the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro.</span></span>


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2a5b1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a5b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a5b1-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span><span class="sxs-lookup"><span data-stu-id="2a5b1-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span></span>
</dt> <dd>

<span data-ttu-id="2a5b1-110">Endereço para conter a hora atual.</span><span class="sxs-lookup"><span data-stu-id="2a5b1-110">Address to contain the current time.</span></span> <span data-ttu-id="2a5b1-111">O valor de retorno deve ser especificado em exemplos.</span><span class="sxs-lookup"><span data-stu-id="2a5b1-111">The return value should be specified in samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a5b1-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2a5b1-112">Return Value</span></span>

<span data-ttu-id="2a5b1-113">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="2a5b1-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a5b1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a5b1-114">Remarks</span></span>

<span data-ttu-id="2a5b1-115">Em geral, essa mensagem é suportada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.</span><span class="sxs-lookup"><span data-stu-id="2a5b1-115">This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span> <span data-ttu-id="2a5b1-116">A mensagem também pode ser enviada se o hardware estiver sendo usado como o mestre de sincronização.</span><span class="sxs-lookup"><span data-stu-id="2a5b1-116">The message can also be sent if the hardware is being used as the synchronization master.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a5b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a5b1-117">Requirements</span></span>



| <span data-ttu-id="2a5b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a5b1-118">Requirement</span></span> | <span data-ttu-id="2a5b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2a5b1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a5b1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a5b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a5b1-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a5b1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a5b1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a5b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a5b1-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a5b1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2a5b1-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2a5b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a5b1-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a5b1-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a5b1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a5b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a5b1-127">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a5b1-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2a5b1-128">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a5b1-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





