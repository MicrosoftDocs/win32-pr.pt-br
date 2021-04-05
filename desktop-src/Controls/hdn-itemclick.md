---
title: HDN_ITEMCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário clicou no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824683"
---
# <a name="hdn_itemclick-notification-code"></a><span data-ttu-id="06c1e-105">Código de notificação do HDN \_ DOclick</span><span class="sxs-lookup"><span data-stu-id="06c1e-105">HDN\_ITEMCLICK notification code</span></span>

<span data-ttu-id="06c1e-106">Notifica uma janela pai do controle de cabeçalho que o usuário clicou no controle.</span><span class="sxs-lookup"><span data-stu-id="06c1e-106">Notifies a header control's parent window that the user clicked the control.</span></span> <span data-ttu-id="06c1e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="06c1e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="06c1e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06c1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06c1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c1e-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que identifica o controle de cabeçalho e especifica o índice do item de cabeçalho que foi clicado e o botão do mouse usado para clicar no item.</span><span class="sxs-lookup"><span data-stu-id="06c1e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that identifies the header control and specifies the index of the header item that was clicked and the mouse button used to click the item.</span></span> <span data-ttu-id="06c1e-111">O membro **pItem** está definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06c1e-111">The **pItem** member is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c1e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06c1e-112">Return value</span></span>

<span data-ttu-id="06c1e-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="06c1e-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c1e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="06c1e-114">Remarks</span></span>

<span data-ttu-id="06c1e-115">Um controle de cabeçalho envia esse código de notificação depois que o usuário libera o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="06c1e-115">A header control sends this notification code after the user releases the left mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c1e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c1e-116">Requirements</span></span>



| <span data-ttu-id="06c1e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c1e-117">Requirement</span></span> | <span data-ttu-id="06c1e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="06c1e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06c1e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06c1e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06c1e-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06c1e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06c1e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06c1e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06c1e-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06c1e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06c1e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06c1e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c1e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c1e-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="06c1e-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="06c1e-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="06c1e-126">**HDN \_ ITEMCLICKW** (Unicode) e **HDN ao \_ clicar** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="06c1e-126">**HDN\_ITEMCLICKW** (Unicode) and **HDN\_ITEMCLICKA** (ANSI)</span></span><br/>               |



 

 





