---
title: Mensagem de ICM_ABOUT (VFW. h)
description: O ICM \_ sobre Message notifica um driver de compactação de vídeo para exibir sua caixa de diálogo about ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo about. Você pode enviar essa mensagem explicitamente ou usando a macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- Multimídia do Windows de mensagem ICM_ABOUT
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008839"
---
# <a name="icm_about-message"></a><span data-ttu-id="40742-105">ICM \_ sobre a mensagem</span><span class="sxs-lookup"><span data-stu-id="40742-105">ICM\_ABOUT message</span></span>

<span data-ttu-id="40742-106">O **ICM \_ sobre** Message notifica um driver de compactação de vídeo para exibir sua caixa de diálogo about ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo about.</span><span class="sxs-lookup"><span data-stu-id="40742-106">The **ICM\_ABOUT** message notifies a video compression driver to display its About dialog box or queries a video compression driver to determine if it has an About dialog box.</span></span> <span data-ttu-id="40742-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .</span><span class="sxs-lookup"><span data-stu-id="40742-107">You can send this message explicitly or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro.</span></span>


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="40742-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40742-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40742-109"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="40742-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="40742-110">Identificador para a janela pai da caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="40742-110">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="40742-111">Você também pode determinar se um driver tem uma caixa de diálogo about especificando-1 nesse parâmetro, como na macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) .</span><span class="sxs-lookup"><span data-stu-id="40742-111">You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro.</span></span> <span data-ttu-id="40742-112">O driver retornará ICERR \_ OK se ele tiver uma caixa de diálogo about ou ICERR \_ sem suporte, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="40742-112">The driver returns ICERR\_OK if it has an About dialog box or ICERR\_UNSUPPORTED otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40742-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="40742-113">Return Value</span></span>

<span data-ttu-id="40742-114">Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="40742-114">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="40742-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40742-115">Requirements</span></span>



| <span data-ttu-id="40742-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="40742-116">Requirement</span></span> | <span data-ttu-id="40742-117">Valor</span><span class="sxs-lookup"><span data-stu-id="40742-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="40742-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40742-118">Minimum supported client</span></span><br/> | <span data-ttu-id="40742-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40742-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="40742-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40742-120">Minimum supported server</span></span><br/> | <span data-ttu-id="40742-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40742-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="40742-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="40742-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="40742-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="40742-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40742-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="40742-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40742-125">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="40742-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="40742-126">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="40742-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





