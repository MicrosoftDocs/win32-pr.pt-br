---
title: Mensagem de WM_CAP_SET_USER_DATA (VFW. h)
description: A Cap do WM \_ \_ definir a \_ \_ mensagem de dados do usuário associa um \_ valor de dados PTR longo a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_USER_DATA
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086365"
---
# <a name="wm_cap_set_user_data-message"></a><span data-ttu-id="fb9ef-105">\_Mensagem de \_ \_ dados do usuário Set Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="fb9ef-105">WM\_CAP\_SET\_USER\_DATA message</span></span>

<span data-ttu-id="fb9ef-106">A **Cap do WM definir a mensagem de \_ \_ \_ \_ dados do usuário** associa um valor de dados **\_ PTR longo** a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="fb9ef-106">The **WM\_CAP\_SET\_USER\_DATA** message associates a **LONG\_PTR** data value with a capture window.</span></span> <span data-ttu-id="fb9ef-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="fb9ef-107">You can send this message explicitly or by using the [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) macro.</span></span>


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a><span data-ttu-id="fb9ef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb9ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb9ef-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span><span class="sxs-lookup"><span data-stu-id="fb9ef-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span></span>
</dt> <dd>

<span data-ttu-id="fb9ef-110">Valor de dados a ser associado a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="fb9ef-110">Data value to associate with a capture window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb9ef-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fb9ef-111">Return Value</span></span>

<span data-ttu-id="fb9ef-112">Retornará **true** se for bem-sucedido ou **false** se a captura de streaming estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="fb9ef-112">Returns **TRUE** if successful or **FALSE** if streaming capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb9ef-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb9ef-113">Remarks</span></span>

<span data-ttu-id="fb9ef-114">Normalmente, essa mensagem é usada para apontar para um bloco de dados associado a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="fb9ef-114">Typically this message is used to point to a block of data associated with a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb9ef-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb9ef-115">Requirements</span></span>



| <span data-ttu-id="fb9ef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb9ef-116">Requirement</span></span> | <span data-ttu-id="fb9ef-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9ef-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb9ef-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb9ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9ef-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb9ef-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fb9ef-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb9ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9ef-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb9ef-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fb9ef-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fb9ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb9ef-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb9ef-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb9ef-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb9ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9ef-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fb9ef-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fb9ef-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fb9ef-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





