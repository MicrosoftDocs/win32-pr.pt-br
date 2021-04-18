---
title: Player. uiMode
description: A propriedade uiMode especifica ou recupera um valor que indica quais controles são mostrados na interface do usuário.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player. uiMode Windows Media Player
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784545"
---
# <a name="playeruimode"></a><span data-ttu-id="6f402-104">Player. uiMode</span><span class="sxs-lookup"><span data-stu-id="6f402-104">Player.uiMode</span></span>

<span data-ttu-id="6f402-105">A propriedade **UIMODE** especifica ou recupera um valor que indica quais controles são mostrados na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f402-105">The **uiMode** property specifies or retrieves a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f402-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f402-106">Syntax</span></span>

<span data-ttu-id="6f402-107">*Player* . **UIMODE**</span><span class="sxs-lookup"><span data-stu-id="6f402-107">*player* .**uiMode**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6f402-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6f402-108">Possible Values</span></span>

<span data-ttu-id="6f402-109">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6f402-109">This property is a read/write **String**.</span></span>



| <span data-ttu-id="6f402-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6f402-110">Value</span></span>     | <span data-ttu-id="6f402-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f402-111">Description</span></span>                                                                                                                                                                                                           | <span data-ttu-id="6f402-112">Exemplo de áudio</span><span class="sxs-lookup"><span data-stu-id="6f402-112">Audio Example</span></span>                                          | <span data-ttu-id="6f402-113">Exemplo de vídeo</span><span class="sxs-lookup"><span data-stu-id="6f402-113">Video Example</span></span>                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6f402-114">invisível</span><span class="sxs-lookup"><span data-stu-id="6f402-114">invisible</span></span> | <span data-ttu-id="6f402-115">O Windows Media Player é incorporado sem nenhuma interface do usuário visível (janela controles, vídeo ou visualização).</span><span class="sxs-lookup"><span data-stu-id="6f402-115">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                        | <span data-ttu-id="6f402-116">(Nada é exibido.)</span><span class="sxs-lookup"><span data-stu-id="6f402-116">(Nothing is displayed.)</span></span>                                | <span data-ttu-id="6f402-117">(Nada é exibido.)</span><span class="sxs-lookup"><span data-stu-id="6f402-117">(Nothing is displayed.)</span></span>                                |
| <span data-ttu-id="6f402-118">none</span><span class="sxs-lookup"><span data-stu-id="6f402-118">none</span></span>      | <span data-ttu-id="6f402-119">O Windows Media Player é inserido sem controles e apenas com a janela de vídeo ou visualização exibida.</span><span class="sxs-lookup"><span data-stu-id="6f402-119">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                         | !["nenhum" com áudio](images/uimode-none-audio-v11.png) | !["nenhum" com vídeo](images/uimode-none-video-v11.png) |
| <span data-ttu-id="6f402-122">mini-aba</span><span class="sxs-lookup"><span data-stu-id="6f402-122">mini</span></span>      | <span data-ttu-id="6f402-123">O Windows Media Player é inserido com os controles janela de status, reproduzir/pausar, parar, desativar mudo e volume mostrados além da janela vídeo ou visualização.</span><span class="sxs-lookup"><span data-stu-id="6f402-123">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                          | !["mini" com áudio](images/uimode-mini-audio-v11.png) | !["mini" com vídeo](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="6f402-126">completa</span><span class="sxs-lookup"><span data-stu-id="6f402-126">full</span></span>      | <span data-ttu-id="6f402-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="6f402-127">Default.</span></span> <span data-ttu-id="6f402-128">O Windows Media Player é inserido com os controles janela de status, barra de busca, reproduzir/pausar, parar, desativar mudo, avançar, anterior, avançar, reverter e volume, além da janela de vídeo ou visualização.</span><span class="sxs-lookup"><span data-stu-id="6f402-128">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</span></span> | !["completo" com áudio](images/uimode-full-audio-v11.png) | !["completo" com vídeo](images/uimode-full-video-v11.png) |
| <span data-ttu-id="6f402-131">custom</span><span class="sxs-lookup"><span data-stu-id="6f402-131">custom</span></span>    | <span data-ttu-id="6f402-132">O Windows Media Player é inserido com uma interface de usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="6f402-132">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="6f402-133">Só pode ser usado em programas C++.</span><span class="sxs-lookup"><span data-stu-id="6f402-133">Can only be used in C++ programs.</span></span>                                                                                                                      | <span data-ttu-id="6f402-134">(A interface do usuário personalizada é exibida.)</span><span class="sxs-lookup"><span data-stu-id="6f402-134">(Custom user interface is displayed.)</span></span>                  | <span data-ttu-id="6f402-135">(A interface do usuário personalizada é exibida.)</span><span class="sxs-lookup"><span data-stu-id="6f402-135">(Custom user interface is displayed.)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="6f402-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f402-136">Remarks</span></span>

<span data-ttu-id="6f402-137">Esta propriedade especifica a aparência do Windows Media Player inserido.</span><span class="sxs-lookup"><span data-stu-id="6f402-137">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="6f402-138">Quando **UIMODE** é definido como "None", "mini" ou "Full", uma janela está presente para a exibição de clipes de vídeo e visualizações de áudio.</span><span class="sxs-lookup"><span data-stu-id="6f402-138">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="6f402-139">Essa janela pode ser ocultada no modo mini ou Full, definindo o atributo **Height** da marca **Object** como 40, que é medido a partir da parte inferior e deixa a parte dos controles da interface do usuário visível.</span><span class="sxs-lookup"><span data-stu-id="6f402-139">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="6f402-140">Se nenhuma interface inserida for desejada, defina os atributos **Width** e **Height** como zero.</span><span class="sxs-lookup"><span data-stu-id="6f402-140">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="6f402-141">Se **UIMODE** for definido como "invisível", nenhuma interface do usuário será exibida, mas o espaço ainda será reservado na página, conforme especificado por **largura** e **altura**.</span><span class="sxs-lookup"><span data-stu-id="6f402-141">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="6f402-142">Isso é útil para reter o layout da página quando **UIMODE** pode mudar.</span><span class="sxs-lookup"><span data-stu-id="6f402-142">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="6f402-143">Além disso, o espaço reservado é transparente, portanto, todos os elementos em camadas por trás do controle ficarão visíveis.</span><span class="sxs-lookup"><span data-stu-id="6f402-143">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="6f402-144">Se **UIMODE** for definido como "Full" ou "mini", o Windows Media Player exibirá os controles de transporte no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6f402-144">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="6f402-145">Se **UIMODE** for definido como "None", nenhum controle será exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6f402-145">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="6f402-146">Se a janela estiver visível e o conteúdo de áudio estiver sendo reproduzido, a visualização exibida será aquela usada mais recentemente no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6f402-146">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="6f402-147">Se **UIMODE** for definido como "Custom" em um programa C++ que implementa **IWMPRemoteMediaServices**, o arquivo de capa indicado por **IWMPRemoteMediaServices:: GetCustomUIMode** será exibido.</span><span class="sxs-lookup"><span data-stu-id="6f402-147">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices::GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="6f402-148">Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".</span><span class="sxs-lookup"><span data-stu-id="6f402-148">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="6f402-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f402-149">Examples</span></span>

<span data-ttu-id="6f402-150">O exemplo a seguir cria um elemento HTML SELECT que permite ao usuário alterar a interface do usuário para um objeto de **Player** incorporado.</span><span class="sxs-lookup"><span data-stu-id="6f402-150">The following example creates an HTML SELECT element that allows the user to change the user interface for an embedded **Player** object.</span></span> <span data-ttu-id="6f402-151">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6f402-151">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



<span data-ttu-id="6f402-152">Windows Media Player 10 Mobile: essa propriedade só aceita ou retorna valores de "nenhum" ou "completo".</span><span class="sxs-lookup"><span data-stu-id="6f402-152">Windows Media Player 10 Mobile: This property only accepts or returns values of "none" or "full".</span></span> <span data-ttu-id="6f402-153">Em dispositivos Smartphone, somente o status de reprodução e um contador são exibidos quando *UIMODE* é definido como "Full".</span><span class="sxs-lookup"><span data-stu-id="6f402-153">On Smartphone devices, only playback status and a counter are displayed when *uiMode* is set to "full".</span></span>

## <a name="requirements"></a><span data-ttu-id="6f402-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f402-154">Requirements</span></span>



| <span data-ttu-id="6f402-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f402-155">Requirement</span></span> | <span data-ttu-id="6f402-156">Valor</span><span class="sxs-lookup"><span data-stu-id="6f402-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f402-157">Versão</span><span class="sxs-lookup"><span data-stu-id="6f402-157">Version</span></span><br/> | <span data-ttu-id="6f402-158">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6f402-158">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="6f402-159">Windows Media Player 9 Series ou posterior para "invisível" ou "personalizado".</span><span class="sxs-lookup"><span data-stu-id="6f402-159">Windows Media Player 9 Series or later for "invisible" or "custom".</span></span><br/> |
| <span data-ttu-id="6f402-160">DLL</span><span class="sxs-lookup"><span data-stu-id="6f402-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="6f402-161"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f402-161"><dt>Wmp.dll</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="6f402-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f402-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f402-163">**Interface IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="6f402-163">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[<span data-ttu-id="6f402-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span><span class="sxs-lookup"><span data-stu-id="6f402-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[<span data-ttu-id="6f402-165">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="6f402-165">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





