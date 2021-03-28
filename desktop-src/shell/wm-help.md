---
description: Indica que o usuário pressionou a tecla F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Mensagem de WM_HELP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967878"
---
# <a name="wm_help-message"></a><span data-ttu-id="bedbb-103">Mensagem de ajuda do WM \_</span><span class="sxs-lookup"><span data-stu-id="bedbb-103">WM\_HELP message</span></span>

<span data-ttu-id="bedbb-104">Indica que o usuário pressionou a tecla F1.</span><span class="sxs-lookup"><span data-stu-id="bedbb-104">Indicates that the user pressed the F1 key.</span></span> <span data-ttu-id="bedbb-105">Se um menu estiver ativo quando F1 for pressionado, **a \_ ajuda do WM** será enviada para a janela associada ao menu; caso contrário, a **\_ ajuda do WM** será enviada para a janela que tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="bedbb-105">If a menu is active when F1 is pressed, **WM\_HELP** is sent to the window associated with the menu; otherwise, **WM\_HELP** is sent to the window that has the keyboard focus.</span></span> <span data-ttu-id="bedbb-106">Se nenhuma janela tiver o foco do teclado, a **\_ ajuda do WM** será enviada para a janela ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="bedbb-106">If no window has the keyboard focus, **WM\_HELP** is sent to the currently active window.</span></span>

## <a name="parameters"></a><span data-ttu-id="bedbb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bedbb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bedbb-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bedbb-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bedbb-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bedbb-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bedbb-110">*lphi*</span><span class="sxs-lookup"><span data-stu-id="bedbb-110">*lphi*</span></span> 
</dt> <dd>

<span data-ttu-id="bedbb-111">O endereço de uma estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contém informações sobre o item de menu, controle, caixa de diálogo ou janela para a qual a ajuda é solicitada.</span><span class="sxs-lookup"><span data-stu-id="bedbb-111">The address of a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains information about the menu item, control, dialog box, or window for which Help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bedbb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bedbb-112">Return value</span></span>

<span data-ttu-id="bedbb-113">Retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="bedbb-113">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bedbb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bedbb-114">Remarks</span></span>

<span data-ttu-id="bedbb-115">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa **a \_ ajuda do WM** para a janela pai de uma janela filho ou para o proprietário de uma janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="bedbb-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes **WM\_HELP** to the parent window of a child window or to the owner of a top-level window.</span></span>

## <a name="requirements"></a><span data-ttu-id="bedbb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bedbb-116">Requirements</span></span>



| <span data-ttu-id="bedbb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bedbb-117">Requirement</span></span> | <span data-ttu-id="bedbb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bedbb-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bedbb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bedbb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bedbb-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bedbb-120">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bedbb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bedbb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bedbb-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bedbb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bedbb-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bedbb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bedbb-124"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="bedbb-124"><dt>Winuser.h</dt></span></span> </dl> |



 

 
