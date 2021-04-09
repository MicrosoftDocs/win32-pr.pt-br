---
title: BCN_HOTITEMCHANGE código de notificação (commctrl. h)
description: Notifica o proprietário do controle de botão que o mouse está inserindo ou deixando a área cliente do controle botão. O controle de botão envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009208"
---
# <a name="bcn_hotitemchange-notification-code"></a><span data-ttu-id="c0e3b-105">Código de notificação do BCN \_ HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="c0e3b-105">BCN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="c0e3b-106">Notifica o proprietário do controle de botão que o mouse está inserindo ou deixando a área cliente do controle botão.</span><span class="sxs-lookup"><span data-stu-id="c0e3b-106">Notifies the button control owner that the mouse is entering or leaving the client area of the button control.</span></span> <span data-ttu-id="c0e3b-107">O controle de botão envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c0e3b-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c0e3b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0e3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0e3b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0e3b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0e3b-110">Um ponteiro para uma estrutura [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .</span><span class="sxs-lookup"><span data-stu-id="c0e3b-110">A pointer to a [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0e3b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0e3b-111">Return value</span></span>

<span data-ttu-id="c0e3b-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c0e3b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e3b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0e3b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0e3b-114">Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="c0e3b-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c0e3b-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0e3b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0e3b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0e3b-116">Requirements</span></span>



| <span data-ttu-id="c0e3b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0e3b-117">Requirement</span></span> | <span data-ttu-id="c0e3b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c0e3b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e3b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0e3b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0e3b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0e3b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0e3b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0e3b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0e3b-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0e3b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0e3b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0e3b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0e3b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0e3b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





