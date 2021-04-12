---
title: NM_CUSTOMTEXT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle sobre as operações de texto personalizado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eebc4033a76d137e28a0c4170c5c613c7933562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369218"
---
# <a name="nm_customtext-notification-code"></a><span data-ttu-id="adb6e-105">\_Código de notificação nm CUSTOMTEXT</span><span class="sxs-lookup"><span data-stu-id="adb6e-105">NM\_CUSTOMTEXT notification code</span></span>

<span data-ttu-id="adb6e-106">Notifica uma janela pai do controle sobre as operações de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="adb6e-106">Notifies a control's parent window about custom text operations.</span></span> <span data-ttu-id="adb6e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="adb6e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="adb6e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adb6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adb6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="adb6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="adb6e-110">Um ponteiro para uma estrutura [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="adb6e-110">A pointer to an [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adb6e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="adb6e-111">Return value</span></span>

<span data-ttu-id="adb6e-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="adb6e-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb6e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adb6e-113">Requirements</span></span>



| <span data-ttu-id="adb6e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="adb6e-114">Requirement</span></span> | <span data-ttu-id="adb6e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="adb6e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adb6e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adb6e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="adb6e-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="adb6e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="adb6e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adb6e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="adb6e-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="adb6e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="adb6e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="adb6e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="adb6e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb6e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





