---
title: Método IWMPControls fastForward
description: O método fastForward inicia a reprodução rápida do item de mídia na direção de encaminhamento. | Método IWMPControls fastForward
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- método fastForward Windows Media Player
- método fastForward Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, método fastForward
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789431"
---
# <a name="iwmpcontrolsfastforward-method"></a><span data-ttu-id="91daa-107">Método IWMPControls:: fastForward</span><span class="sxs-lookup"><span data-stu-id="91daa-107">IWMPControls::fastForward method</span></span>

<span data-ttu-id="91daa-108">O método **Fastforward** inicia a reprodução rápida do item de mídia na direção de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="91daa-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="91daa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91daa-109">Syntax</span></span>


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a><span data-ttu-id="91daa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91daa-110">Parameters</span></span>

<span data-ttu-id="91daa-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="91daa-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91daa-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91daa-112">Return value</span></span>

<span data-ttu-id="91daa-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="91daa-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91daa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="91daa-114">Remarks</span></span>

<span data-ttu-id="91daa-115">O método **Fastforward** reproduz o clipe em cinco vezes a velocidade normal.</span><span class="sxs-lookup"><span data-stu-id="91daa-115">The **fastForward** method plays the clip at five times the normal speed.</span></span> <span data-ttu-id="91daa-116">Chamar **Fastforward** é equivalente a especificar 5,0 para a taxa, definindo a propriedade **IWMPSettings. Rate** .</span><span class="sxs-lookup"><span data-stu-id="91daa-116">Calling **fastForward** is equivalent to specifying 5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="91daa-117">Se a taxa for alterada posteriormente, ou se **IWMPControls. Play** ou **IWMPControls. Stop** for chamado, o Windows Media Player cessará o encaminhamento rápido.</span><span class="sxs-lookup"><span data-stu-id="91daa-117">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="91daa-118">O método **Fastforward** não funciona para transmissões ao vivo e certos tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="91daa-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="91daa-119">Para determinar se você pode avançar rapidamente em um clipe, passe o valor de **System. String** "Fastforward" para a propriedade **IWMPControls. IsAvailable** (o método **IWMPControls. get \_ IsAvailable** em C#).</span><span class="sxs-lookup"><span data-stu-id="91daa-119">To determine whether you can fast forward in a clip, pass the **System.String** value "FastForward" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="91daa-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91daa-120">Examples</span></span>

<span data-ttu-id="91daa-121">O exemplo a seguir usa **Fastforward** para avançar rapidamente o item de mídia atual em resposta ao evento de clique de um botão.</span><span class="sxs-lookup"><span data-stu-id="91daa-121">The following example uses **fastForward** to fast-forward the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="91daa-122">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="91daa-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="91daa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91daa-123">Requirements</span></span>



| <span data-ttu-id="91daa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="91daa-124">Requirement</span></span> | <span data-ttu-id="91daa-125">Valor</span><span class="sxs-lookup"><span data-stu-id="91daa-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91daa-126">Versão</span><span class="sxs-lookup"><span data-stu-id="91daa-126">Version</span></span><br/>   | <span data-ttu-id="91daa-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="91daa-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="91daa-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="91daa-128">Namespace</span></span><br/> | <span data-ttu-id="91daa-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="91daa-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="91daa-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="91daa-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="91daa-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="91daa-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91daa-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="91daa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91daa-133">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="91daa-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91daa-134">**IWMPControls. IsAvailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="91daa-134">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91daa-135">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="91daa-135">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91daa-136">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="91daa-136">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91daa-137">**IWMPSettings. Rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="91daa-137">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





