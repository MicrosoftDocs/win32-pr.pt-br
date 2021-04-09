---
title: PGN_SCROLL código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de pager que a janela contida está prestes a ser rolada. Essa notificação é enviada na forma de uma mensagem de \_ notificação do WM.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085459"
---
# <a name="pgn_scroll-notification-code"></a><span data-ttu-id="14241-105">\_Código de notificação de rolagem PGN</span><span class="sxs-lookup"><span data-stu-id="14241-105">PGN\_SCROLL notification code</span></span>

<span data-ttu-id="14241-106">Notifica uma janela pai do controle de pager que a janela contida está prestes a ser rolada.</span><span class="sxs-lookup"><span data-stu-id="14241-106">Notifies a pager control's parent window that the contained window is about to be scrolled.</span></span> <span data-ttu-id="14241-107">Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="14241-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="14241-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14241-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14241-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14241-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14241-110">Ponteiro para uma estrutura [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) que contém e recebe informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="14241-110">Pointer to an [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="14241-111">O membro **iDir** dessa estrutura indica a direção da rolagem.</span><span class="sxs-lookup"><span data-stu-id="14241-111">The **iDir** member of this structure indicates the direction of the scroll.</span></span> <span data-ttu-id="14241-112">Os membros **iXpos** e **iYpos** contêm a posição horizontal e vertical da janela contida antes da rolagem.</span><span class="sxs-lookup"><span data-stu-id="14241-112">The **iXpos** and **iYpos** members contain the horizontal and vertical position of the contained window prior to the scroll.</span></span> <span data-ttu-id="14241-113">O membro **iScroll** contém o valor delta de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="14241-113">The **iScroll** member contains the default scroll delta amount.</span></span> <span data-ttu-id="14241-114">Você pode modificar esse membro para um valor de rolagem diferente, se desejar.</span><span class="sxs-lookup"><span data-stu-id="14241-114">You can modify this member to a different scroll amount if desired.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14241-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14241-115">Return value</span></span>

<span data-ttu-id="14241-116">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="14241-116">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="14241-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14241-117">Requirements</span></span>



| <span data-ttu-id="14241-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14241-118">Requirement</span></span> | <span data-ttu-id="14241-119">Valor</span><span class="sxs-lookup"><span data-stu-id="14241-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14241-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14241-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14241-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14241-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14241-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14241-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14241-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14241-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14241-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14241-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14241-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14241-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





