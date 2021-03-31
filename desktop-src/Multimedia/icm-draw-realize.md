---
title: Mensagem de ICM_DRAW_REALIZE (VFW. h)
description: A mensagem de desenho do ICM \_ draw \_ Notifica um driver de renderização para perceber sua paleta de desenho durante o desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_REALIZE
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369530"
---
# <a name="icm_draw_realize-message"></a><span data-ttu-id="e0f9b-105">Mensagem de percepção de \_ desenho de ICM \_</span><span class="sxs-lookup"><span data-stu-id="e0f9b-105">ICM\_DRAW\_REALIZE message</span></span>

<span data-ttu-id="e0f9b-106">A mensagem de **desenho do ICM \_ draw \_** notifica um driver de renderização para perceber sua paleta de desenho durante o desenho.</span><span class="sxs-lookup"><span data-stu-id="e0f9b-106">The **ICM\_DRAW\_REALIZE** message notifies a rendering driver to realize its drawing palette while drawing.</span></span> <span data-ttu-id="e0f9b-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .</span><span class="sxs-lookup"><span data-stu-id="e0f9b-107">You can send this message explicitly or by using the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro.</span></span>


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a><span data-ttu-id="e0f9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0f9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f9b-109"><span id="hdc"></span><span id="HDC"></span>*HDC*</span><span class="sxs-lookup"><span data-stu-id="e0f9b-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span></span>
</dt> <dd>

<span data-ttu-id="e0f9b-110">Manipule o controlador de domínio usado para obter a paleta.</span><span class="sxs-lookup"><span data-stu-id="e0f9b-110">Handle to the DC used to realize the palette.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9b-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span><span class="sxs-lookup"><span data-stu-id="e0f9b-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span></span>
</dt> <dd>

<span data-ttu-id="e0f9b-112">Sinalizador de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="e0f9b-112">Background flag.</span></span> <span data-ttu-id="e0f9b-113">Especifique **true** para compreender a paleta como uma tarefa em segundo plano ou **false** para perceber a paleta em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="e0f9b-113">Specify **TRUE** to realize the palette as a background task or **FALSE** to realize the palette in the foreground.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f9b-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e0f9b-114">Return Value</span></span>

<span data-ttu-id="e0f9b-115">Retornará ICERR \_ OK se a paleta de desenho for realizada ou ICERR \_ sem suporte se a paleta associada aos dados descompactados for realizada.</span><span class="sxs-lookup"><span data-stu-id="e0f9b-115">Returns ICERR\_OK if the drawing palette is realized or ICERR\_UNSUPPORTED if the palette associated with the decompressed data is realized.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f9b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0f9b-116">Remarks</span></span>

<span data-ttu-id="e0f9b-117">Os drivers só precisarão responder a esta mensagem se a paleta de desenho for diferente da paleta descompactada.</span><span class="sxs-lookup"><span data-stu-id="e0f9b-117">Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f9b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0f9b-118">Requirements</span></span>



| <span data-ttu-id="e0f9b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f9b-119">Requirement</span></span> | <span data-ttu-id="e0f9b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e0f9b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e0f9b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f9b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f9b-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0f9b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e0f9b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f9b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f9b-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0f9b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e0f9b-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0f9b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0f9b-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9b-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f9b-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e0f9b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f9b-128">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="e0f9b-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e0f9b-129">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="e0f9b-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





