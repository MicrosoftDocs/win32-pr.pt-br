---
title: Controle Spy v 2.0
description: O Spy Control é uma ferramenta que ajuda os desenvolvedores a entenderem os controles comuns como aplicar estilos a eles e como eles respondem a mensagens e notificações.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104008532"
---
# <a name="control-spy-v20"></a><span data-ttu-id="60bb7-103">Controle Spy v 2.0</span><span class="sxs-lookup"><span data-stu-id="60bb7-103">Control Spy v2.0</span></span>

<span data-ttu-id="60bb7-104">O Spy Control é uma ferramenta que ajuda os desenvolvedores a entenderem os controles comuns: como aplicar estilos a eles e como eles respondem a mensagens e notificações.</span><span class="sxs-lookup"><span data-stu-id="60bb7-104">Control Spy is a tool that helps developers understand common controls: how to apply styles to them, and how they respond to messages and notifications.</span></span> <span data-ttu-id="60bb7-105">Usando o espião de controle, você pode ver imediatamente como os estilos diferentes afetam o comportamento e a aparência de cada controle e também como você pode alterar o estado de cada controle enviando mensagens.</span><span class="sxs-lookup"><span data-stu-id="60bb7-105">Using Control Spy, you can immediately see how different styles affect the behavior and appearance of each control, and also how you can change the state of each control by sending messages.</span></span>

<span data-ttu-id="60bb7-106">Duas versões do Control Spy estão disponíveis, uma para [Comctl32.dll versão 5. x](common-control-versions.md) e outra para Comctl32.dll versão 6,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="60bb7-106">Two versions of Control Spy are available, one for [Comctl32.dll version 5.x](common-control-versions.md) and one for Comctl32.dll version 6.0 and later.</span></span> <span data-ttu-id="60bb7-107">ControlSpyV6.exe tem um manifesto de aplicativo interno para que ele use os controles mais recentes, com tema.</span><span class="sxs-lookup"><span data-stu-id="60bb7-107">ControlSpyV6.exe has a built-in application manifest so that it uses the newer, themed controls.</span></span> <span data-ttu-id="60bb7-108">ControlSpyV5.exe não tem esse manifesto e, por isso, o padrão é a versão mais antiga.</span><span class="sxs-lookup"><span data-stu-id="60bb7-108">ControlSpyV5.exe does not have this manifest and so defaults to the older version.</span></span>

