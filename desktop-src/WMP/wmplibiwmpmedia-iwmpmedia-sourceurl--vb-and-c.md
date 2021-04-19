---
title: Propriedade IWMPMedia sourceURL
description: A propriedade sourceURL Obtém a URL do item de mídia.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- Propriedade sourceURL Windows Media Player
- Propriedade sourceURL Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade sourceURL
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754584"
---
# <a name="iwmpmediasourceurl-property"></a><span data-ttu-id="c0590-106">Propriedade IWMPMedia:: sourceURL</span><span class="sxs-lookup"><span data-stu-id="c0590-106">IWMPMedia::sourceURL property</span></span>

<span data-ttu-id="c0590-107">A propriedade **sourceURL** Obtém a URL do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="c0590-107">The **sourceURL** property gets the URL of the media item.</span></span>

<span data-ttu-id="c0590-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c0590-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0590-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0590-109">Syntax</span></span>


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="c0590-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c0590-110">Property value</span></span>

<span data-ttu-id="c0590-111">Um **System. String** que é a URL de origem.</span><span class="sxs-lookup"><span data-stu-id="c0590-111">A **System.String** that is the source URL.</span></span>

## <a name="examples"></a><span data-ttu-id="c0590-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0590-112">Examples</span></span>

<span data-ttu-id="c0590-113">O exemplo a seguir usa **sourceURL** para recuperar a URL do primeiro item de mídia na lista de reprodução "todas as músicas"; a URL do item de mídia é atribuída à propriedade URL do objeto Player.</span><span class="sxs-lookup"><span data-stu-id="c0590-113">The following example uses **sourceURL** to retrieve the URL of the first media item in the "All Music" playlist; the URL of the media item is then assigned to the player object URL property.</span></span> <span data-ttu-id="c0590-114">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="c0590-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="c0590-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0590-115">Requirements</span></span>



| <span data-ttu-id="c0590-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0590-116">Requirement</span></span> | <span data-ttu-id="c0590-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c0590-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0590-118">Versão</span><span class="sxs-lookup"><span data-stu-id="c0590-118">Version</span></span><br/>   | <span data-ttu-id="c0590-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c0590-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c0590-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0590-120">Namespace</span></span><br/> | <span data-ttu-id="c0590-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c0590-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c0590-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="c0590-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c0590-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c0590-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0590-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0590-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0590-125">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c0590-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





