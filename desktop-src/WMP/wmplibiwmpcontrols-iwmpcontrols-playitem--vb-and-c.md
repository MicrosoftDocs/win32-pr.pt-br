---
title: Método IWMPControls playItem
description: O método playItem reproduz o item de mídia especificado. | Método IWMPControls playItem
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- método playItem Windows Media Player
- método playItem Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, método playItem
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788017"
---
# <a name="iwmpcontrolsplayitem-method"></a><span data-ttu-id="f2fbe-107">IWMPControls: método layItem de:p</span><span class="sxs-lookup"><span data-stu-id="f2fbe-107">IWMPControls::playItem method</span></span>

<span data-ttu-id="f2fbe-108">O método **playItem** reproduz o item de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fbe-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2fbe-109">Syntax</span></span>


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a><span data-ttu-id="f2fbe-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2fbe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2fbe-111">*pIWMPMedia* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2fbe-111">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fbe-112">Uma interface **WMPLib. IWMPMedia** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-112">A **WMPLib.IWMPMedia** interface to the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2fbe-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2fbe-113">Return value</span></span>

<span data-ttu-id="f2fbe-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2fbe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2fbe-115">Remarks</span></span>

<span data-ttu-id="f2fbe-116">O item de mídia será carregado e executado automaticamente, independentemente do valor da propriedade **IWMPSettings. AutoStart** .</span><span class="sxs-lookup"><span data-stu-id="f2fbe-116">The media item will load and play automatically, regardless of the value of the **IWMPSettings.autoStart** property.</span></span> <span data-ttu-id="f2fbe-117">Para carregar um item sem reproduzi-lo automaticamente, defina **IWMPSettings. AutoStart** como **false** e atribua um valor a **AxWindowsMediaPlayer. URL**, após o qual **IWMPControls. Play** pode ser chamado para iniciar a reprodução do item.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-117">To load an item without playing it automatically, set **IWMPSettings.autoStart** to **false** and assign a value to **AxWindowsMediaPlayer.URL**, after which **IWMPControls.play** can be called to start playing the item.</span></span>

<span data-ttu-id="f2fbe-118">Observação</span><span class="sxs-lookup"><span data-stu-id="f2fbe-118">Note</span></span>

<span data-ttu-id="f2fbe-119">**playItem** funciona somente com itens em **AxWindowsMediaPlayer. currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-119">**playItem** works only with items in **AxWindowsMediaPlayer.currentPlaylist**.</span></span> <span data-ttu-id="f2fbe-120">Não há suporte para chamar **playItem** com uma referência a um item de mídia salvo.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f2fbe-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2fbe-121">Examples</span></span>

<span data-ttu-id="f2fbe-122">O exemplo a seguir usa **playItem** para reproduzir um item de mídia da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-122">The following example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="f2fbe-123">O item a ser tocado é escolhido com base na sua posição na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="f2fbe-124">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="f2fbe-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a><span data-ttu-id="f2fbe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2fbe-125">Requirements</span></span>



| <span data-ttu-id="f2fbe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2fbe-126">Requirement</span></span> | <span data-ttu-id="f2fbe-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f2fbe-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fbe-128">Versão</span><span class="sxs-lookup"><span data-stu-id="f2fbe-128">Version</span></span><br/>   | <span data-ttu-id="f2fbe-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f2fbe-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f2fbe-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2fbe-130">Namespace</span></span><br/> | <span data-ttu-id="f2fbe-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f2fbe-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f2fbe-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="f2fbe-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f2fbe-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f2fbe-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2fbe-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2fbe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fbe-135">**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fbe-135">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fbe-136">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fbe-136">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fbe-137">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fbe-137">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fbe-138">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fbe-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fbe-139">**IWMPPlaylist. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fbe-139">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2fbe-140">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f2fbe-140">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





