---
title: Mensagem de CB_GETEDITSEL (WinUser. h)
description: Obtém as posições de caractere inicial e final da seleção atual no controle de edição de uma caixa de combinação.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- Controles de CB_GETEDITSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009365"
---
# <a name="cb_geteditsel-message"></a><span data-ttu-id="4579a-104">\_Mensagem de GETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="4579a-104">CB\_GETEDITSEL message</span></span>

<span data-ttu-id="4579a-105">Obtém as posições de caractere inicial e final da seleção atual no controle de edição de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="4579a-105">Gets the starting and ending character positions of the current selection in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="4579a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4579a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4579a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4579a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4579a-108">Um ponteiro para um valor **DWORD** que recebe a posição inicial da seleção.</span><span class="sxs-lookup"><span data-stu-id="4579a-108">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="4579a-109">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4579a-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4579a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4579a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4579a-111">Um ponteiro para um valor **DWORD** que recebe a posição final da seleção.</span><span class="sxs-lookup"><span data-stu-id="4579a-111">A pointer to a **DWORD** value that receives the ending position of the selection.</span></span> <span data-ttu-id="4579a-112">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4579a-112">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4579a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4579a-113">Return value</span></span>

<span data-ttu-id="4579a-114">O valor de retorno é um valor **DWORD** com base em zero com a posição inicial da seleção no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e com a posição final do primeiro caractere após o último caractere selecionado no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4579a-114">The return value is a zero-based **DWORD** value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and with the ending position of the first character after the last selected character in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="4579a-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4579a-115">Examples</span></span>

<span data-ttu-id="4579a-116">O exemplo de código a seguir mostra duas maneiras de recuperar o intervalo de seleção atual.</span><span class="sxs-lookup"><span data-stu-id="4579a-116">The following code example shows two ways of retrieving the current selection range.</span></span>


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a><span data-ttu-id="4579a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4579a-117">Requirements</span></span>



| <span data-ttu-id="4579a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4579a-118">Requirement</span></span> | <span data-ttu-id="4579a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4579a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4579a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4579a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4579a-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4579a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4579a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4579a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4579a-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4579a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4579a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4579a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4579a-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4579a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4579a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4579a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="4579a-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4579a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4579a-128">**\_SETEDITSEL CB**</span><span class="sxs-lookup"><span data-stu-id="4579a-128">**CB\_SETEDITSEL**</span></span>](cb-seteditsel.md)
</dt> <dt>

<span data-ttu-id="4579a-129">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="4579a-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4579a-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4579a-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="4579a-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4579a-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

