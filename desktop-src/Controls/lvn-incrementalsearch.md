---
title: LVN_INCREMENTALSEARCH código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma pesquisa incremental foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750941"
---
# <a name="lvn_incrementalsearch-notification-code"></a><span data-ttu-id="0cd9a-105">\_Código de notificação INCREMENTALSEARCH LVN</span><span class="sxs-lookup"><span data-stu-id="0cd9a-105">LVN\_INCREMENTALSEARCH notification code</span></span>

<span data-ttu-id="0cd9a-106">Notifica uma janela pai do controle de exibição de lista que uma pesquisa incremental foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-106">Notifies a list-view control's parent window that an incremental search has started.</span></span> <span data-ttu-id="0cd9a-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0cd9a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0cd9a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cd9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cd9a-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cd9a-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cd9a-110">Ponteiro para uma estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que descreve o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-110">Pointer to a [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that describes the notification code.</span></span> <span data-ttu-id="0cd9a-111">O chamador é responsável por alocar essa estrutura, incluindo as estruturas [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) e [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contidas.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) and [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structures.</span></span> <span data-ttu-id="0cd9a-112">Defina os membros da estrutura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="0cd9a-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="0cd9a-113">O membro do **código** deve ser definido como \_ INCREMENTALSEARCH LVN.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-113">The **code** member must be set to LVN\_INCREMENTALSEARCH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cd9a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0cd9a-114">Return value</span></span>

<span data-ttu-id="0cd9a-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cd9a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cd9a-116">Remarks</span></span>

<span data-ttu-id="0cd9a-117">O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="0cd9a-117">The notification receiver casts *lParam* to retrieve the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span> <span data-ttu-id="0cd9a-118">O parâmetro *wParam* contém a ID do controle que envia este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-118">The *wParam* parameter contains the ID of the control that sends this notification code.</span></span>

<span data-ttu-id="0cd9a-119">Esse código de notificação fornece a um aplicativo (ou o receptor de notificação) a oportunidade de personalizar uma pesquisa incremental.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-119">This notification code gives an application (or the notification receiver) the opportunity to customize an incremental search.</span></span> <span data-ttu-id="0cd9a-120">Por exemplo, se os itens de pesquisa forem numéricos, o aplicativo poderá executar uma pesquisa numérica em vez de uma pesquisa de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-120">For example, if the search items are numeric, the application can perform a numerical search instead of a string search.</span></span>

<span data-ttu-id="0cd9a-121">O aplicativo define o membro **lParam** da estrutura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contida na estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) para o resultado da pesquisa ou para outro valor definido do aplicativo para reprovar a pesquisa e indicar ao controle como proceder.</span><span class="sxs-lookup"><span data-stu-id="0cd9a-121">The application sets the **lParam** member of the [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure contained in [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure  to the result of the search, or to another application defined value to fail the search and indicate to the control how to proceed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cd9a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cd9a-122">Requirements</span></span>



| <span data-ttu-id="0cd9a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd9a-123">Requirement</span></span> | <span data-ttu-id="0cd9a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0cd9a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd9a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cd9a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd9a-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0cd9a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0cd9a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cd9a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd9a-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0cd9a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0cd9a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cd9a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cd9a-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cd9a-130"><dt>Commctrl.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cd9a-131">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0cd9a-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0cd9a-132">**LVN \_ INCREMENTALSEARCHW** (Unicode) e **LVN \_ INCREMENTALSEARCHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0cd9a-132">**LVN\_INCREMENTALSEARCHW** (Unicode) and **LVN\_INCREMENTALSEARCHA** (ANSI)</span></span><br/> |



 

 





