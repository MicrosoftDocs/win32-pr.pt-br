---
title: Mensagem de ICM_DRAW_CHANGEPALETTE (VFW. h)
description: A \_ mensagem ICM Draw \_ CHANGEPALETTE notifica um driver de renderização que a paleta de filmes está alterando. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_CHANGEPALETTE
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824500"
---
# <a name="icm_draw_changepalette-message"></a><span data-ttu-id="b8f2d-105">\_Mensagem de desenho CHANGEPALETTE de ICM \_</span><span class="sxs-lookup"><span data-stu-id="b8f2d-105">ICM\_DRAW\_CHANGEPALETTE message</span></span>

<span data-ttu-id="b8f2d-106">A mensagem **ICM \_ draw \_ CHANGEPALETTE** notifica um driver de renderização que a paleta de filmes está alterando.</span><span class="sxs-lookup"><span data-stu-id="b8f2d-106">The **ICM\_DRAW\_CHANGEPALETTE** message notifies a rendering driver that the movie palette is changing.</span></span> <span data-ttu-id="b8f2d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .</span><span class="sxs-lookup"><span data-stu-id="b8f2d-107">You can send this message explicitly or by using the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro.</span></span>


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="b8f2d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8f2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f2d-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="b8f2d-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="b8f2d-110">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o novo formato e a tabela de cores opcional.</span><span class="sxs-lookup"><span data-stu-id="b8f2d-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the new format and optional color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f2d-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b8f2d-111">Return Value</span></span>

<span data-ttu-id="b8f2d-112">Retorna ICERR \_ OK se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b8f2d-112">Returns ICERR\_OK if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f2d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8f2d-113">Remarks</span></span>

<span data-ttu-id="b8f2d-114">Essa mensagem deve ser suportada por manipuladores de renderização instaláveis que redesenham DIBs com uma estrutura interna que inclui uma paleta.</span><span class="sxs-lookup"><span data-stu-id="b8f2d-114">This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f2d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8f2d-115">Requirements</span></span>



| <span data-ttu-id="b8f2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8f2d-116">Requirement</span></span> | <span data-ttu-id="b8f2d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b8f2d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8f2d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8f2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f2d-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8f2d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b8f2d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8f2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f2d-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8f2d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8f2d-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b8f2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f2d-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f2d-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f2d-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b8f2d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f2d-125">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="b8f2d-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b8f2d-126">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="b8f2d-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

