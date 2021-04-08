---
title: HDN_ITEMCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que os atributos de um item de cabeçalho estão prestes a ser alterados. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824196"
---
# <a name="hdn_itemchanging-notification-code"></a><span data-ttu-id="d91cc-105">Código de notificação de HDN de \_ alteração</span><span class="sxs-lookup"><span data-stu-id="d91cc-105">HDN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="d91cc-106">Notifica uma janela pai do controle de cabeçalho que os atributos de um item de cabeçalho estão prestes a ser alterados.</span><span class="sxs-lookup"><span data-stu-id="d91cc-106">Notifies a header control's parent window that the attributes of a header item are about to change.</span></span> <span data-ttu-id="d91cc-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d91cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d91cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d91cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d91cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d91cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d91cc-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho e o item de cabeçalho, incluindo os atributos que estão prestes a ser alterados.</span><span class="sxs-lookup"><span data-stu-id="d91cc-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d91cc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d91cc-111">Return value</span></span>

<span data-ttu-id="d91cc-112">Retorna **false** para permitir as alterações ou **true** para evitá-las.</span><span class="sxs-lookup"><span data-stu-id="d91cc-112">Returns **FALSE** to allow the changes, or **TRUE** to prevent them.</span></span>

## <a name="requirements"></a><span data-ttu-id="d91cc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d91cc-113">Requirements</span></span>



| <span data-ttu-id="d91cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91cc-114">Requirement</span></span> | <span data-ttu-id="d91cc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d91cc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d91cc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d91cc-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d91cc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d91cc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d91cc-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d91cc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d91cc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d91cc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d91cc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d91cc-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d91cc-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d91cc-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d91cc-123">**HDN \_ ITEMCHANGINGW** (Unicode) e **HDN \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d91cc-123">**HDN\_ITEMCHANGINGW** (Unicode) and **HDN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



 

 





