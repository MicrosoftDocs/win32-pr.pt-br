---
description: Enviado antes da mensagem de \_ criação do WM quando uma janela é criada pela primeira vez.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Mensagem de WM_NCCREATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788735"
---
# <a name="wm_nccreate-message"></a><span data-ttu-id="a3870-103">Mensagem do WM \_ NCCREATE</span><span class="sxs-lookup"><span data-stu-id="a3870-103">WM\_NCCREATE message</span></span>

<span data-ttu-id="a3870-104">Enviado antes da mensagem [**de \_ criação do WM**](wm-create.md) quando uma janela é criada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="a3870-104">Sent prior to the [**WM\_CREATE**](wm-create.md) message when a window is first created.</span></span>

<span data-ttu-id="a3870-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a3870-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a><span data-ttu-id="a3870-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3870-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3870-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3870-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3870-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a3870-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a3870-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3870-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3870-110">Um ponteiro para a estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contém informações sobre a janela que está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="a3870-110">A pointer to the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span> <span data-ttu-id="a3870-111">Os membros de **CREATESTRUCT** são idênticos aos parâmetros da função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="a3870-111">The members of **CREATESTRUCT** are identical to the parameters of the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3870-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3870-112">Return value</span></span>

<span data-ttu-id="a3870-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a3870-113">Type: **LRESULT**</span></span>

<span data-ttu-id="a3870-114">Se um aplicativo processar essa mensagem, ele deverá retornar **true** para continuar a criação da janela.</span><span class="sxs-lookup"><span data-stu-id="a3870-114">If an application processes this message, it should return **TRUE** to continue creation of the window.</span></span> <span data-ttu-id="a3870-115">Se o aplicativo retornar **false**, a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retornará um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="a3870-115">If the application returns **FALSE**, the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function will return a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3870-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3870-116">Requirements</span></span>



| <span data-ttu-id="a3870-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3870-117">Requirement</span></span> | <span data-ttu-id="a3870-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a3870-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3870-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3870-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3870-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a3870-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a3870-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3870-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3870-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a3870-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3870-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a3870-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3870-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3870-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3870-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3870-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3870-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a3870-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a3870-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="a3870-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="a3870-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="a3870-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="a3870-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a3870-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a3870-130">**OS CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="a3870-130">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="a3870-131">**criação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a3870-131">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

<span data-ttu-id="a3870-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a3870-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3870-133">Windows</span><span class="sxs-lookup"><span data-stu-id="a3870-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
