---
title: Propriedade de taxa de IWMPSettings
description: A propriedade Rate Obtém ou define a taxa de reprodução atual para vídeo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Propriedade de taxa Windows Media Player
- Propriedade de taxa Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade Rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785219"
---
# <a name="iwmpsettingsrate-property"></a><span data-ttu-id="578ad-106">Propriedade IWMPSettings:: Rate</span><span class="sxs-lookup"><span data-stu-id="578ad-106">IWMPSettings::rate property</span></span>

<span data-ttu-id="578ad-107">A propriedade **Rate** Obtém ou define a taxa de reprodução atual para vídeo.</span><span class="sxs-lookup"><span data-stu-id="578ad-107">The **rate** property gets or sets the current playback rate for video.</span></span>

## <a name="syntax"></a><span data-ttu-id="578ad-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="578ad-108">Syntax</span></span>


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a><span data-ttu-id="578ad-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="578ad-109">Property value</span></span>

<span data-ttu-id="578ad-110">Um **sistema. Double** que é a taxa de reprodução, com um valor padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="578ad-110">A **System.Double** that is the playback rate, with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="578ad-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="578ad-111">Remarks</span></span>

<span data-ttu-id="578ad-112">O valor recuperado por essa propriedade atua como um valor de multiplicador que permite reproduzir um item de mídia em uma taxa mais rápida ou mais lenta.</span><span class="sxs-lookup"><span data-stu-id="578ad-112">The value retrieved by this property acts as a multiplier value that enables you to play a media item at a faster or slower rate.</span></span> <span data-ttu-id="578ad-113">O valor padrão de 1,0 indica a velocidade de criação.</span><span class="sxs-lookup"><span data-stu-id="578ad-113">The default value of 1.0 indicates the authored speed.</span></span>

<span data-ttu-id="578ad-114">Observe que uma faixa de áudio torna-se difícil de entender em taxas menores que 0,5 ou superiores a 1,5.</span><span class="sxs-lookup"><span data-stu-id="578ad-114">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="578ad-115">Uma taxa de reprodução de 2 indica duas vezes a velocidade de reprodução normal.</span><span class="sxs-lookup"><span data-stu-id="578ad-115">A playback rate of 2 indicates twice the normal playback speed.</span></span>

<span data-ttu-id="578ad-116">O Windows Media Player tentará usar o mais efetivo dos quatro modos de reprodução diferentes a seguir</span><span class="sxs-lookup"><span data-stu-id="578ad-116">Windows Media Player will attempt to use the most effective of the following four different playback modes</span></span>

-   <span data-ttu-id="578ad-117">Reprodução de vídeo suave com densidade de áudio mantida</span><span class="sxs-lookup"><span data-stu-id="578ad-117">Smooth video playback with audio pitch maintained</span></span>
-   <span data-ttu-id="578ad-118">Reprodução de vídeo suave com densidade de áudio não mantida</span><span class="sxs-lookup"><span data-stu-id="578ad-118">Smooth video playback with audio pitch not maintained</span></span>
-   <span data-ttu-id="578ad-119">Uma reprodução de vídeo suave sem áudio</span><span class="sxs-lookup"><span data-stu-id="578ad-119">Smooth video playback with no audio</span></span>
-   <span data-ttu-id="578ad-120">Reprodução de vídeo com quadro-chave sem áudio</span><span class="sxs-lookup"><span data-stu-id="578ad-120">Keyframe video playback with no audio</span></span>

<span data-ttu-id="578ad-121">O modo escolhido pelo Windows Media Player depende de vários fatores, incluindo tipo de arquivo e local, sistema operacional, rede e servidor.</span><span class="sxs-lookup"><span data-stu-id="578ad-121">The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="578ad-122">Outras considerações também se aplicam, dependendo do formato de mídia digital usado para criar o conteúdo:</span><span class="sxs-lookup"><span data-stu-id="578ad-122">Other considerations apply as well, depending on the digital media format used to create the content:</span></span>

