---
title: Método IWMPControls fastReverse
description: O método fastReverse inicia a reprodução rápida do item de mídia na direção inversa.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- método fastReverse Windows Media Player
- método fastReverse Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, método fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813020"
---
# <a name="iwmpcontrolsfastreverse-method"></a><span data-ttu-id="946fe-106">Método IWMPControls:: fastReverse</span><span class="sxs-lookup"><span data-stu-id="946fe-106">IWMPControls::fastReverse method</span></span>

<span data-ttu-id="946fe-107">O método **fastReverse** inicia a reprodução rápida do item de mídia na direção inversa.</span><span class="sxs-lookup"><span data-stu-id="946fe-107">The **fastReverse** method starts fast play of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="946fe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="946fe-108">Syntax</span></span>


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a><span data-ttu-id="946fe-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="946fe-109">Parameters</span></span>

<span data-ttu-id="946fe-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="946fe-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="946fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="946fe-111">Return value</span></span>

<span data-ttu-id="946fe-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="946fe-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="946fe-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="946fe-113">Remarks</span></span>

<span data-ttu-id="946fe-114">O método **fastReverse** examina o clipe de forma inversa em cinco vezes a velocidade normal, exibindo apenas os quadros-chave se for um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="946fe-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="946fe-115">Chamar **fastReverse** é equivalente a especificar-5,0 para a taxa, definindo a propriedade **IWMPSettings. Rate** .</span><span class="sxs-lookup"><span data-stu-id="946fe-115">Calling **fastReverse** is equivalent to specifying -5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="946fe-116">Se a taxa for alterada posteriormente, ou se **IWMPControls. Play** ou **IWMPControls. Stop** for chamado, o Windows Media Player será interrompido rapidamente.</span><span class="sxs-lookup"><span data-stu-id="946fe-116">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="946fe-117">Se o item fizer parte de uma lista de reprodução, o **fastReverse** para no início da faixa atual. Por exemplo, se Track 3 estiver em **fastReverse**, quando o início do Track 3 for atingido, o Windows Media Player não vai para o Track 2.</span><span class="sxs-lookup"><span data-stu-id="946fe-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="946fe-118">A contagem de execuções não é incrementada ao chamar **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="946fe-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="946fe-119">Se você chamar **IWMPControls. Fastforward** enquanto **fastReverse** estiver em execução, **fastReverse** será interrompido e **IWMPControls. Fastforward** será iniciado.</span><span class="sxs-lookup"><span data-stu-id="946fe-119">If you call **IWMPControls.fastForward** while **fastReverse** is running, **fastReverse** will be stopped and **IWMPControls.fastForward** will begin.</span></span>

<span data-ttu-id="946fe-120">Esse método não funciona para transmissões ao vivo e certos tipos de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="946fe-120">This method does not work for live broadcasts and certain digital media types.</span></span> <span data-ttu-id="946fe-121">Para determinar se você pode usar a inversão rápida em um clipe, passe o valor de **System. String** "fastReverse" para a propriedade **IWMPControls. IsAvailable** (o método **IWMPControls. get \_ IsAvailable** no C#).</span><span class="sxs-lookup"><span data-stu-id="946fe-121">To determine whether you can use fast reverse in a clip, pass the **System.String** value "FastReverse" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="946fe-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="946fe-122">Examples</span></span>

<span data-ttu-id="946fe-123">O exemplo a seguir usa **fastReverse** para reverter o item de mídia atual em resposta ao evento de clique de um botão.</span><span class="sxs-lookup"><span data-stu-id="946fe-123">The following example uses **fastReverse** to reverse the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="946fe-124">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="946fe-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="946fe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="946fe-125">Requirements</span></span>



| <span data-ttu-id="946fe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="946fe-126">Requirement</span></span> | <span data-ttu-id="946fe-127">Valor</span><span class="sxs-lookup"><span data-stu-id="946fe-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946fe-128">Versão</span><span class="sxs-lookup"><span data-stu-id="946fe-128">Version</span></span><br/>   | <span data-ttu-id="946fe-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="946fe-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="946fe-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="946fe-130">Namespace</span></span><br/> | <span data-ttu-id="946fe-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="946fe-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="946fe-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="946fe-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="946fe-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="946fe-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="946fe-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="946fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946fe-135">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="946fe-135">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="946fe-136">**IWMPControls. fastForward (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="946fe-136">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="946fe-137">**IWMPControls. IsAvailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="946fe-137">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="946fe-138">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="946fe-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="946fe-139">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="946fe-139">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="946fe-140">**IWMPSettings. Rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="946fe-140">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





