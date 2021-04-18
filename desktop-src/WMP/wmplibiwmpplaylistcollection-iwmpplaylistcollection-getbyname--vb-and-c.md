---
title: Método IWMPPlaylistCollection getByName
description: O método getByName retorna uma interface IWMPPlaylistArray que fornece acesso a listas de reprodução com o nome especificado, se existir.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- método getByName Windows Media Player
- método getByName Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771619"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a><span data-ttu-id="1fed1-106">Método IWMPPlaylistCollection:: getByName</span><span class="sxs-lookup"><span data-stu-id="1fed1-106">IWMPPlaylistCollection::getByName method</span></span>

<span data-ttu-id="1fed1-107">O método **getByName** retorna uma interface **IWMPPlaylistArray** que fornece acesso a listas de reprodução com o nome especificado, se existir.</span><span class="sxs-lookup"><span data-stu-id="1fed1-107">The **getByName** method returns a **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fed1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fed1-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="1fed1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fed1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fed1-110">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fed1-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fed1-111">Um **System. String** que é o nome da playlist.</span><span class="sxs-lookup"><span data-stu-id="1fed1-111">A **System.String** that is the name of the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fed1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fed1-112">Return value</span></span>

<span data-ttu-id="1fed1-113">Uma interface **WMPLib. IWMPPlaylistArray** para a matriz de listas de reprodução recuperada.</span><span class="sxs-lookup"><span data-stu-id="1fed1-113">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fed1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fed1-114">Remarks</span></span>

<span data-ttu-id="1fed1-115">Use **IWMPPlaylistArray. Count** para determinar se existe uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1fed1-115">Use **IWMPPlaylistArray.count** to determine whether a playlist exists.</span></span> <span data-ttu-id="1fed1-116">Se **Count** for zero, a matriz estará vazia.</span><span class="sxs-lookup"><span data-stu-id="1fed1-116">If **count** is zero, the array is empty.</span></span>

<span data-ttu-id="1fed1-117">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1fed1-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="1fed1-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1fed1-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1fed1-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1fed1-119">Examples</span></span>

<span data-ttu-id="1fed1-120">O exemplo a seguir usa **getByName** para verificar a coleção de playlist de uma lista de reprodução chamada "favoritos--4 e 5 estrelas classificados".</span><span class="sxs-lookup"><span data-stu-id="1fed1-120">The following example uses **getByName** to check the playlist collection for a playlist named "Favorites -- 4 and 5 star rated".</span></span> <span data-ttu-id="1fed1-121">Se existir uma lista de reprodução com esse nome, **getByName** a definirá como a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="1fed1-121">If a playlist by that name exists, **getByName** sets it as the current playlist.</span></span> <span data-ttu-id="1fed1-122">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="1fed1-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a><span data-ttu-id="1fed1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fed1-123">Requirements</span></span>



| <span data-ttu-id="1fed1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fed1-124">Requirement</span></span> | <span data-ttu-id="1fed1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1fed1-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fed1-126">Versão</span><span class="sxs-lookup"><span data-stu-id="1fed1-126">Version</span></span><br/>   | <span data-ttu-id="1fed1-127">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1fed1-127">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="1fed1-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fed1-128">Namespace</span></span><br/> | <span data-ttu-id="1fed1-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1fed1-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1fed1-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="1fed1-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1fed1-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1fed1-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fed1-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fed1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fed1-133">**Interface IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1fed1-133">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1fed1-134">**IWMPPlaylistArray. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1fed1-134">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1fed1-135">**Interface IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1fed1-135">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