<span data-ttu-id="60bb7-109">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="60bb7-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="60bb7-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="60bb7-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="60bb7-111">Estilos</span><span class="sxs-lookup"><span data-stu-id="60bb7-111">Styles</span></span>](#styles)
-   [<span data-ttu-id="60bb7-112">Mensagens</span><span class="sxs-lookup"><span data-stu-id="60bb7-112">Messages</span></span>](#messages)
-   [<span data-ttu-id="60bb7-113">Tamanho/cor</span><span class="sxs-lookup"><span data-stu-id="60bb7-113">Size/Color</span></span>](#sizecolor)
-   [<span data-ttu-id="60bb7-114">Onde obter o espião de controle</span><span class="sxs-lookup"><span data-stu-id="60bb7-114">Where to Get Control Spy</span></span>](#where-to-get-control-spy)
-   [<span data-ttu-id="60bb7-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60bb7-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="60bb7-116">Visão geral</span><span class="sxs-lookup"><span data-stu-id="60bb7-116">Overview</span></span>

<span data-ttu-id="60bb7-117">O Spy de controle hospeda um controle comum selecionado no centro de sua janela de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60bb7-117">Control Spy hosts a selected common control in the center of its application window.</span></span> <span data-ttu-id="60bb7-118">Você pode alterar qual controle é mostrado selecionando controles diferentes na caixa de listagem no lado esquerdo da janela.</span><span class="sxs-lookup"><span data-stu-id="60bb7-118">You can change which control is shown by selecting different controls from the list box at the left side of the window.</span></span> <span data-ttu-id="60bb7-119">As mensagens ou notificações recebidas pelo controle serão listadas no lado direito da janela à medida que chegarem.</span><span class="sxs-lookup"><span data-stu-id="60bb7-119">Messages or notifications received by the control will be listed at the right side of the window as they arrive.</span></span> <span data-ttu-id="60bb7-120">Você pode habilitar ou desabilitar essa funcionalidade usando as caixas de seleção **mensagens recebidas** e **notificações recebidas** .</span><span class="sxs-lookup"><span data-stu-id="60bb7-120">You can enable or disable this functionality by using the **Messages Received** and **Notifications Received** check boxes.</span></span>

<span data-ttu-id="60bb7-121">A imagem a seguir mostra o aplicativo do Spy Control.</span><span class="sxs-lookup"><span data-stu-id="60bb7-121">The following image shows the Control Spy application.</span></span>

![janela do Spy Control](images/controlspy-main.png)

<span data-ttu-id="60bb7-123">Na parte inferior da janela, há várias guias que apresentam mais funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="60bb7-123">At the bottom of the window, there are several tabs that present more functionality.</span></span>

## <a name="styles"></a><span data-ttu-id="60bb7-124">Estilos</span><span class="sxs-lookup"><span data-stu-id="60bb7-124">Styles</span></span>

<span data-ttu-id="60bb7-125">A guia **estilos** permite que você altere o estilo da janela atual do controle.</span><span class="sxs-lookup"><span data-stu-id="60bb7-125">The **Styles** tab enables you to change the current window style of the control.</span></span> <span data-ttu-id="60bb7-126">Selecione ou desmarque qualquer um dos estilos listados e, em seguida, clique no botão **aplicar** para alterar o estilo do controle exibido.</span><span class="sxs-lookup"><span data-stu-id="60bb7-126">Select or deselect any of the listed styles, then click the **Apply** button to change the style of the displayed control.</span></span> <span data-ttu-id="60bb7-127">Como alternativa, você pode usar o botão **recriar** para criar um novo controle com os estilos selecionados.</span><span class="sxs-lookup"><span data-stu-id="60bb7-127">Alternately, you can use the **Recreate** button to create a new control with the selected styles.</span></span> <span data-ttu-id="60bb7-128">O botão **Redefinir** retornará o controle para os estilos padrão.</span><span class="sxs-lookup"><span data-stu-id="60bb7-128">The **Reset** button will return the control to the default styles.</span></span>

<span data-ttu-id="60bb7-129">Os botões **copiar estilo** e **Copiar do filestyle** abaixo da guia copiarão as constantes de estilo selecionadas para a área de transferência como uma lista de bits ou ( \| ) delimitadas.</span><span class="sxs-lookup"><span data-stu-id="60bb7-129">The **Copy Style** and **Copy ExStyle** buttons below the tab will copy the selected style constants to the Clipboard as a bitwise OR (\|) delimited list.</span></span> <span data-ttu-id="60bb7-130">Você pode colar essa lista diretamente em sua chamada para [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para fornecer um controle em seu próprio aplicativo com o mesmo estilo.</span><span class="sxs-lookup"><span data-stu-id="60bb7-130">You can paste this list directly into your call to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to provide a control in your own application with the same style.</span></span>

<span data-ttu-id="60bb7-131">A imagem a seguir mostra a guia **estilos** de um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="60bb7-131">The following image shows the **Styles** tab for a button control.</span></span>

![guia estilos do Spy Control](images/controlspy-styles.png)

## <a name="messages"></a><span data-ttu-id="60bb7-133">Mensagens</span><span class="sxs-lookup"><span data-stu-id="60bb7-133">Messages</span></span>

<span data-ttu-id="60bb7-134">A guia **mensagens** permite que você envie quase qualquer mensagem a um controle.</span><span class="sxs-lookup"><span data-stu-id="60bb7-134">The **Messages** tab enables you to send almost any message to a control.</span></span> <span data-ttu-id="60bb7-135">Depois de selecionar uma mensagem na caixa de listagem, você pode inserir dados que são enviados como os parâmetros *wParam* e *lParam* da chamada para [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="60bb7-135">After selecting a message from the list box, you can enter data which is sent as the *wParam* and *lParam* parameters of the call to [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="60bb7-136">Depois de clicar em **Enviar**, a mensagem é enviada ao controle e qualquer resultado é exibido na caixa de texto na parte inferior da guia.</span><span class="sxs-lookup"><span data-stu-id="60bb7-136">After you click **Send**, the message is sent to the control and any result is displayed in the text box at the bottom of the tab.</span></span>

<span data-ttu-id="60bb7-137">A imagem a seguir mostra a guia mensagens quando uma determinada mensagem é selecionada.</span><span class="sxs-lookup"><span data-stu-id="60bb7-137">The following image shows the messages tab when a particular message is selected.</span></span>

![guia Mensagens do Spy Control](images/controlspy-messages.png)

## <a name="sizecolor"></a><span data-ttu-id="60bb7-139">Tamanho/cor</span><span class="sxs-lookup"><span data-stu-id="60bb7-139">Size/Color</span></span>

<span data-ttu-id="60bb7-140">A guia **tamanho/cor** pode ser usada para alterar o tamanho do controle, bem como a cor de seu plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="60bb7-140">The **Size/Color** tab can be used to change the size of the control as well as the color of its background.</span></span>

## <a name="where-to-get-control-spy"></a><span data-ttu-id="60bb7-141">Onde obter o espião de controle</span><span class="sxs-lookup"><span data-stu-id="60bb7-141">Where to Get Control Spy</span></span>

<span data-ttu-id="60bb7-142">Você pode baixar o [Control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) do MSDN.</span><span class="sxs-lookup"><span data-stu-id="60bb7-142">You can download [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) from MSDN.</span></span> <span data-ttu-id="60bb7-143">Ambas as versões estão contidas no download.</span><span class="sxs-lookup"><span data-stu-id="60bb7-143">Both versions are contained in the download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60bb7-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60bb7-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="60bb7-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="60bb7-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="60bb7-146">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="60bb7-146">Windows Controls</span></span>](window-controls.md)
</dt> <dt>

[<span data-ttu-id="60bb7-147">Habilitar estilos visuais</span><span class="sxs-lookup"><span data-stu-id="60bb7-147">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> </dl>

 

 