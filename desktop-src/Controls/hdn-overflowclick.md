---
title: HDN_OVERFLOWCLICK código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho para seu pai quando o botão de estouro do cabeçalho é clicado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824457"
---
# <a name="hdn_overflowclick-notification-code"></a><span data-ttu-id="db7ad-105">Código de notificação do HDN \_ OVERFLOWCLICK</span><span class="sxs-lookup"><span data-stu-id="db7ad-105">HDN\_OVERFLOWCLICK notification code</span></span>

<span data-ttu-id="db7ad-106">Enviado por um controle de cabeçalho para seu pai quando o botão de estouro do cabeçalho é clicado.</span><span class="sxs-lookup"><span data-stu-id="db7ad-106">Sent by a header control to its parent when the header's overflow button is clicked.</span></span> <span data-ttu-id="db7ad-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="db7ad-107">This notification code is sent in the form of an [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="db7ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db7ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7ad-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db7ad-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db7ad-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que descreve o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="db7ad-110">A pointer to a [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that describes the notification code.</span></span> <span data-ttu-id="db7ad-111">O processo de chamada é responsável por alocar essa estrutura, incluindo a estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contida.</span><span class="sxs-lookup"><span data-stu-id="db7ad-111">The calling process is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="db7ad-112">Defina os membros da estrutura **NMHDR** , incluindo o membro do *código* que deve ser definido como HDN \_ OVERFLOWCLICK.</span><span class="sxs-lookup"><span data-stu-id="db7ad-112">Set the members of the **NMHDR** structure, including the *code* member that must be set to HDN\_OVERFLOWCLICK.</span></span>

<span data-ttu-id="db7ad-113">Defina o membro **iItem** da estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) para o índice do primeiro item de cabeçalho que não está visível e, portanto, deve ser exibido em um estouro.</span><span class="sxs-lookup"><span data-stu-id="db7ad-113">Set the **iItem** member of the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure to the index of the first header item that is not visible and thus should be displayed on an overflow.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7ad-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db7ad-114">Return value</span></span>

<span data-ttu-id="db7ad-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="db7ad-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7ad-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="db7ad-116">Remarks</span></span>

<span data-ttu-id="db7ad-117">O receptor de notificação converte **lParam** para recuperar a estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="db7ad-117">The notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="db7ad-118">**WParam** contém a ID do controle que envia a notificação.</span><span class="sxs-lookup"><span data-stu-id="db7ad-118">**WPARAM** contains the ID of the control that sends the notification.</span></span>

<span data-ttu-id="db7ad-119">Esta mensagem é enviada somente quando o estilo de [**\_ estouro HDS**](header-control-styles.md) é definido no controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="db7ad-119">This message is sent only when style [**HDS\_OVERFLOW**](header-control-styles.md) is set on the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="db7ad-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db7ad-120">Requirements</span></span>



| <span data-ttu-id="db7ad-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="db7ad-121">Requirement</span></span> | <span data-ttu-id="db7ad-122">Valor</span><span class="sxs-lookup"><span data-stu-id="db7ad-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db7ad-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db7ad-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db7ad-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db7ad-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db7ad-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db7ad-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db7ad-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db7ad-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db7ad-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db7ad-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="db7ad-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7ad-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





