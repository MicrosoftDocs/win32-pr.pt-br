---
title: Mensagem de WM_NCHITTEST (WinUser. h)
description: Enviado para uma janela a fim de determinar qual parte da janela corresponde a uma coordenada de tela específica.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Entrada de mouse e teclado de mensagem WM_NCHITTEST
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813580"
---
# <a name="wm_nchittest-message"></a><span data-ttu-id="6d3a3-104">Mensagem do WM \_ NCHITTEST</span><span class="sxs-lookup"><span data-stu-id="6d3a3-104">WM\_NCHITTEST message</span></span>

<span data-ttu-id="6d3a3-105">Enviado para uma janela a fim de determinar qual parte da janela corresponde a uma coordenada de tela específica.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-105">Sent to a window in order to determine what part of the window corresponds to a particular screen coordinate.</span></span> <span data-ttu-id="6d3a3-106">Isso pode acontecer, por exemplo, quando o cursor se move, quando um botão do mouse é pressionado ou liberado, ou em resposta a uma chamada para uma função como [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-106">This can happen, for example, when the cursor moves, when a mouse button is pressed or released, or in response to a call to a function such as [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span></span> <span data-ttu-id="6d3a3-107">Se o mouse não for capturado, a mensagem será enviada para a janela abaixo do cursor.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-107">If the mouse is not captured, the message is sent to the window beneath the cursor.</span></span> <span data-ttu-id="6d3a3-108">Caso contrário, a mensagem será enviada para a janela que capturou o mouse.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-108">Otherwise, the message is sent to the window that has captured the mouse.</span></span>

<span data-ttu-id="6d3a3-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a><span data-ttu-id="6d3a3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d3a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3a3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d3a3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d3a3-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6d3a3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d3a3-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d3a3-114">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-114">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="6d3a3-115">A coordenada é relativa ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-115">The coordinate is relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="6d3a3-116">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-116">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="6d3a3-117">A coordenada é relativa ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-117">The coordinate is relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3a3-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d3a3-118">Return value</span></span>

<span data-ttu-id="6d3a3-119">O valor de retorno da função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) é um dos valores a seguir, indicando a posição do ponto de acesso do cursor.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-119">The return value of the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function is one of the following values, indicating the position of the cursor hot spot.</span></span>



| <span data-ttu-id="6d3a3-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6d3a3-120">Return code/value</span></span>                                                                                                                                    | <span data-ttu-id="6d3a3-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d3a3-121">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d3a3-122"><dt>**HTBORDER**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-122"><dt>**HTBORDER**</dt> <dt>18</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-123">Na borda de uma janela que não tem uma borda de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-123">In the border of a window that does not have a sizing border.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="6d3a3-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-125">Na borda inferior horizontal de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela verticalmente).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-125">In the lower-horizontal border of a resizable window (the user can click the mouse to resize the window vertically).</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="6d3a3-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span></span> </dl>  | <span data-ttu-id="6d3a3-127">No canto inferior esquerdo de uma borda de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela diagonalmente).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-127">In the lower-left corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="6d3a3-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span></span> </dl> | <span data-ttu-id="6d3a3-129">No canto inferior direito de uma borda de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela diagonalmente).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-129">In the lower-right corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="6d3a3-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-131">Em uma barra de título.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-131">In a title bar.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="6d3a3-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="6d3a3-133">Em uma área de cliente.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-133">In a client area.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="6d3a3-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span></span> </dl>       | <span data-ttu-id="6d3a3-135">Em um botão **fechar** .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-135">In a **Close** button.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="6d3a3-136"><dt>**HTERROR**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-136"><dt>**HTERROR**</dt> <dt>-2</dt></span></span> </dl>       | <span data-ttu-id="6d3a3-137">Na tela de fundo ou em uma linha divisória entre janelas (o mesmo que **HTNOWHERE**, exceto que a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) produz um aviso sonoro do sistema para indicar um erro).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-137">On the screen background or on a dividing line between windows (same as **HTNOWHERE**, except that the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function produces a system beep to indicate an error).</span></span><br/> |
| <dl> <span data-ttu-id="6d3a3-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-139">Em uma caixa de tamanho (igual a **HTSIZE**).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-139">In a size box (same as **HTSIZE**).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="6d3a3-140"><dt>**HTHELP**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-140"><dt>**HTHELP**</dt> <dt>21</dt></span></span> </dl>        | <span data-ttu-id="6d3a3-141">Em um botão de **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-141">In a **Help** button.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="6d3a3-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-143">Em uma barra de rolagem horizontal.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-143">In a horizontal scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="6d3a3-144"><dt>**HTLEFT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-144"><dt>**HTLEFT**</dt> <dt>10</dt></span></span> </dl>        | <span data-ttu-id="6d3a3-145">Na borda esquerda de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela horizontalmente).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-145">In the left border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="6d3a3-146"><dt>**HTMENU**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-146"><dt>**HTMENU**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="6d3a3-147">Em um menu.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-147">In a menu.</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="6d3a3-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span></span> </dl>    | <span data-ttu-id="6d3a3-149">Em um botão **maximizar** .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-149">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="6d3a3-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span></span> </dl>    | <span data-ttu-id="6d3a3-151">Em um botão **minimizar** .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-151">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="6d3a3-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-153">Na tela de fundo ou em uma linha divisória entre janelas.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-153">On the screen background or on a dividing line between windows.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="6d3a3-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="6d3a3-155">Em um botão **minimizar** .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-155">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="6d3a3-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span></span> </dl>       | <span data-ttu-id="6d3a3-157">Na borda direita de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela horizontalmente).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-157">In the right border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="6d3a3-158"><dt>**HTSIZE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-158"><dt>**HTSIZE**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="6d3a3-159">Em uma caixa de tamanho (igual a **HTGROWBOX**).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-159">In a size box (same as **HTGROWBOX**).</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="6d3a3-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-161">Em um menu de janela ou em um botão **fechar** em uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-161">In a window menu or in a **Close** button in a child window.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="6d3a3-162"><dt>**HTTOP**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-162"><dt>**HTTOP**</dt> <dt>12</dt></span></span> </dl>         | <span data-ttu-id="6d3a3-163">Na borda superior horizontal de uma janela.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-163">In the upper-horizontal border of a window.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="6d3a3-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span></span> </dl>     | <span data-ttu-id="6d3a3-165">No canto superior esquerdo de uma borda de janela.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-165">In the upper-left corner of a window border.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="6d3a3-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="6d3a3-167">No canto superior direito de uma borda de janela.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-167">In the upper-right corner of a window border.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="6d3a3-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="6d3a3-169">Em uma janela atualmente coberta por outra janela no mesmo thread (a mensagem será enviada para janelas subjacentes no mesmo thread até que um deles retorne um código que não seja **HTTRANSPARENT**).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-169">In a window currently covered by another window in the same thread (the message will be sent to underlying windows in the same thread until one of them returns a code that is not **HTTRANSPARENT**).</span></span><br/>  |
| <dl> <span data-ttu-id="6d3a3-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span></span> </dl>      | <span data-ttu-id="6d3a3-171">Na barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-171">In the vertical scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="6d3a3-172"><dt>**HTZOOM**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-172"><dt>**HTZOOM**</dt> <dt>9</dt></span></span> </dl>         | <span data-ttu-id="6d3a3-173">Em um botão **maximizar** .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-173">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="6d3a3-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d3a3-174">Remarks</span></span>

