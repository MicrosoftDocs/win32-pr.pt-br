---
title: Método IWMPMedia isMemberOf
description: O método isMemberOf retorna um valor que indica se o item de mídia especificado é um membro da playlist especificada.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- método isMemberOf Windows Media Player
- método isMemberOf Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764602"
---
# <a name="iwmpmediaismemberof-method"></a><span data-ttu-id="e8b4a-106">Método IWMPMedia:: isMemberOf</span><span class="sxs-lookup"><span data-stu-id="e8b4a-106">IWMPMedia::isMemberOf method</span></span>

<span data-ttu-id="e8b4a-107">O método **isMemberOf** retorna um valor que indica se o item de mídia especificado é um membro da playlist especificada.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-107">The **isMemberOf** method returns a value indicating whether the specified media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b4a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8b4a-108">Syntax</span></span>


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a><span data-ttu-id="e8b4a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8b4a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8b4a-110">*pPlaylist* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8b4a-110">*pPlaylist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b4a-111">Uma interface **WMPLib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="e8b4a-111">A **WMPLib.IWMPPlaylist** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8b4a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8b4a-112">Return value</span></span>

<span data-ttu-id="e8b4a-113">Um valor **System. Boolean** que indica se o item de mídia é um membro da playlist.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-113">A **System.Boolean** value that indicates whether the media item is a member of the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b4a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8b4a-114">Remarks</span></span>

<span data-ttu-id="e8b4a-115">Esse método não pode verificar as listas de reprodução recuperadas por meio da interface **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="e8b4a-115">This method cannot check playlists retrieved through the **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="e8b4a-116">Para testar se um item de mídia é membro de uma lista de reprodução nomeada específica, recupere a coleção de playlist com a propriedade **AxWindowsMediaPlayer. playlistcollection** .</span><span class="sxs-lookup"><span data-stu-id="e8b4a-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the **AxWindowsMediaPlayer.playlistCollection** property.</span></span> <span data-ttu-id="e8b4a-117">Depois de recuperar a coleção, recupere a lista de reprodução individual chamando o método **IWMPPlaylistCollection. getByName** .</span><span class="sxs-lookup"><span data-stu-id="e8b4a-117">Once you retrieve the collection, retrieve the individual playlist by calling the **IWMPPlaylistCollection.getByName** method.</span></span>

<span data-ttu-id="e8b4a-118">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-118">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e8b4a-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e8b4a-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e8b4a-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e8b4a-120">Examples</span></span>

<span data-ttu-id="e8b4a-121">O exemplo a seguir usa **isMemberOf** para testar se o item de mídia atual é um membro da lista de reprodução chamado todas as músicas.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-121">The following example uses **isMemberOf** to test whether the current media item is a member of the playlist named All Music.</span></span> <span data-ttu-id="e8b4a-122">Se não for, o item de mídia atual será anexado à lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-122">If it is not, the current media item is appended to the playlist.</span></span> <span data-ttu-id="e8b4a-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a><span data-ttu-id="e8b4a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8b4a-124">Requirements</span></span>



| <span data-ttu-id="e8b4a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8b4a-125">Requirement</span></span> | <span data-ttu-id="e8b4a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e8b4a-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b4a-127">Versão</span><span class="sxs-lookup"><span data-stu-id="e8b4a-127">Version</span></span><br/>   | <span data-ttu-id="e8b4a-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="e8b4a-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e8b4a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8b4a-129">Namespace</span></span><br/> | <span data-ttu-id="e8b4a-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e8b4a-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e8b4a-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="e8b4a-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e8b4a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e8b4a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8b4a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8b4a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b4a-134">**AxWindowsMediaPlayer. playlistcollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8b4a-134">**AxWindowsMediaPlayer.playlistCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8b4a-135">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8b4a-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8b4a-136">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8b4a-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e8b4a-137">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e8b4a-137">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





