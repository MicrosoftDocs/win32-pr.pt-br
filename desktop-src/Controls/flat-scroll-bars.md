---
title: Barras de rolagem simples
description: O Microsoft Internet Explorer 4,0 introduziu uma nova tecnologia Visual chamada barras de rolagem simples.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423886"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="576b6-103">Barras de rolagem simples</span><span class="sxs-lookup"><span data-stu-id="576b6-103">Flat Scroll Bars</span></span>

<span data-ttu-id="576b6-104">O Microsoft Internet Explorer 4,0 introduziu uma nova tecnologia Visual chamada barras de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="576b6-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="576b6-105">Funcionalmente, barras de rolagem simples se comportam exatamente como barras de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="576b6-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="576b6-106">A diferença é que você pode personalizar sua aparência para uma extensão maior do que as barras de rolagem padrão.</span><span class="sxs-lookup"><span data-stu-id="576b6-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="576b6-107">A ilustração a seguir mostra uma janela que contém uma barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="576b6-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![captura de tela de uma janela que contém uma barra de rolagem simples](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="576b6-109">As barras de rolagem simples têm suporte em Comctl32.dll versões 4,71 a 5,82.</span><span class="sxs-lookup"><span data-stu-id="576b6-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="576b6-110">Comctl32.dll versões 6, 0 e posteriores não dão suporte a barras de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="576b6-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="576b6-111">Usando barras de rolagem simples</span><span class="sxs-lookup"><span data-stu-id="576b6-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="576b6-112">Esta seção descreve como implementar barras de rolagem simples em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="576b6-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="576b6-113">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="576b6-113">Before You Begin</span></span>

<span data-ttu-id="576b6-114">Para usar as funções da barra de rolagem simples, você deve incluir commctrl. h em seus arquivos de origem e vincular com o Comctl32. lib.</span><span class="sxs-lookup"><span data-stu-id="576b6-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="576b6-115">Adicionando barras de rolagem simples a uma janela</span><span class="sxs-lookup"><span data-stu-id="576b6-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="576b6-116">Para adicionar barras de rolagem simples a uma janela, chame [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passando o identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="576b6-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="576b6-117">Em vez de usar as funções da barra de rolagem padrão para manipular suas barras de rolagem, você deve usar a função equivalente do FlatSB \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="576b6-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="576b6-118">Há funções de barra de rolagem simples para configurar e recuperar as informações de rolagem, o intervalo e a posição.</span><span class="sxs-lookup"><span data-stu-id="576b6-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="576b6-119">Se as barras de rolagem simples não tiverem sido inicializadas para a sua janela, a API da barra de rolagem simples adiará as funções padrão correspondentes, se alguma for usada.</span><span class="sxs-lookup"><span data-stu-id="576b6-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="576b6-120">Isso permite ativar e desativar barras de rolagem simples sem a necessidade de escrever código condicional.</span><span class="sxs-lookup"><span data-stu-id="576b6-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="576b6-121">Como um aplicativo pode ter definido métricas personalizadas para suas barras de rolagem simples, eles não são atualizados automaticamente quando as métricas do sistema são alteradas.</span><span class="sxs-lookup"><span data-stu-id="576b6-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="576b6-122">Quando as métricas da barra de rolagem do sistema mudam, uma mensagem [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) é transmitida, com seu *wParam* definido como [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="576b6-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="576b6-123">Para atualizar barras de rolagem simples para as novas métricas do sistema, os aplicativos devem manipular essa mensagem e alterar explicitamente as propriedades dependentes de métrica da barra de rolagem simples.</span><span class="sxs-lookup"><span data-stu-id="576b6-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="576b6-124">Para atualizar as propriedades da barra de rolagem, use [**FlatSB \_ SetScrollProp.**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop)</span><span class="sxs-lookup"><span data-stu-id="576b6-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="576b6-125">O fragmento de código a seguir altera as propriedades dependentes de métrica de uma barra de rolagem simples para os valores atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="576b6-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="576b6-126">Aprimorando barras de rolagem simples</span><span class="sxs-lookup"><span data-stu-id="576b6-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="576b6-127">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) permite modificar as barras de rolagem simples para personalizar a aparência da janela.</span><span class="sxs-lookup"><span data-stu-id="576b6-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="576b6-128">Para barras de rolagem verticais, você pode alterar a largura da barra e a altura das setas de direção.</span><span class="sxs-lookup"><span data-stu-id="576b6-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="576b6-129">Para barras de rolagem horizontais, você pode alterar a altura da barra e a largura das setas de direção.</span><span class="sxs-lookup"><span data-stu-id="576b6-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="576b6-130">Você também pode alterar a cor da tela de fundo das barras de rolagem horizontais e verticais.</span><span class="sxs-lookup"><span data-stu-id="576b6-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="576b6-131">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) também permite personalizar como as barras de rolagem simples são exibidas.</span><span class="sxs-lookup"><span data-stu-id="576b6-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="576b6-132">Alterando as propriedades WSB PROP VSTYLE e \_ \_ WSB \_ PROP HSTYLE, você pode definir o tipo de barra de rolagem \_ que deseja usar.</span><span class="sxs-lookup"><span data-stu-id="576b6-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="576b6-133">Três estilos estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="576b6-133">Three styles are available.</span></span>



|   <span data-ttu-id="576b6-134">Estilo</span><span class="sxs-lookup"><span data-stu-id="576b6-134">Style</span></span>                 |   <span data-ttu-id="576b6-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="576b6-135">Description</span></span>                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="576b6-136">MODO ENCARTA FSB \_ \_</span><span class="sxs-lookup"><span data-stu-id="576b6-136">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="576b6-137">Uma barra de rolagem simples padrão é exibida.</span><span class="sxs-lookup"><span data-stu-id="576b6-137">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="576b6-138">Quando o mouse se move sobre um botão de direção ou o polegar, essa parte da barra de rolagem será exibida em 3D.</span><span class="sxs-lookup"><span data-stu-id="576b6-138">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="576b6-139">MODO SIMPLES \_ FSB \_</span><span class="sxs-lookup"><span data-stu-id="576b6-139">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="576b6-140">Uma barra de rolagem simples padrão é exibida.</span><span class="sxs-lookup"><span data-stu-id="576b6-140">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="576b6-141">Quando o mouse se move sobre um botão de direção ou o polegar, essa parte da barra de rolagem será exibida em cores invertidas.</span><span class="sxs-lookup"><span data-stu-id="576b6-141">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="576b6-142">MODO \_ REGULAR \_ FSB</span><span class="sxs-lookup"><span data-stu-id="576b6-142">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="576b6-143">Uma barra de rolagem normal e não desfiada é exibida.</span><span class="sxs-lookup"><span data-stu-id="576b6-143">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="576b6-144">Nenhum efeito visual especial será aplicado.</span><span class="sxs-lookup"><span data-stu-id="576b6-144">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="576b6-145">Removendo barras de rolagem simples</span><span class="sxs-lookup"><span data-stu-id="576b6-145">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="576b6-146">Se você quiser remover barras de rolagem simples de sua janela, chame a função [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , passando o identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="576b6-146">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="576b6-147">Essa função remove apenas as barras de rolagem simples da janela em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="576b6-147">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="576b6-148">Você não precisa chamar essa função quando sua janela é destruída.</span><span class="sxs-lookup"><span data-stu-id="576b6-148">You do not need to call this function when your window is destroyed.</span></span>

 

 