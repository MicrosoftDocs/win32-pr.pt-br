---
title: Propriedade AxWindowsMediaPlayer. fullScreen
description: A propriedade fullScreen Obtém ou define um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Propriedade fullScreen Windows Media Player
- Propriedade fullScreen Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759746"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a><span data-ttu-id="6a1e7-106">Propriedade AxWindowsMediaPlayer. fullScreen</span><span class="sxs-lookup"><span data-stu-id="6a1e7-106">AxWindowsMediaPlayer.fullScreen property</span></span>

<span data-ttu-id="6a1e7-107">A propriedade fullScreen Obtém ou define um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-107">The fullScreen property gets or sets a value indicating whether video content is played in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1e7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a1e7-108">Syntax</span></span>


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="6a1e7-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6a1e7-109">Property value</span></span>

<span data-ttu-id="6a1e7-110">Um valor System. Boolean que indica se o conteúdo é reproduzido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-110">A System.Boolean value that indicates whether content is played in full-screen mode.</span></span> <span data-ttu-id="6a1e7-111">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1e7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a1e7-112">Remarks</span></span>

<span data-ttu-id="6a1e7-113">Para que o modo de tela inteira funcione corretamente ao inserir o controle do Windows Media Player, a área de exibição de vídeo deve ter uma altura e largura de pelo menos um pixel.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-113">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="6a1e7-114">Se **UIMODE** for definido como "mini" ou "Full", a altura do controle em si deverá ser 65 ou maior para acomodar a área de exibição do vídeo além da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-114">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="6a1e7-115">Se **UIMODE** for definido como "invisível", a configuração dessa propriedade como true gerará um erro e não afetará o comportamento do controle.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-115">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="6a1e7-116">Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) é igual a false e **UIMODE** é igual a "None".</span><span class="sxs-lookup"><span data-stu-id="6a1e7-116">During full-screen playback, Windows Media Player hides the mouse cursor when [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="6a1e7-117">Se **UIMODE** for definido como "Full" ou "mini", o Windows Media Player exibirá controles de transporte no modo de tela inteira quando o cursor do mouse se mover.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-117">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="6a1e7-118">Após um breve intervalo de sem movimento do mouse, os controles de transporte ficam ocultos.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-118">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="6a1e7-119">Se **UIMODE** for definido como "None", nenhum controle será exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-119">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="6a1e7-120">A exibição de controles de transporte no modo de tela inteira requer o sistema operacional Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-120">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

 

<span data-ttu-id="6a1e7-121">Se os controles de transporte não forem exibidos no modo de tela inteira, o Windows Media Player sairá automaticamente do modo de tela inteira quando a reprodução for interrompida.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-121">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

## <a name="examples"></a><span data-ttu-id="6a1e7-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a1e7-122">Examples</span></span>

<span data-ttu-id="6a1e7-123">O exemplo a seguir cria um botão que usa a propriedade fullScreen para alternar um objeto de player incorporado para o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-123">The following example creates a button that uses the fullScreen property to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="6a1e7-124">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="6a1e7-124">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6a1e7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a1e7-125">Requirements</span></span>



| <span data-ttu-id="6a1e7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a1e7-126">Requirement</span></span> | <span data-ttu-id="6a1e7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6a1e7-127">Value</span></span> |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1e7-128">Versão</span><span class="sxs-lookup"><span data-stu-id="6a1e7-128">Version</span></span><br/>   | <span data-ttu-id="6a1e7-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="6a1e7-129">Windows Media Player 9 Series or later</span></span><br/>                                                                  |
| <span data-ttu-id="6a1e7-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a1e7-130">Namespace</span></span><br/> | <span data-ttu-id="6a1e7-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6a1e7-131">**AxWMPLib**</span></span><br/>                                                                                            |
| <span data-ttu-id="6a1e7-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="6a1e7-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6a1e7-133"><dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6a1e7-133"><dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a1e7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a1e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1e7-135">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6a1e7-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6a1e7-136">**AxWindowsMediaPlayer. uiMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6a1e7-136">**AxWindowsMediaPlayer.uiMode (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





