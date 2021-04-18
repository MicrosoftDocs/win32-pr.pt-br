---
title: Método play IWMPControls
description: O método play começa a reprodução do item de mídia atual ou retoma a reprodução de um item pausado.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- método play Windows Media Player
- método play Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, método play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789430"
---
# <a name="iwmpcontrolsplay-method"></a><span data-ttu-id="fc90b-106">IWMPControls::p método deite</span><span class="sxs-lookup"><span data-stu-id="fc90b-106">IWMPControls::play method</span></span>

<span data-ttu-id="fc90b-107">O método **Play** começa a reprodução do item de mídia atual ou retoma a reprodução de um item pausado.</span><span class="sxs-lookup"><span data-stu-id="fc90b-107">The **play** method begins playback of the current media item, or resumes playback of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc90b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc90b-108">Syntax</span></span>


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a><span data-ttu-id="fc90b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc90b-109">Parameters</span></span>

<span data-ttu-id="fc90b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fc90b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc90b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc90b-111">Return value</span></span>

<span data-ttu-id="fc90b-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fc90b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc90b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc90b-113">Remarks</span></span>

<span data-ttu-id="fc90b-114">Se esse método for chamado durante o encaminhamento rápido ou o retrocesso, a taxa de reprodução (o valor de **IWMPSettings. Rate**) será definida como 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc90b-114">If this method is called while fast-forwarding or rewinding, the rate of playback (the value of **IWMPSettings.rate**) is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="fc90b-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc90b-115">Examples</span></span>

<span data-ttu-id="fc90b-116">O exemplo a seguir usa **Play** para reproduzir o item de mídia atual em resposta ao evento Click de um botão.</span><span class="sxs-lookup"><span data-stu-id="fc90b-116">The following example uses **play** to play the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="fc90b-117">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="fc90b-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="fc90b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc90b-118">Requirements</span></span>



| <span data-ttu-id="fc90b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc90b-119">Requirement</span></span> | <span data-ttu-id="fc90b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fc90b-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc90b-121">Versão</span><span class="sxs-lookup"><span data-stu-id="fc90b-121">Version</span></span><br/>   | <span data-ttu-id="fc90b-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="fc90b-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fc90b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc90b-123">Namespace</span></span><br/> | <span data-ttu-id="fc90b-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fc90b-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fc90b-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="fc90b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fc90b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fc90b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc90b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc90b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc90b-128">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fc90b-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fc90b-129">**IWMPControls. playItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fc90b-129">**IWMPControls.playItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fc90b-130">**IWMPSettings. Rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fc90b-130">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





