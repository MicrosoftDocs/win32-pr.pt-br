---
title: Mensagem de SETRGBSTRING (Commdlg. h)
description: O procedimento de gancho de uma caixa de diálogo de cor, CCHookProc, pode enviar a mensagem registrada SETRGBSTRING para a caixa de diálogo para definir a seleção de cor atual.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Caixas de diálogo de mensagem SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644921"
---
# <a name="setrgbstring-message"></a><span data-ttu-id="57072-104">Mensagem SETRGBSTRING</span><span class="sxs-lookup"><span data-stu-id="57072-104">SETRGBSTRING message</span></span>

<span data-ttu-id="57072-105">O procedimento de gancho de uma caixa de diálogo de **cor** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), pode enviar a mensagem registrada **SETRGBSTRING** para a caixa de diálogo para definir a seleção de cor atual.</span><span class="sxs-lookup"><span data-stu-id="57072-105">The hook procedure of a **Color** dialog box, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), can send the **SETRGBSTRING** registered message to the dialog box to set the current color selection.</span></span>


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a><span data-ttu-id="57072-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57072-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57072-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57072-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57072-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="57072-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57072-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57072-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57072-110">O valor RGB da cor a ser selecionada na caixa de diálogo **cor** .</span><span class="sxs-lookup"><span data-stu-id="57072-110">The RGB value of the color to select in the **Color** dialog box.</span></span> <span data-ttu-id="57072-111">Você pode usar a macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para especificar as intensidades vermelhas, verdes e azuis de um valor de cor RGB.</span><span class="sxs-lookup"><span data-stu-id="57072-111">You can use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro to specify the red, green, and blue intensities of an RGB color value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57072-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57072-112">Return value</span></span>

<span data-ttu-id="57072-113">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="57072-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57072-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="57072-114">Remarks</span></span>

<span data-ttu-id="57072-115">Se *lParam* corresponder a uma das cores básicas ou a uma das 16 cores personalizadas, o procedimento da caixa de diálogo selecionará essa cor.</span><span class="sxs-lookup"><span data-stu-id="57072-115">If *lParam* matches one of the basic colors or one of the 16 custom colors, the dialog box procedure selects that color.</span></span> <span data-ttu-id="57072-116">O procedimento da caixa de diálogo também atualiza todos os controles na extensão de cor personalizada da caixa de diálogo **cor** , se ela estiver aberta.</span><span class="sxs-lookup"><span data-stu-id="57072-116">The dialog box procedure also updates all the controls in the custom color extension of the **Color** dialog box, if it is open.</span></span>

<span data-ttu-id="57072-117">Se *lParam* não corresponder a uma cor básica ou personalizada, o procedimento da caixa de diálogo não alterará a seleção de cor atual, mas atualizará os controles de cor personalizados, se estiverem visíveis.</span><span class="sxs-lookup"><span data-stu-id="57072-117">If *lParam* does not match a basic or custom color, the dialog box procedure does not change the current color selection, but it does update the custom color controls, if they are visible.</span></span>

## <a name="examples"></a><span data-ttu-id="57072-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57072-118">Examples</span></span>

<span data-ttu-id="57072-119">O código de exemplo a seguir obtém o identificador de mensagem **SETRGBSTRING** e, em seguida, define a seleção de cor como azul.</span><span class="sxs-lookup"><span data-stu-id="57072-119">The following sample code gets the **SETRGBSTRING** message identifier and then sets the color selection to blue.</span></span>


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a><span data-ttu-id="57072-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57072-120">Requirements</span></span>



| <span data-ttu-id="57072-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="57072-121">Requirement</span></span> | <span data-ttu-id="57072-122">Valor</span><span class="sxs-lookup"><span data-stu-id="57072-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57072-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57072-123">Minimum supported client</span></span><br/> | <span data-ttu-id="57072-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="57072-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="57072-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57072-125">Minimum supported server</span></span><br/> | <span data-ttu-id="57072-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="57072-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57072-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="57072-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="57072-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57072-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="57072-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="57072-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57072-130">**SETRGBSTRINGW** (Unicode) e **SETRGBSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="57072-130">**SETRGBSTRINGW** (Unicode) and **SETRGBSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="57072-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="57072-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="57072-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="57072-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57072-133">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="57072-133">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="57072-134">**RGB**</span><span class="sxs-lookup"><span data-stu-id="57072-134">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[<span data-ttu-id="57072-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="57072-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

<span data-ttu-id="57072-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="57072-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57072-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="57072-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

