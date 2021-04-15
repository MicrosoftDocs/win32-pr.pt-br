---
title: Mensagem de MCIWNDM_SETZOOM (VFW. h)
description: A \_ mensagem setZoom do MCIWNDM redimensiona uma imagem de vídeo de acordo com um fator de zoom. Essa Marco ajusta o tamanho de uma janela MCIWnd enquanto mantém uma taxa de proporção constante. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETZOOM
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454746"
---
# <a name="mciwndm_setzoom-message"></a><span data-ttu-id="95cda-106">Mensagem de MCIWNDM \_ SETzoom</span><span class="sxs-lookup"><span data-stu-id="95cda-106">MCIWNDM\_SETZOOM message</span></span>

<span data-ttu-id="95cda-107">A **mensagem \_ setZoom do MCIWNDM** redimensiona uma imagem de vídeo de acordo com um fator de zoom.</span><span class="sxs-lookup"><span data-stu-id="95cda-107">The **MCIWNDM\_SETZOOM** message resizes a video image according to a zoom factor.</span></span> <span data-ttu-id="95cda-108">Essa Marco ajusta o tamanho de uma janela MCIWnd enquanto mantém uma taxa de proporção constante.</span><span class="sxs-lookup"><span data-stu-id="95cda-108">This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio.</span></span> <span data-ttu-id="95cda-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="95cda-109">You can send this message explicitly or by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span>


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a><span data-ttu-id="95cda-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95cda-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95cda-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span><span class="sxs-lookup"><span data-stu-id="95cda-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span></span>
</dt> <dd>

<span data-ttu-id="95cda-112">Fator de zoom expresso como um percentual da imagem original.</span><span class="sxs-lookup"><span data-stu-id="95cda-112">Zoom factor expressed as a percentage of the original image.</span></span> <span data-ttu-id="95cda-113">Especifique 100 para exibir a imagem com seu tamanho criado, 200 para exibir a imagem com duas vezes seu tamanho normal ou 50 para exibir a imagem com metade do tamanho normal.</span><span class="sxs-lookup"><span data-stu-id="95cda-113">Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95cda-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="95cda-114">Return Value</span></span>

<span data-ttu-id="95cda-115">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="95cda-115">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="95cda-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95cda-116">Requirements</span></span>



| <span data-ttu-id="95cda-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="95cda-117">Requirement</span></span> | <span data-ttu-id="95cda-118">Valor</span><span class="sxs-lookup"><span data-stu-id="95cda-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="95cda-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95cda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95cda-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95cda-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="95cda-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95cda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95cda-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95cda-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="95cda-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="95cda-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95cda-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="95cda-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95cda-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="95cda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95cda-126">**MCIWndSetZoom**</span><span class="sxs-lookup"><span data-stu-id="95cda-126">**MCIWndSetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





