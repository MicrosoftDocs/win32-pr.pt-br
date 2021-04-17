---
title: Método IWMPPlaylistCollection newPlaylist
description: O método newPlaylist retorna uma interface IWMPPlaylist para uma lista de reprodução nova e vazia na biblioteca.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811699"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a><span data-ttu-id="dbcc0-106">Método IWMPPlaylistCollection:: newPlaylist</span><span class="sxs-lookup"><span data-stu-id="dbcc0-106">IWMPPlaylistCollection::newPlaylist method</span></span>

<span data-ttu-id="dbcc0-107">O método **newPlaylist** retorna uma interface **IWMPPlaylist** para uma lista de reprodução nova e vazia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-107">The **newPlaylist** method returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcc0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbcc0-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a><span data-ttu-id="dbcc0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbcc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbcc0-110">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbcc0-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbcc0-111">Um **System. String** que é o nome da nova lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-111">A **System.String** that is the name of the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbcc0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbcc0-112">Return value</span></span>

<span data-ttu-id="dbcc0-113">Uma interface **WMPLib. IWMPPlaylist** para a nova lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-113">A **WMPLib.IWMPPlaylist** interface for the new playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbcc0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbcc0-114">Remarks</span></span>

<span data-ttu-id="dbcc0-115">Esse método cria uma lista de reprodução vazia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="dbcc0-116">Para preencher a lista de reprodução com itens de mídia, use **IWMPPlaylist. appendItem** ou **IWMPPlaylist. insertItem**.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-116">To fill the playlist with media items, use **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="dbcc0-117">Várias listas de reprodução com o mesmo nome são permitidas na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="dbcc0-118">Para evitar a criação de um nome de playlist duplicado com esse método, use o método **getByName** e **IWMPPlaylistArray. Count** para descobrir se uma lista de reprodução com um nome específico já existe.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-118">To avoid creating a duplicate playlist name with this method, use the **getByName** method and **IWMPPlaylistArray.count** to discover whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="dbcc0-119">Espaços à esquerda e à direita não são permitidos em nomes de playlist e são removidos automaticamente do valor especificado para o parâmetro *bstrname* .</span><span class="sxs-lookup"><span data-stu-id="dbcc0-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *bstrName* parameter.</span></span>

<span data-ttu-id="dbcc0-120">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="dbcc0-121">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dbcc0-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dbcc0-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dbcc0-122">Examples</span></span>

<span data-ttu-id="dbcc0-123">O exemplo a seguir cria uma nova lista de reprodução vazia chamada "3list", adiciona-a à coleção de playlist e retorna uma interface a ela.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-123">The following example creates a new empty playlist called "ThreeList", adds it to the playlist collection, and returns an interface to it.</span></span> <span data-ttu-id="dbcc0-124">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a><span data-ttu-id="dbcc0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbcc0-125">Requirements</span></span>



| <span data-ttu-id="dbcc0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbcc0-126">Requirement</span></span> | <span data-ttu-id="dbcc0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="dbcc0-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbcc0-128">Versão</span><span class="sxs-lookup"><span data-stu-id="dbcc0-128">Version</span></span><br/>   | <span data-ttu-id="dbcc0-129">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dbcc0-129">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="dbcc0-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbcc0-130">Namespace</span></span><br/> | <span data-ttu-id="dbcc0-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dbcc0-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dbcc0-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="dbcc0-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dbcc0-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dbcc0-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbcc0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbcc0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbcc0-135">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbcc0-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbcc0-136">**IWMPPlaylist. appendItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbcc0-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbcc0-137">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbcc0-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbcc0-138">**IWMPPlaylistArray. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbcc0-138">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbcc0-139">**Interface IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbcc0-139">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbcc0-140">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbcc0-140">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





