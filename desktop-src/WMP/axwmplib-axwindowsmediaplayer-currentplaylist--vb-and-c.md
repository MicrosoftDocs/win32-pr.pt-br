---
title: Propriedade AxWindowsMediaPlayer. currentPlaylist
description: A propriedade currentPlaylist Obtém ou define a interface IWMPPlaylist atual que fornece uma maneira fácil de organizar e manipular itens de mídia em uma lista.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Propriedade currentPlaylist Windows Media Player
- Propriedade currentPlaylist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783633"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a><span data-ttu-id="a4387-106">Propriedade AxWindowsMediaPlayer. currentPlaylist</span><span class="sxs-lookup"><span data-stu-id="a4387-106">AxWindowsMediaPlayer.currentPlaylist property</span></span>

<span data-ttu-id="a4387-107">A propriedade currentPlaylist Obtém ou define a interface **IWMPPlaylist** atual que fornece uma maneira fácil de organizar e manipular itens de mídia em uma lista.</span><span class="sxs-lookup"><span data-stu-id="a4387-107">The currentPlaylist property gets or sets the current **IWMPPlaylist** interface that provides an easy way to organize and manipulate media items in a list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4387-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4387-108">Syntax</span></span>


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="a4387-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a4387-109">Property value</span></span>

<span data-ttu-id="a4387-110">A interface WMPLib. IWMPPlaylist que fornece acesso à playlist atual.</span><span class="sxs-lookup"><span data-stu-id="a4387-110">The WMPLib.IWMPPlaylist interface that provides access to the current playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4387-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4387-111">Remarks</span></span>

<span data-ttu-id="a4387-112">Se a propriedade IWMPSettings. AutoStart (também acessada via AxWindowsMediaPlayer. Settings.**AutoStart**) é true, a reprodução é iniciada automaticamente sempre que você definir **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="a4387-112">If the IWMPSettings.autoStart property (also accessed via AxWindowsMediaPlayer.settings.**autoStart**) is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="a4387-113">Essa propriedade usa uma interface IWMPPlaylist, que pode ser adquirida de várias maneiras, como ao obter o valor do *IWMPPlaylistArray*. **Item** ou *IWMPPlaylistCollection*. Propriedades **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="a4387-113">This property takes an IWMPPlaylist interface, which can be acquired in several ways, such as by getting the value from the *IWMPPlaylistArray*.**Item** or *IWMPPlaylistCollection*.**newPlaylist** properties.</span></span> <span data-ttu-id="a4387-114">Para carregar um item da **playlist** usando um nome de arquivo, defina a propriedade URL ou use AxWindowsMediaPlayer. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="a4387-114">To load a **playlist** item using a file name, set the URL property or use AxWindowsMediaPlayer.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="a4387-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4387-115">Examples</span></span>

<span data-ttu-id="a4387-116">O exemplo a seguir recupera a primeira lista de reprodução na biblioteca e usa a propriedade currentPlaylist para definir a lista de reprodução recuperada como a playlist atual e exibir seu nome.</span><span class="sxs-lookup"><span data-stu-id="a4387-116">The following example retrieves the first playlist in the library and uses the currentPlaylist property to set the retrieved playlist as the current playlist, and display its name.</span></span> <span data-ttu-id="a4387-117">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="a4387-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a><span data-ttu-id="a4387-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4387-118">Requirements</span></span>



| <span data-ttu-id="a4387-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4387-119">Requirement</span></span> | <span data-ttu-id="a4387-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a4387-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4387-121">Versão</span><span class="sxs-lookup"><span data-stu-id="a4387-121">Version</span></span><br/>   | <span data-ttu-id="a4387-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a4387-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a4387-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4387-123">Namespace</span></span><br/> | <span data-ttu-id="a4387-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a4387-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a4387-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="a4387-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a4387-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a4387-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4387-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4387-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4387-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4387-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4387-129">**AxWindowsMediaPlayer. newPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4387-129">**AxWindowsMediaPlayer.newPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="a4387-130">**AxWindowsMediaPlayer. Settings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4387-130">**AxWindowsMediaPlayer.settings (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4387-131">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4387-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4387-132">**IWMPPlaylistArray. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4387-132">**IWMPPlaylistArray.Item (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4387-133">**IWMPPlaylistCollection. newPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4387-133">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4387-134">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4387-134">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





