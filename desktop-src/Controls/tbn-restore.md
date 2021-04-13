---
title: TBN_RESTORE código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está em processo de restauração. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455602"
---
# <a name="tbn_restore-notification-code"></a><span data-ttu-id="e3a0e-105">Código de notificação de restauração do TBN \_</span><span class="sxs-lookup"><span data-stu-id="e3a0e-105">TBN\_RESTORE notification code</span></span>

<span data-ttu-id="e3a0e-106">Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está em processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="e3a0e-106">Notifies a toolbar's parent window that a toolbar is in the process of being restored.</span></span> <span data-ttu-id="e3a0e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e3a0e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e3a0e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a0e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3a0e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a0e-110">Ponteiro para uma estrutura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .</span><span class="sxs-lookup"><span data-stu-id="e3a0e-110">Pointer to an [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a0e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3a0e-111">Return value</span></span>

<span data-ttu-id="e3a0e-112">O aplicativo deve retornar zero em resposta ao primeiro código de notificação de **\_ restauração tbn** recebido no início do processo de restauração para continuar restaurando as informações do botão.</span><span class="sxs-lookup"><span data-stu-id="e3a0e-112">The application should return zero in response to the first **TBN\_RESTORE** notification code received at the start of the restore process to continue restoring the button information.</span></span> <span data-ttu-id="e3a0e-113">Se o aplicativo retornar um valor diferente de zero, o processo de restauração será cancelado.</span><span class="sxs-lookup"><span data-stu-id="e3a0e-113">If the application returns a nonzero value, the restore process is canceled.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a0e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a0e-114">Remarks</span></span>

<span data-ttu-id="e3a0e-115">O aplicativo receberá esse código de notificação uma vez no início do processo de restauração e uma vez para cada botão.</span><span class="sxs-lookup"><span data-stu-id="e3a0e-115">The application will receive this notification code once at the start of the restore process and once for each button.</span></span> <span data-ttu-id="e3a0e-116">Esse código de notificação lhe dá a oportunidade de extrair as informações do fluxo de dados que você salvou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e3a0e-116">This notification code gives you an opportunity to extract the information from the data stream that you saved previously.</span></span> <span data-ttu-id="e3a0e-117">Se você não tiver salvo nenhuma informação, ignore o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="e3a0e-117">If you haven't saved any information, ignore the notification code.</span></span> <span data-ttu-id="e3a0e-118">Consulte [personalização da barra de ferramentas](toolbar-controls-overview.md) para obter uma discussão mais detalhada sobre como lidar com a **tbn \_ Restore**.</span><span class="sxs-lookup"><span data-stu-id="e3a0e-118">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle **TBN\_RESTORE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a0e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a0e-119">Requirements</span></span>



| <span data-ttu-id="e3a0e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a0e-120">Requirement</span></span> | <span data-ttu-id="e3a0e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e3a0e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a0e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3a0e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a0e-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3a0e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3a0e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3a0e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a0e-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3a0e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3a0e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3a0e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a0e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a0e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





