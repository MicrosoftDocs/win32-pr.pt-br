---
title: TBN_DRAGOUT código de notificação (commctrl. h)
description: Enviado por um controle Toolbar quando o usuário clica em um botão e, em seguida, move o cursor para fora do botão. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009115"
---
# <a name="tbn_dragout-notification-code"></a><span data-ttu-id="a2d04-105">Código de notificação de arrastar e TBN \_</span><span class="sxs-lookup"><span data-stu-id="a2d04-105">TBN\_DRAGOUT notification code</span></span>

<span data-ttu-id="a2d04-106">Enviado por um controle Toolbar quando o usuário clica em um botão e, em seguida, move o cursor para fora do botão.</span><span class="sxs-lookup"><span data-stu-id="a2d04-106">Sent by a toolbar control when the user clicks a button and then moves the cursor off the button.</span></span> <span data-ttu-id="a2d04-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a2d04-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a2d04-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2d04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2d04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2d04-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2d04-110">Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="a2d04-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="a2d04-111">Para este código de notificação, somente os membros **HDR** e **iItem** dessa estrutura são válidos.</span><span class="sxs-lookup"><span data-stu-id="a2d04-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="a2d04-112">O membro **iItem** dessa estrutura contém o identificador de comando do botão que está sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="a2d04-112">The **iItem** member of this structure contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2d04-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2d04-113">Return value</span></span>

<span data-ttu-id="a2d04-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a2d04-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2d04-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2d04-115">Remarks</span></span>

<span data-ttu-id="a2d04-116">Esse código de notificação permite que um aplicativo implemente a funcionalidade de arrastar e soltar para botões da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a2d04-116">This notification code allows an application to implement drag-and-drop functionality for toolbar buttons.</span></span> <span data-ttu-id="a2d04-117">Ao processar esse código de notificação, o aplicativo iniciará a operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="a2d04-117">When processing this notification code, the application will begin the drag-and-drop operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d04-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2d04-118">Requirements</span></span>



| <span data-ttu-id="a2d04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2d04-119">Requirement</span></span> | <span data-ttu-id="a2d04-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a2d04-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d04-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2d04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d04-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2d04-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2d04-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2d04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d04-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2d04-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2d04-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2d04-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2d04-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2d04-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





