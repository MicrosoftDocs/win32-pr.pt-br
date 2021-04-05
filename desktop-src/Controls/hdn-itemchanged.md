---
title: HDN_ITEMCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que os atributos de um item de cabeçalho foram alterados. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- HDN_ITEMCHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008940"
---
# <a name="hdn_itemchanged-notification-code"></a><span data-ttu-id="47e18-105">Código de notificação HDN com \_ alterações</span><span class="sxs-lookup"><span data-stu-id="47e18-105">HDN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="47e18-106">Notifica uma janela pai do controle de cabeçalho que os atributos de um item de cabeçalho foram alterados.</span><span class="sxs-lookup"><span data-stu-id="47e18-106">Notifies a header control's parent window that the attributes of a header item have changed.</span></span> <span data-ttu-id="47e18-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="47e18-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="47e18-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47e18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e18-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47e18-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47e18-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho, incluindo os atributos que foram alterados.</span><span class="sxs-lookup"><span data-stu-id="47e18-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control, including the attributes that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e18-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47e18-111">Return value</span></span>

<span data-ttu-id="47e18-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="47e18-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e18-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47e18-113">Requirements</span></span>



| <span data-ttu-id="47e18-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e18-114">Requirement</span></span> | <span data-ttu-id="47e18-115">Valor</span><span class="sxs-lookup"><span data-stu-id="47e18-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47e18-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47e18-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47e18-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47e18-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47e18-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47e18-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47e18-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="47e18-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47e18-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47e18-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e18-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e18-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="47e18-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="47e18-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="47e18-123">**HDN \_ ITEMCHANGEDW** (Unicode) e **HDN \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="47e18-123">**HDN\_ITEMCHANGEDW** (Unicode) and **HDN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



 

 





