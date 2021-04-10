---
title: Mensagem de ICM_DRAW_BEGIN (VFW. h)
description: A \_ mensagem de início de desenho ICM \_ Notifica um driver de renderização para se preparar para desenhar dados.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_BEGIN
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918952"
---
# <a name="icm_draw_begin-message"></a><span data-ttu-id="03cad-104">Mensagem de início de \_ desenho ICM \_</span><span class="sxs-lookup"><span data-stu-id="03cad-104">ICM\_DRAW\_BEGIN message</span></span>

<span data-ttu-id="03cad-105">A mensagem de **\_ \_ início de desenho ICM** notifica um driver de renderização para se preparar para desenhar dados.</span><span class="sxs-lookup"><span data-stu-id="03cad-105">The **ICM\_DRAW\_BEGIN** message notifies a rendering driver to prepare to draw data.</span></span>


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="03cad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03cad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03cad-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span><span class="sxs-lookup"><span data-stu-id="03cad-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span></span>
</dt> <dd>

<span data-ttu-id="03cad-108">Ponteiro para uma estrutura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="03cad-108">Pointer to an [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="03cad-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="03cad-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="03cad-110">Tamanho, em bytes, de **ICDRAWBEGIN**.</span><span class="sxs-lookup"><span data-stu-id="03cad-110">Size, in bytes, of **ICDRAWBEGIN**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03cad-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="03cad-111">Return Value</span></span>

<span data-ttu-id="03cad-112">Retornará ICERR \_ OK se o driver der suporte a desenhar os dados na tela na maneira e no formato especificados, ou então um código de erro.</span><span class="sxs-lookup"><span data-stu-id="03cad-112">Returns ICERR\_OK if the driver supports drawing the data to the screen in the specified manner and format, or an error code otherwise.</span></span> <span data-ttu-id="03cad-113">Os possíveis valores de erro incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="03cad-113">Possible error values include the following.</span></span>



| <span data-ttu-id="03cad-114">Valor</span><span class="sxs-lookup"><span data-stu-id="03cad-114">Value</span></span>               | <span data-ttu-id="03cad-115">Significado</span><span class="sxs-lookup"><span data-stu-id="03cad-115">Meaning</span></span>                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="03cad-116">ICERR \_ BADFORMAT</span><span class="sxs-lookup"><span data-stu-id="03cad-116">ICERR\_BADFORMAT</span></span>    | <span data-ttu-id="03cad-117">Não há suporte para o formato de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="03cad-117">Input or output format is not supported.</span></span>                                      |
| <span data-ttu-id="03cad-118">ICERR \_ sem suporte</span><span class="sxs-lookup"><span data-stu-id="03cad-118">ICERR\_NOTSUPPORTED</span></span> | <span data-ttu-id="03cad-119">O driver não é desenhado diretamente na tela ou não oferece suporte a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="03cad-119">Driver does not draw directly to the screen or does not support this message.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="03cad-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="03cad-120">Remarks</span></span>

<span data-ttu-id="03cad-121">Se você quiser que o driver Descompacte dados em um buffer, envie a mensagem de [**\_ \_ início de descompactação ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="03cad-121">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="03cad-122">As mensagens de final **ICM \_ draw \_ begin** e [**ICM \_ draw \_**](icm-draw-end.md) não são aninhadas.</span><span class="sxs-lookup"><span data-stu-id="03cad-122">The **ICM\_DRAW\_BEGIN** and [**ICM\_DRAW\_END**](icm-draw-end.md) messages do not nest.</span></span> <span data-ttu-id="03cad-123">Se o driver receber o **início de ICM e \_ \_ começar** antes que a descompactação seja interrompida com a **\_ \_ extremidade de desenho ICM**, ela deverá reiniciar a descompactação com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="03cad-123">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="03cad-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03cad-124">Requirements</span></span>



| <span data-ttu-id="03cad-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="03cad-125">Requirement</span></span> | <span data-ttu-id="03cad-126">Valor</span><span class="sxs-lookup"><span data-stu-id="03cad-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="03cad-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03cad-127">Minimum supported client</span></span><br/> | <span data-ttu-id="03cad-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03cad-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="03cad-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03cad-129">Minimum supported server</span></span><br/> | <span data-ttu-id="03cad-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03cad-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="03cad-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="03cad-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="03cad-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="03cad-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03cad-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="03cad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cad-134">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="03cad-134">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="03cad-135">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="03cad-135">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





