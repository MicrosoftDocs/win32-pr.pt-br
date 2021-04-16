---
title: Método IWMPPlaylist appendItem
description: O método appendItem adiciona um item de mídia ao final de uma lista de reprodução.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- método appendItem Windows Media Player
- método appendItem Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método appendItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765277"
---
# <a name="iwmpplaylistappenditem-method"></a><span data-ttu-id="a1507-106">Método IWMPPlaylist:: appendItem</span><span class="sxs-lookup"><span data-stu-id="a1507-106">IWMPPlaylist::appendItem method</span></span>

<span data-ttu-id="a1507-107">O método **appendItem** adiciona um item de mídia ao final de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a1507-107">The **appendItem** method adds a media item to the end of a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1507-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1507-108">Syntax</span></span>


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a><span data-ttu-id="a1507-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1507-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1507-110">*pIWMPMedia* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a1507-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1507-111">Uma interface **WMPLib. IWMPMedia** que representa o item de mídia a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="a1507-111">An **WMPLib.IWMPMedia** interface that represents the media item to be appended.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1507-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1507-112">Return value</span></span>

<span data-ttu-id="a1507-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a1507-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1507-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1507-114">Remarks</span></span>

<span data-ttu-id="a1507-115">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a1507-115">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="a1507-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a1507-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a1507-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1507-117">Examples</span></span>

<span data-ttu-id="a1507-118">O exemplo a seguir usa **appendItem** para adicionar o item de mídia atual à lista de reprodução denominada "trêslist".</span><span class="sxs-lookup"><span data-stu-id="a1507-118">The following example uses **appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="a1507-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="a1507-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a><span data-ttu-id="a1507-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1507-120">Requirements</span></span>



| <span data-ttu-id="a1507-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1507-121">Requirement</span></span> | <span data-ttu-id="a1507-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a1507-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1507-123">Versão</span><span class="sxs-lookup"><span data-stu-id="a1507-123">Version</span></span><br/>   | <span data-ttu-id="a1507-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a1507-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a1507-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1507-125">Namespace</span></span><br/> | <span data-ttu-id="a1507-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a1507-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a1507-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="a1507-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a1507-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a1507-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1507-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1507-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1507-130">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a1507-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a1507-131">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a1507-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





