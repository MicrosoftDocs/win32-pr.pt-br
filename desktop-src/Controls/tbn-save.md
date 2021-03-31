---
title: TBN_SAVE código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está sendo salva. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645225"
---
# <a name="tbn_save-notification-code"></a><span data-ttu-id="7a294-105">TBN \_ salvar código de notificação</span><span class="sxs-lookup"><span data-stu-id="7a294-105">TBN\_SAVE notification code</span></span>

<span data-ttu-id="7a294-106">Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está sendo salva.</span><span class="sxs-lookup"><span data-stu-id="7a294-106">Notifies a toolbar's parent window that a toolbar is in the process of being saved.</span></span> <span data-ttu-id="7a294-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7a294-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7a294-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a294-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a294-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a294-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a294-110">Ponteiro para uma estrutura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .</span><span class="sxs-lookup"><span data-stu-id="7a294-110">Pointer to an [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a294-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a294-111">Return value</span></span>

<span data-ttu-id="7a294-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7a294-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a294-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a294-113">Remarks</span></span>

<span data-ttu-id="7a294-114">O aplicativo receberá esse código de notificação uma vez no início do processo de salvamento e uma vez para cada botão.</span><span class="sxs-lookup"><span data-stu-id="7a294-114">The application will receive this notification code once at the start of the save process and once for each button.</span></span> <span data-ttu-id="7a294-115">Esse código de notificação lhe dá a oportunidade de adicionar suas próprias informações ao salvas pelo shell.</span><span class="sxs-lookup"><span data-stu-id="7a294-115">This notification code gives you an opportunity to add your own information to that saved by the Shell.</span></span> <span data-ttu-id="7a294-116">Se você não quiser adicionar informações, ignore o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="7a294-116">If you do not wish to add information, ignore the notification code.</span></span> <span data-ttu-id="7a294-117">Consulte [personalização da barra de ferramentas](toolbar-controls-overview.md) para obter uma discussão mais detalhada sobre como lidar com tbn \_ Save.</span><span class="sxs-lookup"><span data-stu-id="7a294-117">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle TBN\_SAVE.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a294-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a294-118">Requirements</span></span>



| <span data-ttu-id="7a294-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a294-119">Requirement</span></span> | <span data-ttu-id="7a294-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7a294-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a294-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a294-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a294-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a294-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a294-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a294-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a294-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a294-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a294-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a294-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a294-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a294-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a294-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7a294-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a294-128">TBN \_ restauração</span><span class="sxs-lookup"><span data-stu-id="7a294-128">TBN\_RESTORE</span></span>](tbn-restore.md)
</dt> </dl>

 

 





