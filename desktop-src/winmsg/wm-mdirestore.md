---
description: Um aplicativo envia a mensagem do WM \_ MDIRESTORE para uma janela de cliente MDI (interface de vários documentos) para restaurar uma janela filho MDI do tamanho maximizado ou minimizado.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Mensagem de WM_MDIRESTORE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796258"
---
# <a name="wm_mdirestore-message"></a><span data-ttu-id="a921f-103">Mensagem do WM \_ MDIRESTORE</span><span class="sxs-lookup"><span data-stu-id="a921f-103">WM\_MDIRESTORE message</span></span>

<span data-ttu-id="a921f-104">Um aplicativo envia a mensagem do **WM \_ MDIRESTORE** para uma janela de cliente MDI (interface de vários documentos) para restaurar uma janela filho MDI do tamanho maximizado ou minimizado.</span><span class="sxs-lookup"><span data-stu-id="a921f-104">An application sends the **WM\_MDIRESTORE** message to a multiple-document interface (MDI) client window to restore an MDI child window from maximized or minimized size.</span></span>


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a><span data-ttu-id="a921f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a921f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a921f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a921f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a921f-107">Um identificador para a janela filho MDI a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="a921f-107">A handle to the MDI child window to be restored.</span></span>

</dd> <dt>

<span data-ttu-id="a921f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a921f-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a921f-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a921f-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a921f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a921f-110">Return value</span></span>

<span data-ttu-id="a921f-111">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="a921f-111">Type: **zero**</span></span>

<span data-ttu-id="a921f-112">O valor de retorno é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="a921f-112">The return value is always zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a921f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a921f-113">Requirements</span></span>



| <span data-ttu-id="a921f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a921f-114">Requirement</span></span> | <span data-ttu-id="a921f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a921f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a921f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a921f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a921f-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a921f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a921f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a921f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a921f-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a921f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a921f-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a921f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a921f-121"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a921f-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a921f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a921f-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a921f-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a921f-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a921f-124">**MDIMAXIMIZE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a921f-124">**WM\_MDIMAXIMIZE**</span></span>](wm-mdimaximize.md)
</dt> <dt>

<span data-ttu-id="a921f-125">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a921f-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a921f-126">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="a921f-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




