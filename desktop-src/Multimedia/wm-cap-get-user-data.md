---
title: Mensagem de WM_CAP_GET_USER_DATA (VFW. h)
description: A mensagem de obtenção de dados do usuário do WM \_ Cap \_ \_ \_ recupera um \_ valor de dados PTR longo associado a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_USER_DATA
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499660"
---
# <a name="wm_cap_get_user_data-message"></a><span data-ttu-id="48dff-105">\_Mensagem de \_ obtenção \_ de \_ dados do usuário do WM Cap</span><span class="sxs-lookup"><span data-stu-id="48dff-105">WM\_CAP\_GET\_USER\_DATA message</span></span>

<span data-ttu-id="48dff-106">A mensagem de **\_ obtenção de \_ \_ \_ dados do usuário do WM Cap** recupera um valor de dados **\_ PTR longo** associado a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="48dff-106">The **WM\_CAP\_GET\_USER\_DATA** message retrieves a **LONG\_PTR** data value associated with a capture window.</span></span> <span data-ttu-id="48dff-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="48dff-107">You can send this message explicitly or by using the [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) macro.</span></span>


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="48dff-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="48dff-108">Return Value</span></span>

<span data-ttu-id="48dff-109">Retorna um valor salvo anteriormente usando a mensagem de [**dados do usuário do WM \_ Cap \_ \_ \_ set**](wm-cap-set-user-data.md) .</span><span class="sxs-lookup"><span data-stu-id="48dff-109">Returns a value previously saved by using the [**WM\_CAP\_SET\_USER\_DATA**](wm-cap-set-user-data.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="48dff-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48dff-110">Requirements</span></span>



| <span data-ttu-id="48dff-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="48dff-111">Requirement</span></span> | <span data-ttu-id="48dff-112">Valor</span><span class="sxs-lookup"><span data-stu-id="48dff-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="48dff-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48dff-113">Minimum supported client</span></span><br/> | <span data-ttu-id="48dff-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48dff-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="48dff-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48dff-115">Minimum supported server</span></span><br/> | <span data-ttu-id="48dff-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48dff-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48dff-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="48dff-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="48dff-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="48dff-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48dff-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="48dff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48dff-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="48dff-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="48dff-121">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="48dff-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