<span data-ttu-id="6d3a3-175">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="6d3a3-175">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="6d3a3-176">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="6d3a3-176">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="6d3a3-177">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-177">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="6d3a3-178">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-178">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d3a3-179">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-179">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="6d3a3-180">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-180">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="6d3a3-181">**Windows Vista:** Ao criar quadros personalizados que incluem os botões de legenda padrão, essa mensagem deve ser passada primeiro para a função [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="6d3a3-181">**Windows Vista:** When creating custom frames that include the standard caption buttons, this message should first be passed to the [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="6d3a3-182">Isso permite que o Gerenciador de Janelas da Área de Trabalho (DWM) forneça testes de colisão para os botões de legendas.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-182">This enables the Desktop Window Manager (DWM) to provide hit-testing for the captions buttons.</span></span> <span data-ttu-id="6d3a3-183">Se **DwmDefWindowProc** não tratar a mensagem, o processamento adicional do **WM \_ NCHITTEST** poderá ser necessário.</span><span class="sxs-lookup"><span data-stu-id="6d3a3-183">If **DwmDefWindowProc** does not handle the message, further processing of **WM\_NCHITTEST** may be needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3a3-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d3a3-184">Requirements</span></span>



| <span data-ttu-id="6d3a3-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d3a3-185">Requirement</span></span> | <span data-ttu-id="6d3a3-186">Valor</span><span class="sxs-lookup"><span data-stu-id="6d3a3-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3a3-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d3a3-187">Minimum supported client</span></span><br/> | <span data-ttu-id="6d3a3-188">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d3a3-188">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6d3a3-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d3a3-189">Minimum supported server</span></span><br/> | <span data-ttu-id="6d3a3-190">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d3a3-190">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6d3a3-191">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6d3a3-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d3a3-192"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d3a3-192"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d3a3-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d3a3-193">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d3a3-194">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6d3a3-194">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d3a3-195">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6d3a3-195">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6d3a3-196">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="6d3a3-196">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="6d3a3-197">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="6d3a3-197">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

<span data-ttu-id="6d3a3-198">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6d3a3-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6d3a3-199">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="6d3a3-199">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="6d3a3-200">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6d3a3-200">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6d3a3-201">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="6d3a3-201">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="6d3a3-202">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d3a3-202">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

