---
title: Método Pause IWMPControls
description: O método pause pausa a reprodução do item de mídia. | Método Pause IWMPControls
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- Método Pause Windows Media Player
- Método Pause Windows Media Player, interface IWMPControls
- Interface IWMPControls do Windows Media Player, método pause
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761318"
---
# <a name="iwmpcontrolspause-method"></a><span data-ttu-id="947f5-107">IWMPControls: método ause de:p</span><span class="sxs-lookup"><span data-stu-id="947f5-107">IWMPControls::pause method</span></span>

<span data-ttu-id="947f5-108">O método **Pause** pausa a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="947f5-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="947f5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="947f5-109">Syntax</span></span>


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a><span data-ttu-id="947f5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="947f5-110">Parameters</span></span>

<span data-ttu-id="947f5-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="947f5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="947f5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="947f5-112">Return value</span></span>

<span data-ttu-id="947f5-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="947f5-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="947f5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="947f5-114">Remarks</span></span>

<span data-ttu-id="947f5-115">Quando um arquivo é pausado, o Windows Media Player não fornece nenhum recurso do sistema, como o dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="947f5-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="947f5-116">Para determinar se um determinado tipo de mídia pode ser pausado, passe o valor de **System. String** "Pause" para a propriedade **IWMPControls. IsAvailable** (o método **IWMPControls. get \_ IsAvailable** em C#).</span><span class="sxs-lookup"><span data-stu-id="947f5-116">To determine whether a particular media type can be paused, pass the **System.String** value "pause" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="947f5-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="947f5-117">Examples</span></span>

<span data-ttu-id="947f5-118">O exemplo a seguir usa **Pause** para pausar a reprodução do item de mídia atual em resposta ao evento de clique de um botão.</span><span class="sxs-lookup"><span data-stu-id="947f5-118">The following example uses **pause** to pause playback of the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="947f5-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="947f5-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="947f5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="947f5-120">Requirements</span></span>



| <span data-ttu-id="947f5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="947f5-121">Requirement</span></span> | <span data-ttu-id="947f5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="947f5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="947f5-123">Versão</span><span class="sxs-lookup"><span data-stu-id="947f5-123">Version</span></span><br/>   | <span data-ttu-id="947f5-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="947f5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="947f5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="947f5-125">Namespace</span></span><br/> | <span data-ttu-id="947f5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="947f5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="947f5-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="947f5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="947f5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="947f5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="947f5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="947f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="947f5-130">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="947f5-130">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="947f5-131">**IWMPControls. IsAvailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="947f5-131">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





