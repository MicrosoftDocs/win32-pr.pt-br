---
title: Propriedade AxWindowsMediaPlayer. uiMode
description: A propriedade uiMode Obtém ou define um valor que indica quais controles são mostrados na interface do usuário.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- Propriedade uiMode Windows Media Player
- Propriedade uiMode Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781057"
---
# <a name="axwindowsmediaplayeruimode-property"></a><span data-ttu-id="ff65d-106">Propriedade AxWindowsMediaPlayer. uiMode</span><span class="sxs-lookup"><span data-stu-id="ff65d-106">AxWindowsMediaPlayer.uiMode property</span></span>

<span data-ttu-id="ff65d-107">A propriedade uiMode Obtém ou define um valor que indica quais controles são mostrados na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff65d-107">The uiMode property gets or sets a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff65d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff65d-108">Syntax</span></span>


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a><span data-ttu-id="ff65d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ff65d-109">Property value</span></span>

<span data-ttu-id="ff65d-110">Um System. String que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff65d-110">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="ff65d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ff65d-111">Value</span></span>     | <span data-ttu-id="ff65d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff65d-112">Description</span></span>                                                                                                                                                                                                     | <span data-ttu-id="ff65d-113">Exemplo de áudio</span><span class="sxs-lookup"><span data-stu-id="ff65d-113">Audio example</span></span>                                                   | <span data-ttu-id="ff65d-114">Exemplo de vídeo</span><span class="sxs-lookup"><span data-stu-id="ff65d-114">Video example</span></span>                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ff65d-115">invisível</span><span class="sxs-lookup"><span data-stu-id="ff65d-115">invisible</span></span> | <span data-ttu-id="ff65d-116">O Windows Media Player é incorporado sem nenhuma interface do usuário visível (janela controles, vídeo ou visualização).</span><span class="sxs-lookup"><span data-stu-id="ff65d-116">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                  | <span data-ttu-id="ff65d-117">(Nada é exibido.)</span><span class="sxs-lookup"><span data-stu-id="ff65d-117">(Nothing is displayed.)</span></span>                                         | <span data-ttu-id="ff65d-118">(Nada é exibido.)</span><span class="sxs-lookup"><span data-stu-id="ff65d-118">(Nothing is displayed.)</span></span>                                         |
| <span data-ttu-id="ff65d-119">none</span><span class="sxs-lookup"><span data-stu-id="ff65d-119">none</span></span>      | <span data-ttu-id="ff65d-120">O Windows Media Player é inserido sem controles e apenas com a janela de vídeo ou visualização exibida.</span><span class="sxs-lookup"><span data-stu-id="ff65d-120">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                   | ![UIMode = ' none ' com áudio](images/uimode-none-audio-v11.png) | ![UIMode = ' none ' com vídeo](images/uimode-none-video-v11.png) |
| <span data-ttu-id="ff65d-123">mini-aba</span><span class="sxs-lookup"><span data-stu-id="ff65d-123">mini</span></span>      | <span data-ttu-id="ff65d-124">O Windows Media Player é inserido com os controles janela de status, reproduzir/pausar, parar, desativar mudo e volume mostrados além da janela vídeo ou visualização.</span><span class="sxs-lookup"><span data-stu-id="ff65d-124">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                    | ![UIMode = ' Mini ' com áudio](images/uimode-mini-audio-v11.png) | ![UIMode = ' Mini ' com vídeo](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="ff65d-127">completa</span><span class="sxs-lookup"><span data-stu-id="ff65d-127">full</span></span>      | <span data-ttu-id="ff65d-128">Padrão.</span><span class="sxs-lookup"><span data-stu-id="ff65d-128">Default.</span></span> <span data-ttu-id="ff65d-129">O Windows Media Player é inserido com os controles janela de status, barra de busca, reproduzir/pausar, parar, desativar mudo, avançar, anterior, avançar, retroceder e volume, além da janela vídeo ou visualização.</span><span class="sxs-lookup"><span data-stu-id="ff65d-129">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, rewind, and volume controls in addition to the video or visualization window.</span></span> | ![UIMode = ' full ' com áudio](images/uimode-full-audio-v11.png) | ![UIMode = ' full ' com vídeo](images/uimode-full-video-v11.png) |
| <span data-ttu-id="ff65d-132">custom</span><span class="sxs-lookup"><span data-stu-id="ff65d-132">custom</span></span>    | <span data-ttu-id="ff65d-133">O Windows Media Player é inserido com uma interface de usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="ff65d-133">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="ff65d-134">Só pode ser usado em programas C++.</span><span class="sxs-lookup"><span data-stu-id="ff65d-134">Can only be used in C++ programs.</span></span>                                                                                                                | <span data-ttu-id="ff65d-135">(A interface do usuário personalizada é exibida.)</span><span class="sxs-lookup"><span data-stu-id="ff65d-135">(Custom user interface is displayed.)</span></span>                           | <span data-ttu-id="ff65d-136">(A interface do usuário personalizada é exibida.)</span><span class="sxs-lookup"><span data-stu-id="ff65d-136">(Custom user interface is displayed.)</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="ff65d-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff65d-137">Remarks</span></span>

<span data-ttu-id="ff65d-138">Esta propriedade especifica a aparência do Windows Media Player inserido.</span><span class="sxs-lookup"><span data-stu-id="ff65d-138">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="ff65d-139">Quando **UIMODE** é definido como "None", "mini" ou "Full", uma janela está presente para a exibição de clipes de vídeo e visualizações de áudio.</span><span class="sxs-lookup"><span data-stu-id="ff65d-139">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="ff65d-140">Essa janela pode ser ocultada no modo mini ou Full, definindo o atributo **Height** da marca **Object** como 40, que é medido a partir da parte inferior e deixa a parte dos controles da interface do usuário visível.</span><span class="sxs-lookup"><span data-stu-id="ff65d-140">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="ff65d-141">Se nenhuma interface inserida for desejada, defina os atributos **Width** e **Height** como zero.</span><span class="sxs-lookup"><span data-stu-id="ff65d-141">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="ff65d-142">Se **UIMODE** for definido como "invisível", nenhuma interface do usuário será exibida, mas o espaço ainda será reservado na página, conforme especificado por **largura** e **altura**.</span><span class="sxs-lookup"><span data-stu-id="ff65d-142">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="ff65d-143">Isso é útil para reter o layout da página quando **UIMODE** pode mudar.</span><span class="sxs-lookup"><span data-stu-id="ff65d-143">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="ff65d-144">Além disso, o espaço reservado é transparente, portanto, todos os elementos em camadas por trás do controle ficarão visíveis.</span><span class="sxs-lookup"><span data-stu-id="ff65d-144">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="ff65d-145">Se **UIMODE** for definido como "Full" ou "mini", o Windows Media Player exibirá os controles de transporte no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="ff65d-145">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="ff65d-146">Se **UIMODE** for definido como "None", nenhum controle será exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="ff65d-146">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="ff65d-147">Se a janela estiver visível e o conteúdo de áudio estiver sendo reproduzido, a visualização exibida será aquela usada mais recentemente no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ff65d-147">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="ff65d-148">Se **UIMODE** for definido como "Custom" em um programa C++ que implementa **IWMPRemoteMediaServices**, o arquivo de capa indicado por **IWMPRemoteMediaServices. GetCustomUIMode** será exibido.</span><span class="sxs-lookup"><span data-stu-id="ff65d-148">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices.GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="ff65d-149">Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".</span><span class="sxs-lookup"><span data-stu-id="ff65d-149">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="ff65d-150">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff65d-150">Examples</span></span>

<span data-ttu-id="ff65d-151">O exemplo a seguir cria uma caixa de listagem que permite ao usuário alterar o modo de interface do usuário para um objeto incorporado do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ff65d-151">The following example creates a list box that allows the user to change the user interface mode for an embedded Windows Media Player object.</span></span> <span data-ttu-id="ff65d-152">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="ff65d-152">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ff65d-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff65d-153">Requirements</span></span>



| <span data-ttu-id="ff65d-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff65d-154">Requirement</span></span> | <span data-ttu-id="ff65d-155">Valor</span><span class="sxs-lookup"><span data-stu-id="ff65d-155">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff65d-156">Versão</span><span class="sxs-lookup"><span data-stu-id="ff65d-156">Version</span></span><br/>   | <span data-ttu-id="ff65d-157">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ff65d-157">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="ff65d-158">Windows Media Player 9 Series ou posterior para "invisível" ou "personalizado"</span><span class="sxs-lookup"><span data-stu-id="ff65d-158">Windows Media Player 9 Series or later for "invisible" or "custom"</span></span><br/>   |
| <span data-ttu-id="ff65d-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff65d-159">Namespace</span></span><br/> | <span data-ttu-id="ff65d-160">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ff65d-160">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ff65d-161">Assembly</span><span class="sxs-lookup"><span data-stu-id="ff65d-161">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ff65d-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ff65d-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff65d-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff65d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff65d-164">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ff65d-164">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ff65d-165">**AxWindowsMediaPlayer. enableContextMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ff65d-165">**AxWindowsMediaPlayer.enableContextMenu (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





