---
description: Enviado para a janela afetada na extremidade superior após a alteração do idioma de entrada de um aplicativo. Você deve fazer qualquer configuração específica do aplicativo e passar a mensagem para a função DefWindowProc, que passa a mensagem para todas as janelas filho de primeiro nível.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Mensagem de WM_INPUTLANGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332401"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="0e4f4-104">Mensagem do WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="0e4f4-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="0e4f4-105">Enviado para a janela afetada na extremidade superior após a alteração do idioma de entrada de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e4f4-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="0e4f4-106">Você deve fazer qualquer configuração específica do aplicativo e passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que passa a mensagem para todas as janelas filho de primeiro nível.</span><span class="sxs-lookup"><span data-stu-id="0e4f4-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="0e4f4-107">Essas janelas filhas podem passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que ela passe a mensagem para suas janelas filhas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0e4f4-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="0e4f4-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0e4f4-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a><span data-ttu-id="0e4f4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e4f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e4f4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e4f4-110">*wParam*</span></span>

</dt> <dd>
  
<span data-ttu-id="0e4f4-111">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="0e4f4-111">Type: **WPARAM**</span></span>

<span data-ttu-id="0e4f4-112">A [página de código](../Intl/code-pages.md) da nova localidade.</span><span class="sxs-lookup"><span data-stu-id="0e4f4-112">The [code page](../Intl/code-pages.md) of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="0e4f4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e4f4-113">*lParam*</span></span>

</dt> <dd>
 
<span data-ttu-id="0e4f4-114">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="0e4f4-114">Type: **LPARAM**</span></span>

<span data-ttu-id="0e4f4-115">O identificador de localidade de entrada **HKL** .</span><span class="sxs-lookup"><span data-stu-id="0e4f4-115">The **HKL** input locale identifier.</span></span> <span data-ttu-id="0e4f4-116">Para obter mais informações, consulte [idiomas, localidades e layouts de teclado](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="0e4f4-116">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e4f4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e4f4-117">Return value</span></span>

<span data-ttu-id="0e4f4-118">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0e4f4-118">Type: **LRESULT**</span></span>

<span data-ttu-id="0e4f4-119">Um aplicativo deve retornar diferente de zero se processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="0e4f4-119">An application should return nonzero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e4f4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e4f4-120">Remarks</span></span>

<span data-ttu-id="0e4f4-121">Você pode recuperar o [nome da localidade](../Intl/locale-names.md) do teclado por meio da função [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) .</span><span class="sxs-lookup"><span data-stu-id="0e4f4-121">You can retrieve keyboard [locale name](../Intl/locale-names.md) via [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) function.</span></span> <span data-ttu-id="0e4f4-122">Com o nome da localidade, você pode usar [funções de localidade modernas](/windows/win32/intl/calling-the--locale-name--functions):</span><span class="sxs-lookup"><span data-stu-id="0e4f4-122">With locale name you can use [modern locale functions](/windows/win32/intl/calling-the--locale-name--functions):</span></span>

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a><span data-ttu-id="0e4f4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e4f4-123">Requirements</span></span>

| <span data-ttu-id="0e4f4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e4f4-124">Requirement</span></span> | <span data-ttu-id="0e4f4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0e4f4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e4f4-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e4f4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e4f4-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e4f4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0e4f4-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e4f4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e4f4-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e4f4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e4f4-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0e4f4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e4f4-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e4f4-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="0e4f4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e4f4-132">See also</span></span>

<span data-ttu-id="0e4f4-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0e4f4-133">**Reference**</span></span>

- [<span data-ttu-id="0e4f4-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0e4f4-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [<span data-ttu-id="0e4f4-135">**INPUTLANGCHANGEREQUEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0e4f4-135">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)

<span data-ttu-id="0e4f4-136">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="0e4f4-136">**Conceptual**</span></span>

- [<span data-ttu-id="0e4f4-137">Windows</span><span class="sxs-lookup"><span data-stu-id="0e4f4-137">Windows</span></span>](windows.md) 
