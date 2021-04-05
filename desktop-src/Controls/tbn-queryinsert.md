---
title: TBN_QUERYINSERT código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas se um botão pode ser inserido à esquerda do botão especificado enquanto o usuário estiver personalizando uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919082"
---
# <a name="tbn_queryinsert-notification-code"></a><span data-ttu-id="7c6fb-105">Código de notificação do TBN \_ QUERYINSERT</span><span class="sxs-lookup"><span data-stu-id="7c6fb-105">TBN\_QUERYINSERT notification code</span></span>

<span data-ttu-id="7c6fb-106">Notifica a janela pai da barra de ferramentas se um botão pode ser inserido à esquerda do botão especificado enquanto o usuário estiver personalizando uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-106">Notifies the toolbar's parent window whether a button may be inserted to the left of the specified button while the user is customizing a toolbar.</span></span> <span data-ttu-id="7c6fb-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7c6fb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7c6fb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c6fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c6fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6fb-110">Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="7c6fb-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="7c6fb-111">O membro **iItem** contém o índice de base zero do botão a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-111">The **iItem** member contains the zero-based index of the button to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6fb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c6fb-112">Return value</span></span>

<span data-ttu-id="7c6fb-113">Retorne **true** para permitir que um botão seja inserido na frente do botão fornecido ou **false** para impedir que o botão seja inserido.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-113">Return **TRUE** to allow a button to be inserted in front of the given button, or **FALSE** to prevent the button from being inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6fb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c6fb-114">Requirements</span></span>



| <span data-ttu-id="7c6fb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c6fb-115">Requirement</span></span> | <span data-ttu-id="7c6fb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7c6fb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6fb-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c6fb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6fb-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c6fb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c6fb-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c6fb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6fb-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c6fb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c6fb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c6fb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c6fb-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fb-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





