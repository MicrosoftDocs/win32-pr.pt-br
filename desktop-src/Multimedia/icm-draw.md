---
title: Mensagem de ICM_DRAW (VFW. h)
description: A \_ mensagem de desenho ICM notifica um driver de renderização para descompactar um quadro de dados e desenhá-lo na tela.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- Multimídia do Windows de mensagem ICM_DRAW
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644567"
---
# <a name="icm_draw-message"></a><span data-ttu-id="ef089-104">Mensagem de desenho de ICM \_</span><span class="sxs-lookup"><span data-stu-id="ef089-104">ICM\_DRAW message</span></span>

<span data-ttu-id="ef089-105">A mensagem de **\_ desenho ICM** notifica um driver de renderização para descompactar um quadro de dados e desenhá-lo na tela.</span><span class="sxs-lookup"><span data-stu-id="ef089-105">The **ICM\_DRAW** message notifies a rendering driver to decompress a frame of data and draw it to the screen.</span></span>


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="ef089-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef089-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef089-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ef089-108">Ponteiro para uma estrutura [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .</span><span class="sxs-lookup"><span data-stu-id="ef089-108">Pointer to an [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ef089-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef089-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ef089-110">Tamanho, em bytes, de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span><span class="sxs-lookup"><span data-stu-id="ef089-110">Size, in bytes, of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef089-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ef089-111">Return Value</span></span>

<span data-ttu-id="ef089-112">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ef089-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef089-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef089-113">Remarks</span></span>

<span data-ttu-id="ef089-114">Se o \_ sinalizador de atualização ICDRAW estiver definido no membro **dwFlags** de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), a área da tela usada para desenhar será inválida e precisará ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="ef089-114">If the ICDRAW\_UPDATE flag is set in the **dwFlags** member of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), the area of the screen used for drawing is invalid and needs to be updated.</span></span> <span data-ttu-id="ef089-115">A extensão da atualização depende do conteúdo do membro **lpData** .</span><span class="sxs-lookup"><span data-stu-id="ef089-115">The extent of updating depends on the contents of the **lpData** member.</span></span>

<span data-ttu-id="ef089-116">Se **lpData** for **nulo**, o driver deverá atualizar o retângulo de destino inteiro com a imagem atual.</span><span class="sxs-lookup"><span data-stu-id="ef089-116">If **lpData** is **NULL**, the driver should update the entire destination rectangle with the current image.</span></span> <span data-ttu-id="ef089-117">Se o driver mantiver uma cópia da imagem em um buffer fora da tela, ele poderá falhar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="ef089-117">If the driver maintains a copy of the image in an off-screen buffer, it can fail this message.</span></span> <span data-ttu-id="ef089-118">Se **lpData** não for **NULL**, o driver deverá desenhar os dados e verificar se o destino inteiro foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="ef089-118">If **lpData** is not **NULL**, the driver should draw the data and make sure the entire destination is updated.</span></span>

<span data-ttu-id="ef089-119">Se o \_ sinalizador ICDRAW HURRYUP for definido em **dwFlags**, o aplicativo de chamada deseja que o driver prossiga o mais rápido possível, possivelmente nem mesmo atualizando a tela.</span><span class="sxs-lookup"><span data-stu-id="ef089-119">If the ICDRAW\_HURRYUP flag is set in **dwFlags**, the calling application wants the driver to proceed as quickly as possible, possibly not even updating the screen.</span></span>

<span data-ttu-id="ef089-120">Se o \_ sinalizador de PREROLL ICDRAW estiver definido em **dwFlags**, este quadro de vídeo será informações preliminares e não deverá ser exibido, se possível.</span><span class="sxs-lookup"><span data-stu-id="ef089-120">If the ICDRAW\_PREROLL flag is set in **dwFlags**, this video frame is preliminary information and should not be displayed if possible.</span></span> <span data-ttu-id="ef089-121">Por exemplo, se Play for iniciar do quadro 10 e o quadro 0 for o quadro-chave anterior mais próximo, os quadros de 0 a 9 terão o ICDRAW \_ PRErolled set.</span><span class="sxs-lookup"><span data-stu-id="ef089-121">For example, if play is to start from frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 will have ICDRAW\_PREROLL set.</span></span>

<span data-ttu-id="ef089-122">Se você quiser que o driver Descompacte dados em um buffer, envie a mensagem de [**\_ descompactação ICM**](icm-decompress.md) .</span><span class="sxs-lookup"><span data-stu-id="ef089-122">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS**](icm-decompress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef089-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef089-123">Requirements</span></span>



| <span data-ttu-id="ef089-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef089-124">Requirement</span></span> | <span data-ttu-id="ef089-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ef089-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef089-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef089-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ef089-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ef089-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ef089-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef089-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ef089-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ef089-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef089-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ef089-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef089-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef089-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef089-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef089-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef089-133">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="ef089-133">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ef089-134">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="ef089-134">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





