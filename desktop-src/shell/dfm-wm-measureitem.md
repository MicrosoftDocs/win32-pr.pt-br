---
description: Enviado para a janela do proprietário de um controle ou item de menu quando o controle ou o menu é criado.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Mensagem de DFM_WM_MEASUREITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370609"
---
# <a name="dfm_wm_measureitem-message"></a><span data-ttu-id="5fe6e-103">Mensagem do DFM do \_ WM \_ MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="5fe6e-103">DFM\_WM\_MEASUREITEM message</span></span>

<span data-ttu-id="5fe6e-104">Enviado para a janela do proprietário de um controle ou item de menu quando o controle ou o menu é criado.</span><span class="sxs-lookup"><span data-stu-id="5fe6e-104">Sent to the owner window of a control or menu item when the control or menu is created.</span></span>


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a><span data-ttu-id="5fe6e-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fe6e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fe6e-106">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fe6e-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe6e-107">O valor do membro **CtlID** da estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lpMeasureItem* .</span><span class="sxs-lookup"><span data-stu-id="5fe6e-107">The value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter.</span></span> <span data-ttu-id="5fe6e-108">Esse valor identifica o controle que enviou a mensagem **DFM do \_ WM \_ MEASUREITEM** .</span><span class="sxs-lookup"><span data-stu-id="5fe6e-108">This value identifies the control that sent the **DFM\_WM\_MEASUREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6e-109">*lpMeasureItem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5fe6e-109">*lpMeasureItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe6e-110">Um ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contém as dimensões do controle ou item de menu desenhado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="5fe6e-110">A pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fe6e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fe6e-111">Remarks</span></span>

<span data-ttu-id="5fe6e-112">Quando a janela do proprietário recebe a mensagem **DFM do \_ WM \_ MEASUREITEM** , o proprietário preenche a estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lpMeasureItem* da mensagem e retorna; isso informa o sistema das dimensões do controle.</span><span class="sxs-lookup"><span data-stu-id="5fe6e-112">When the owner window receives the **DFM\_WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe6e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fe6e-113">Requirements</span></span>



| <span data-ttu-id="5fe6e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fe6e-114">Requirement</span></span> | <span data-ttu-id="5fe6e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5fe6e-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe6e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fe6e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fe6e-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fe6e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5fe6e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fe6e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fe6e-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5fe6e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5fe6e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fe6e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fe6e-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fe6e-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
