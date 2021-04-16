---
title: Propriedade de playlist IWMPCdrom
description: A propriedade playlist Obtém uma interface IWMPPlaylist que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz de um DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Propriedade playlist Windows Media Player
- Propriedade playlist Windows Media Player, interface IWMPCdrom
- Interface IWMPCdrom Windows Media Player, Propriedade playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765032"
---
# <a name="iwmpcdromplaylist-property"></a><span data-ttu-id="4699d-106">IWMPCdrom: Propriedade laylist de:P</span><span class="sxs-lookup"><span data-stu-id="4699d-106">IWMPCdrom::Playlist property</span></span>

<span data-ttu-id="4699d-107">A propriedade **playlist** Obtém uma interface **IWMPPlaylist** que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz de um DVD.</span><span class="sxs-lookup"><span data-stu-id="4699d-107">The **Playlist** property gets an **IWMPPlaylist** interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="4699d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4699d-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="4699d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4699d-109">Property value</span></span>

<span data-ttu-id="4699d-110">Uma interface **WMPLib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="4699d-110">A **WMPLib.IWMPPlaylist** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="4699d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4699d-111">Remarks</span></span>

<span data-ttu-id="4699d-112">Normalmente, o conteúdo baseado em DVD é organizado em títulos.</span><span class="sxs-lookup"><span data-stu-id="4699d-112">Typically, DVD-based content organized into titles.</span></span> <span data-ttu-id="4699d-113">Cada título contém um ou mais capítulos.</span><span class="sxs-lookup"><span data-stu-id="4699d-113">Each title contains one or more chapters.</span></span> <span data-ttu-id="4699d-114">Cada DVD é criado de forma diferente, portanto, como os títulos e capítulos são usados, cabe ao autor do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4699d-114">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="4699d-115">Para um DVD, essa propriedade Obtém uma lista de reprodução que contém como o primeiro item uma interface **IWMPMedia** chamada "DVD".</span><span class="sxs-lookup"><span data-stu-id="4699d-115">For a DVD, this property gets a playlist that contains as the first item an **IWMPMedia** interface named "DVD".</span></span> <span data-ttu-id="4699d-116">Essa interface representa a mídia de DVD.</span><span class="sxs-lookup"><span data-stu-id="4699d-116">This interface represents the DVD media.</span></span> <span data-ttu-id="4699d-117">A reprodução dos resultados do item no DVD será reproduzida desde o início se for a primeira reprodução após a inserção de um novo DVD ou a retomada da reprodução se o DVD for o mesmo que o último DVD exibido.</span><span class="sxs-lookup"><span data-stu-id="4699d-117">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="4699d-118">Definir esse item como o item atual durante os resultados da reprodução no DVD é reproduzido desde o início.</span><span class="sxs-lookup"><span data-stu-id="4699d-118">Setting this item as the current item during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="4699d-119">Itens adicionais (representados por interfaces **IWMPMedia** ) na playlist são títulos de DVD que são representados por listas de reprodução aninhadas.</span><span class="sxs-lookup"><span data-stu-id="4699d-119">Additional items (represented by **IWMPMedia** interfaces) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="4699d-120">Quando você define **IWMPControls. currentItem** como igual a um desses itens aninhados da lista de reprodução, o Windows Media Player define automaticamente a lista de reprodução aninhada como a lista de reprodução atual após a execução do capítulo começar.</span><span class="sxs-lookup"><span data-stu-id="4699d-120">When you set **IWMPControls.currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins.</span></span> <span data-ttu-id="4699d-121">Você pode usar as propriedades de interface **IWMPPlaylist** , métodos e eventos associados para trabalhar com capítulos de DVD, que também são itens de playlist.</span><span class="sxs-lookup"><span data-stu-id="4699d-121">You can then use the **IWMPPlaylist** interface properties, methods and associated events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="4699d-122">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4699d-122">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="4699d-123">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4699d-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4699d-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4699d-124">Examples</span></span>

<span data-ttu-id="4699d-125">O exemplo a seguir usa **playlist** para preencher uma caixa de texto de várias linhas, chamada mytext, com a lista Track do CD de áudio atualmente na primeira unidade de CD.</span><span class="sxs-lookup"><span data-stu-id="4699d-125">The following example uses **Playlist** to fill a multi-line text box, named myText, with the track list of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="4699d-126">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="4699d-126">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a><span data-ttu-id="4699d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4699d-127">Requirements</span></span>



| <span data-ttu-id="4699d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4699d-128">Requirement</span></span> | <span data-ttu-id="4699d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4699d-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4699d-130">Versão</span><span class="sxs-lookup"><span data-stu-id="4699d-130">Version</span></span><br/>   | <span data-ttu-id="4699d-131">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4699d-131">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4699d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="4699d-132">Namespace</span></span><br/> | <span data-ttu-id="4699d-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4699d-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4699d-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="4699d-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4699d-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4699d-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4699d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4699d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4699d-137">**Interface IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4699d-137">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4699d-138">**IWMPControls. currentItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4699d-138">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4699d-139">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4699d-139">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4699d-140">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4699d-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4699d-141">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4699d-141">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4699d-142">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4699d-142">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





