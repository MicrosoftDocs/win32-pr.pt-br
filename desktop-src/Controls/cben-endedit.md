---
title: CBEN_ENDEDIT código de notificação (commctrl. h)
description: Enviado quando o usuário concluiu uma operação na caixa de edição ou selecionou um item na lista suspensa do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369254"
---
# <a name="cben_endedit-notification-code"></a><span data-ttu-id="70c31-105">Código de notificação do CBEN \_ ENDEDIT</span><span class="sxs-lookup"><span data-stu-id="70c31-105">CBEN\_ENDEDIT notification code</span></span>

<span data-ttu-id="70c31-106">Enviado quando o usuário concluiu uma operação na caixa de edição ou selecionou um item na lista suspensa do controle.</span><span class="sxs-lookup"><span data-stu-id="70c31-106">Sent when the user has concluded an operation within the edit box or has selected an item from the control's drop-down list.</span></span> <span data-ttu-id="70c31-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="70c31-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="70c31-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70c31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70c31-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70c31-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70c31-110">Um ponteiro para uma estrutura [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) que contém informações sobre como o usuário concluiu a operação de edição.</span><span class="sxs-lookup"><span data-stu-id="70c31-110">A pointer to an [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) structure that contains information about how the user concluded the edit operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70c31-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70c31-111">Return value</span></span>

<span data-ttu-id="70c31-112">**False** para aceitar o código de notificação e permitir que o controle exiba o item selecionado; caso contrário, **true**.</span><span class="sxs-lookup"><span data-stu-id="70c31-112">**FALSE** to accept the notification code and allow the control to display the selected item; otherwise, **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c31-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70c31-113">Requirements</span></span>



| <span data-ttu-id="70c31-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c31-114">Requirement</span></span> | <span data-ttu-id="70c31-115">Valor</span><span class="sxs-lookup"><span data-stu-id="70c31-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70c31-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c31-116">Minimum supported client</span></span><br/> | <span data-ttu-id="70c31-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70c31-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70c31-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c31-118">Minimum supported server</span></span><br/> | <span data-ttu-id="70c31-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70c31-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70c31-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70c31-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c31-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c31-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="70c31-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="70c31-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="70c31-123">**CBEN \_ ENDEDITW** (Unicode) e **CBEN \_ endediçãoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="70c31-123">**CBEN\_ENDEDITW** (Unicode) and **CBEN\_ENDEDITA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="70c31-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="70c31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c31-125">Sobre controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="70c31-125">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> </dl>

 

 





