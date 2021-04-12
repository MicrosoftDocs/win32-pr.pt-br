---
title: Mensagem de TBN_DELETINGBUTTON (commctrl. h)
description: Enviado por um controle Toolbar quando um botão está prestes a ser excluído. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- Controles de TBN_DELETINGBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499285"
---
# <a name="tbn_deletingbutton-message"></a><span data-ttu-id="98cf2-105">\_Mensagem tbn DELETINGBUTTON</span><span class="sxs-lookup"><span data-stu-id="98cf2-105">TBN\_DELETINGBUTTON message</span></span>

<span data-ttu-id="98cf2-106">Enviado por um controle Toolbar quando um botão está prestes a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="98cf2-106">Sent by a toolbar control when a button is about to be deleted.</span></span> <span data-ttu-id="98cf2-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="98cf2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="98cf2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98cf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98cf2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98cf2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98cf2-110">Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contém informações sobre o botão que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="98cf2-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about the button being deleted.</span></span> <span data-ttu-id="98cf2-111">Para este código de notificação, somente os membros **HDR** e **iItem** dessa estrutura são válidos.</span><span class="sxs-lookup"><span data-stu-id="98cf2-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="98cf2-112">O membro **iItem** dessa estrutura contém o identificador de comando do botão que está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="98cf2-112">The **iItem** member of this structure contains the command identifier of the button being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98cf2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98cf2-113">Return value</span></span>

<span data-ttu-id="98cf2-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="98cf2-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="98cf2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98cf2-115">Requirements</span></span>



| <span data-ttu-id="98cf2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="98cf2-116">Requirement</span></span> | <span data-ttu-id="98cf2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="98cf2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98cf2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98cf2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="98cf2-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98cf2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98cf2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98cf2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="98cf2-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="98cf2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98cf2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98cf2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="98cf2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="98cf2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





