---
description: A mensagem do WM \_ CTLCOLOR é usada em versões de 16 bits do Windows para alterar o esquema de cores das caixas de listagem, as caixas de listagem de caixas de combinação, caixas de mensagens, controles de botão, controles de edição, controles estáticos e caixas de diálogo. Observação para obter informações relacionadas a essa mensagem e as versões de 32 bits do Windows, consulte comentários.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Mensagem de WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769132"
---
# <a name="wm_ctlcolor-message"></a><span data-ttu-id="caabf-103">Mensagem do WM \_ CTLCOLOR</span><span class="sxs-lookup"><span data-stu-id="caabf-103">WM\_CTLCOLOR message</span></span>

<span data-ttu-id="caabf-104">A mensagem do **WM \_ CTLCOLOR** é usada em versões de 16 bits do Windows para alterar o esquema de cores das caixas de listagem, as caixas de listagem de caixas de combinação, caixas de mensagens, controles de botão, controles de edição, controles estáticos e caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="caabf-104">The **WM\_CTLCOLOR** message is used in 16-bit versions of Windows to change the color scheme of list boxes, the list boxes of combo boxes, message boxes, button controls, edit controls, static controls, and dialog boxes.</span></span>

> [!Note]  
> <span data-ttu-id="caabf-105">Para obter informações relacionadas a essa mensagem e as versões de 32 bits do Windows, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="caabf-105">For information related to this message and 32-bit versions of Windows, see Remarks.</span></span>

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a><span data-ttu-id="caabf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caabf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caabf-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="caabf-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="caabf-108">Um identificador para a janela de destino.</span><span class="sxs-lookup"><span data-stu-id="caabf-108">A handle to destination window.</span></span>

</dd> <dt>

<span data-ttu-id="caabf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="caabf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caabf-110">Um identificador para um contexto de exibição (DC).</span><span class="sxs-lookup"><span data-stu-id="caabf-110">A handle to a display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="caabf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="caabf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caabf-112">Um identificador para uma janela filho (controle).</span><span class="sxs-lookup"><span data-stu-id="caabf-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caabf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="caabf-113">Return value</span></span>

<span data-ttu-id="caabf-114">Se um aplicativo processar essa mensagem, ele retornará um identificador para um pincel.</span><span class="sxs-lookup"><span data-stu-id="caabf-114">If an application processes this message, it returns a handle to a brush.</span></span> <span data-ttu-id="caabf-115">O sistema usa o pincel para pintar o plano de fundo do controle.</span><span class="sxs-lookup"><span data-stu-id="caabf-115">The system uses the brush to paint the background of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="caabf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="caabf-116">Remarks</span></span>

<span data-ttu-id="caabf-117">A mensagem do **WM \_ CTLCOLOR** do Windows de 16 bits foi substituída por notificações mais específicas.</span><span class="sxs-lookup"><span data-stu-id="caabf-117">The **WM\_CTLCOLOR** message from 16-bit Windows has been replaced by more specific notifications.</span></span> <span data-ttu-id="caabf-118">Essas substituições incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="caabf-118">These replacements include the following:</span></span>

-   [<span data-ttu-id="caabf-119">**CTLCOLORBTN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="caabf-119">**WM\_CTLCOLORBTN**</span></span>](../controls/wm-ctlcolorbtn.md)
-   [<span data-ttu-id="caabf-120">**CTLCOLOREDIT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="caabf-120">**WM\_CTLCOLOREDIT**</span></span>](../controls/wm-ctlcoloredit.md)
-   [<span data-ttu-id="caabf-121">**CTLCOLORDLG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="caabf-121">**WM\_CTLCOLORDLG**</span></span>](../dlgbox/wm-ctlcolordlg.md)
-   [<span data-ttu-id="caabf-122">**CTLCOLORLISTBOX do WM \_**</span><span class="sxs-lookup"><span data-stu-id="caabf-122">**WM\_CTLCOLORLISTBOX**</span></span>](../controls/wm-ctlcolorlistbox.md)
-   [<span data-ttu-id="caabf-123">**CTLCOLORSCROLLBAR do WM \_**</span><span class="sxs-lookup"><span data-stu-id="caabf-123">**WM\_CTLCOLORSCROLLBAR**</span></span>](../controls/wm-ctlcolorscrollbar.md)
-   [<span data-ttu-id="caabf-124">**CTLCOLORSTATIC do WM \_**</span><span class="sxs-lookup"><span data-stu-id="caabf-124">**WM\_CTLCOLORSTATIC**</span></span>](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a><span data-ttu-id="caabf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caabf-125">Requirements</span></span>



| <span data-ttu-id="caabf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="caabf-126">Requirement</span></span> | <span data-ttu-id="caabf-127">Valor</span><span class="sxs-lookup"><span data-stu-id="caabf-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="caabf-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="caabf-128">Header</span></span><br/> | <dl> <span data-ttu-id="caabf-129"><dt>WindowsX. h</dt></span><span class="sxs-lookup"><span data-stu-id="caabf-129"><dt>WindowsX.h</dt></span></span> </dl> |



 

 
