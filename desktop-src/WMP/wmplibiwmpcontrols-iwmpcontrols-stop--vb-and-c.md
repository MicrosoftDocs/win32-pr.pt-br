---
title: Método IWMPControls Stop
description: O método Stop interrompe a reprodução do item de mídia. | Método IWMPControls Stop
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- método Stop Windows Media Player
- método Stop Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, método Stop
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788016"
---
# <a name="iwmpcontrolsstop-method"></a><span data-ttu-id="4eec2-107">Método IWMPControls:: Stop</span><span class="sxs-lookup"><span data-stu-id="4eec2-107">IWMPControls::stop method</span></span>

<span data-ttu-id="4eec2-108">O método **Stop** interrompe a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="4eec2-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eec2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4eec2-109">Syntax</span></span>


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a><span data-ttu-id="4eec2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4eec2-110">Parameters</span></span>

<span data-ttu-id="4eec2-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4eec2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4eec2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4eec2-112">Return value</span></span>

<span data-ttu-id="4eec2-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4eec2-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eec2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4eec2-114">Remarks</span></span>

<span data-ttu-id="4eec2-115">Esse método faz com que o Windows Media Player libere os recursos do sistema que está usando, como o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="4eec2-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="4eec2-116">O item de mídia atual, no entanto, não é liberado.</span><span class="sxs-lookup"><span data-stu-id="4eec2-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="4eec2-117">Quando o Windows Media Player é interrompido, a posição de reprodução atual no item de mídia é redefinida para o início do item.</span><span class="sxs-lookup"><span data-stu-id="4eec2-117">When Windows Media Player is stopped, the current playback position in the media item is reset to the beginning of the item.</span></span> <span data-ttu-id="4eec2-118">Posteriormente, chamar **IWMPControls. Play** iniciará a reprodução desde o início do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="4eec2-118">Subsequently calling **IWMPControls.play** will start playback from the beginning of the media item.</span></span> <span data-ttu-id="4eec2-119">Para interromper uma operação de reprodução sem alterar a posição atual, use o método **IWMPControls. Pause** .</span><span class="sxs-lookup"><span data-stu-id="4eec2-119">To halt a play operation without changing the current position, use the **IWMPControls.pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="4eec2-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4eec2-120">Examples</span></span>

<span data-ttu-id="4eec2-121">O exemplo a seguir usa **Stop** para interromper o item de mídia atual em resposta ao evento Click de um botão.</span><span class="sxs-lookup"><span data-stu-id="4eec2-121">The following example uses **stop** to stop the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="4eec2-122">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="4eec2-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4eec2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eec2-123">Requirements</span></span>



| <span data-ttu-id="4eec2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eec2-124">Requirement</span></span> | <span data-ttu-id="4eec2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4eec2-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eec2-126">Versão</span><span class="sxs-lookup"><span data-stu-id="4eec2-126">Version</span></span><br/>   | <span data-ttu-id="4eec2-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4eec2-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4eec2-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4eec2-128">Namespace</span></span><br/> | <span data-ttu-id="4eec2-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4eec2-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4eec2-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="4eec2-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4eec2-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4eec2-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eec2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="4eec2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eec2-133">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4eec2-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4eec2-134">**IWMPControls. Next (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4eec2-134">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4eec2-135">**IWMPControls. PAUSE (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4eec2-135">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4eec2-136">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4eec2-136">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4eec2-137">**IWMPControls. Previous (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4eec2-137">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





