---
Description: Enviado como um sinal de que uma janela ou um aplicativo deve ser encerrado.
ms.assetid: 19500baf-e0ad-4dfa-804f-6a6e0652cffb
title: Mensagem de WM_CLOSE (WinUser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2f1403050cfd3c98ddf90df4399547158a583c50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791493"
---
# <a name="wm_close-message"></a><span data-ttu-id="10f7d-103">Mensagem de fechamento do WM \_</span><span class="sxs-lookup"><span data-stu-id="10f7d-103">WM\_CLOSE message</span></span>

<span data-ttu-id="10f7d-104">Enviado como um sinal de que uma janela ou um aplicativo deve ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="10f7d-104">Sent as a signal that a window or an application should terminate.</span></span>

<span data-ttu-id="10f7d-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="10f7d-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CLOSE                        0x0010
```



## <a name="parameters"></a><span data-ttu-id="10f7d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10f7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10f7d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10f7d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10f7d-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="10f7d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="10f7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10f7d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10f7d-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="10f7d-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10f7d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10f7d-111">Return value</span></span>

<span data-ttu-id="10f7d-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="10f7d-112">Type: **LRESULT**</span></span>

<span data-ttu-id="10f7d-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="10f7d-113">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="10f7d-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10f7d-114">Example</span></span>

```cpp
LRESULT CALLBACK WindowProc(
    __in HWND hWindow,
    __in UINT uMsg,
    __in WPARAM wParam,
    __in LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CLOSE:
        DestroyWindow(hWindow);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWindow, uMsg, wParam, lParam);
    }

    return 0;
}
```
<span data-ttu-id="10f7d-115">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) no github.</span><span class="sxs-lookup"><span data-stu-id="10f7d-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="10f7d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="10f7d-116">Remarks</span></span>

<span data-ttu-id="10f7d-117">Um aplicativo pode solicitar confirmação ao usuário, antes de destruir uma janela, processando a mensagem **de \_ fechamento do WM** e chamando a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) somente se o usuário confirmar a escolha.</span><span class="sxs-lookup"><span data-stu-id="10f7d-117">An application can prompt the user for confirmation, prior to destroying a window, by processing the **WM\_CLOSE** message and calling the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function only if the user confirms the choice.</span></span>

<span data-ttu-id="10f7d-118">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) chama a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir a janela.</span><span class="sxs-lookup"><span data-stu-id="10f7d-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function calls the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f7d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f7d-119">Requirements</span></span>



| <span data-ttu-id="10f7d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f7d-120">Requirement</span></span> | <span data-ttu-id="10f7d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="10f7d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f7d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10f7d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10f7d-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10f7d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="10f7d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10f7d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10f7d-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10f7d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10f7d-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10f7d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="10f7d-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10f7d-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f7d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="10f7d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="10f7d-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="10f7d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10f7d-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="10f7d-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="10f7d-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="10f7d-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

<span data-ttu-id="10f7d-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="10f7d-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="10f7d-133">Windows</span><span class="sxs-lookup"><span data-stu-id="10f7d-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