-   <span data-ttu-id="578ad-123">**Windows Media Video (WMV) e ASF.**</span><span class="sxs-lookup"><span data-stu-id="578ad-123">**Windows Media Video (WMV) and ASF.**</span></span> <span data-ttu-id="578ad-124">Os valores ideais para a propriedade **Rate** são de 1 a 10, ou de 1 a 10 para a reprodução reversa.</span><span class="sxs-lookup"><span data-stu-id="578ad-124">Optimal values for the **rate** property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="578ad-125">Os valores de 0,5 a 1,0 ou de-0,5 a-1,0 também podem funcionar bem em casos em que a densidade de áudio pode ser mantida, como ao reproduzir arquivos localizados no computador local.</span><span class="sxs-lookup"><span data-stu-id="578ad-125">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer.</span></span> <span data-ttu-id="578ad-126">Valores com uma magnitude absoluta maior que 10 são permitidos, mas não são muito significativos.</span><span class="sxs-lookup"><span data-stu-id="578ad-126">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="578ad-127">**Outros formatos de vídeo.**</span><span class="sxs-lookup"><span data-stu-id="578ad-127">**Other video formats.**</span></span> <span data-ttu-id="578ad-128">A propriedade **Rate** pode variar de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="578ad-128">The **rate** property can range from 0 to 9.</span></span> <span data-ttu-id="578ad-129">Valores negativos não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="578ad-129">Negative values are not allowed.</span></span> <span data-ttu-id="578ad-130">Valores menores que 1 representam movimento lento.</span><span class="sxs-lookup"><span data-stu-id="578ad-130">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="578ad-131">Os valores acima de 9 são permitidos, mas não são muito significativos.</span><span class="sxs-lookup"><span data-stu-id="578ad-131">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="578ad-132">O método **IWMPControls. Fastforward** altera o valor de **Rate** para 5,0, enquanto o método **IWMPControls. fastReverse** altera o valor de **Rate** para 5,0.</span><span class="sxs-lookup"><span data-stu-id="578ad-132">The **IWMPControls.fastForward** method changes the value of **rate** to 5.0, while the **IWMPControls.fastReverse** method changes the value of **rate** to  5.0.</span></span>

<span data-ttu-id="578ad-133">A taxa de reprodução de alguns formatos de mídia digital não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="578ad-133">The playback rate of some digital media formats cannot be altered.</span></span> <span data-ttu-id="578ad-134">Use a propriedade **IWMPSettings. IsAvailable** (em C#, o método **IWMPSettings. get \_ IsAvailable** ) para descobrir se essa propriedade pode ser especificada para um item de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="578ad-134">Use the **IWMPSettings.isAvailable** property (In C# the **IWMPSettings.get\_isAvailable** method) to discover whether this property can be specified for a particular media item.</span></span>

## <a name="examples"></a><span data-ttu-id="578ad-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="578ad-135">Examples</span></span>

<span data-ttu-id="578ad-136">O exemplo a seguir usa um controle intermediário numérico que permite ao usuário alterar a velocidade de reprodução da mídia atual.</span><span class="sxs-lookup"><span data-stu-id="578ad-136">The following example uses a numeric updown control that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="578ad-137">Quando o usuário clica nas setas para cima ou para baixo do controle, a propriedade **taxa** é definida com o novo valor.</span><span class="sxs-lookup"><span data-stu-id="578ad-137">When the user clicks the up or down arrows of the control, the **rate** property is set to the new value.</span></span> <span data-ttu-id="578ad-138">O intervalo de valores possível no controle é de 0,5 (meia velocidade) a 2,0 (velocidade dupla).</span><span class="sxs-lookup"><span data-stu-id="578ad-138">The possible range of values in the control are 0.5 (half-speed) to 2.0 (double-speed).</span></span> <span data-ttu-id="578ad-139">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="578ad-139">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="578ad-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="578ad-140">Requirements</span></span>



| <span data-ttu-id="578ad-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="578ad-141">Requirement</span></span> | <span data-ttu-id="578ad-142">Valor</span><span class="sxs-lookup"><span data-stu-id="578ad-142">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="578ad-143">Versão</span><span class="sxs-lookup"><span data-stu-id="578ad-143">Version</span></span><br/>   | <span data-ttu-id="578ad-144">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="578ad-144">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="578ad-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="578ad-145">Namespace</span></span><br/> | <span data-ttu-id="578ad-146">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="578ad-146">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="578ad-147">Assembly</span><span class="sxs-lookup"><span data-stu-id="578ad-147">Assembly</span></span><br/>  | <dl> <span data-ttu-id="578ad-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="578ad-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="578ad-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="578ad-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578ad-150">**IWMPControls. fastForward (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="578ad-150">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="578ad-151">**IWMPControls. fastReverse (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="578ad-151">**IWMPControls.fastReverse (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="578ad-152">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="578ad-152">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="578ad-153">**IWMPSettings. IsAvailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="578ad-153">**IWMPSettings.isAvailable (VB and C#)**</span></span>](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="578ad-154">**IWMPSettings. mudo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="578ad-154">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





