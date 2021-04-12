---
title: TBN_DRAGOVER código de notificação (commctrl. h)
description: Asseguro se uma \_ mensagem MARKBUTTON TB deve ser enviada para um botão que está sendo arrastado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454875"
---
# <a name="tbn_dragover-notification-code"></a><span data-ttu-id="a56c6-105">Código de notificação do TBN \_ DRAGOVER</span><span class="sxs-lookup"><span data-stu-id="a56c6-105">TBN\_DRAGOVER notification code</span></span>

<span data-ttu-id="a56c6-106">Asseguro se uma mensagem [**\_ MARKBUTTON TB**](tb-markbutton.md) deve ser enviada para um botão que está sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="a56c6-106">Ascertains whether a [**TB\_MARKBUTTON**](tb-markbutton.md) message should be sent for a button that is being dragged over.</span></span> <span data-ttu-id="a56c6-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a56c6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a56c6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a56c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a56c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a56c6-110">Um ponteiro para uma estrutura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que especifica qual item está sendo arrastado.</span><span class="sxs-lookup"><span data-stu-id="a56c6-110">A pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that specifies which item is being dragged over.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a56c6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a56c6-111">Return value</span></span>

<span data-ttu-id="a56c6-112">**False** se a barra de ferramentas deve enviar uma \_ mensagem MARKBUTTON TB; caso contrário, **true**.</span><span class="sxs-lookup"><span data-stu-id="a56c6-112">**FALSE** if the toolbar should send a TB\_MARKBUTTON message; otherwise **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a56c6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a56c6-113">Requirements</span></span>



| <span data-ttu-id="a56c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56c6-114">Requirement</span></span> | <span data-ttu-id="a56c6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a56c6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a56c6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a56c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a56c6-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a56c6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a56c6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a56c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a56c6-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a56c6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a56c6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a56c6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a56c6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a56c6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





