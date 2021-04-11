---
title: Mensagem de DM_REPOSITION (WinUser. h)
description: Reposiciona uma caixa de diálogo de nível superior para que ela caiba na área de área de trabalho. Um aplicativo pode enviar essa mensagem a uma caixa de diálogo depois de redimensioná-la para garantir que toda a caixa de diálogo permaneça visível.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Caixas de diálogo de DM_REPOSITION mensagem
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009723"
---
# <a name="dm_reposition-message"></a><span data-ttu-id="e2252-105">\_Mensagem de REposicionamento de DM</span><span class="sxs-lookup"><span data-stu-id="e2252-105">DM\_REPOSITION message</span></span>

<span data-ttu-id="e2252-106">Reposiciona uma caixa de diálogo de nível superior para que ela caiba na área de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2252-106">Repositions a top-level dialog box so that it fits within the desktop area.</span></span> <span data-ttu-id="e2252-107">Um aplicativo pode enviar essa mensagem a uma caixa de diálogo depois de redimensioná-la para garantir que toda a caixa de diálogo permaneça visível.</span><span class="sxs-lookup"><span data-stu-id="e2252-107">An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.</span></span>


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="e2252-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2252-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2252-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2252-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2252-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e2252-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2252-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2252-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2252-112">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e2252-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2252-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2252-113">Return value</span></span>

<span data-ttu-id="e2252-114">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e2252-114">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2252-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2252-115">Remarks</span></span>

<span data-ttu-id="e2252-116">Essa mensagem não terá efeito se a caixa de diálogo for uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="e2252-116">This message has no effect if the dialog box is a child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2252-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2252-117">Requirements</span></span>



| <span data-ttu-id="e2252-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2252-118">Requirement</span></span> | <span data-ttu-id="e2252-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e2252-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2252-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2252-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2252-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e2252-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e2252-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2252-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2252-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e2252-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2252-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e2252-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2252-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2252-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2252-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2252-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2252-127">Visão geral das caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="e2252-127">Dialog Boxes Overview</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





