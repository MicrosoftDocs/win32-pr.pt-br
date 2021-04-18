---
title: Propriedade AxWindowsMediaPlayer. PlayState
description: A propriedade PlayState Obtém um valor de enumeração que indica o estado da operação do Windows Media Player.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Propriedade PlayState do Windows Media Player
- Propriedade PlayState Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade PlayState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760466"
---
# <a name="axwindowsmediaplayerplaystate-property"></a><span data-ttu-id="45095-106">Propriedade AxWindowsMediaPlayer. PlayState</span><span class="sxs-lookup"><span data-stu-id="45095-106">AxWindowsMediaPlayer.playState property</span></span>

<span data-ttu-id="45095-107">A propriedade PlayState Obtém um valor de enumeração que indica o estado da operação do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="45095-107">The playState property gets an enumeration value indicating the state of the Windows Media Player operation.</span></span>

<span data-ttu-id="45095-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="45095-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45095-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45095-109">Syntax</span></span>


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a><span data-ttu-id="45095-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="45095-110">Property value</span></span>

<span data-ttu-id="45095-111">O valor de enumeração WMPLib. WMPPlayState.</span><span class="sxs-lookup"><span data-stu-id="45095-111">The WMPLib.WMPPlayState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45095-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="45095-112">Remarks</span></span>

<span data-ttu-id="45095-113">Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="45095-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="45095-114">Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="45095-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="45095-115">Você não deve escrever código que dependa da ordem de estado.</span><span class="sxs-lookup"><span data-stu-id="45095-115">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="45095-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45095-116">Examples</span></span>

<span data-ttu-id="45095-117">O exemplo a seguir usa a propriedade PlayState para exibir o status de execução atual do Player em um rótulo.</span><span class="sxs-lookup"><span data-stu-id="45095-117">The following example uses the playState property to display the current playing status of the player in a label.</span></span> <span data-ttu-id="45095-118">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="45095-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a><span data-ttu-id="45095-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45095-119">Requirements</span></span>



| <span data-ttu-id="45095-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45095-120">Requirement</span></span> | <span data-ttu-id="45095-121">Valor</span><span class="sxs-lookup"><span data-stu-id="45095-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45095-122">Versão</span><span class="sxs-lookup"><span data-stu-id="45095-122">Version</span></span><br/>   | <span data-ttu-id="45095-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="45095-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="45095-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="45095-124">Namespace</span></span><br/> | <span data-ttu-id="45095-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="45095-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="45095-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="45095-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="45095-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="45095-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45095-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="45095-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45095-129">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="45095-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="45095-130">**Evento AxWindowsMediaPlayer. PlayStateChange (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="45095-130">**AxWindowsMediaPlayer.PlayStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="45095-131">**WMPPlayState**</span><span class="sxs-lookup"><span data-stu-id="45095-131">**WMPPlayState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





