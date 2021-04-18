---
title: Método IWMPMediaCollection getAll
description: O método getAll retorna uma interface IWMPPlaylist que corresponde à playlist que contém todos os itens de mídia na biblioteca.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- método getAll Windows Media Player
- método getAll Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750729"
---
# <a name="iwmpmediacollectiongetall-method"></a><span data-ttu-id="fca7f-106">Método IWMPMediaCollection:: getAll</span><span class="sxs-lookup"><span data-stu-id="fca7f-106">IWMPMediaCollection::getAll method</span></span>

<span data-ttu-id="fca7f-107">O método **getAll** retorna uma interface **IWMPPlaylist** que corresponde à playlist que contém todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fca7f-107">The **getAll** method returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca7f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fca7f-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="fca7f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fca7f-109">Parameters</span></span>

<span data-ttu-id="fca7f-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fca7f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fca7f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fca7f-111">Return value</span></span>

<span data-ttu-id="fca7f-112">A interface **WMPLib. IWMPPlaylist** da lista de reprodução que contém todos os itens de mídia solicitados.</span><span class="sxs-lookup"><span data-stu-id="fca7f-112">The **WMPLib.IWMPPlaylist** interface for the playlist that contains all of the requested media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="fca7f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fca7f-113">Remarks</span></span>

<span data-ttu-id="fca7f-114">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fca7f-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="fca7f-115">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fca7f-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fca7f-116">Há duas maneiras de recuperar uma interface **IWMPMediaCollection** , e o comportamento do método **getAll** depende de quais dessas duas maneiras você usa.</span><span class="sxs-lookup"><span data-stu-id="fca7f-116">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getAll** method depends on which of those two ways you use.</span></span> <span data-ttu-id="fca7f-117">Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método **getAll** retornará todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fca7f-117">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getAll** method returns all the media items in the library.</span></span> <span data-ttu-id="fca7f-118">No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método **getAll** retornará apenas os itens de áudio na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fca7f-118">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getAll** method returns only the audio items in the library.</span></span>

## <a name="examples"></a><span data-ttu-id="fca7f-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fca7f-119">Examples</span></span>

<span data-ttu-id="fca7f-120">O exemplo a seguir usa **getAll** para reproduzir itens de mídia aleatoriamente da coleção de mídias.</span><span class="sxs-lookup"><span data-stu-id="fca7f-120">The following example uses **getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="fca7f-121">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="fca7f-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="fca7f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fca7f-122">Requirements</span></span>



| <span data-ttu-id="fca7f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca7f-123">Requirement</span></span> | <span data-ttu-id="fca7f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fca7f-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca7f-125">Versão</span><span class="sxs-lookup"><span data-stu-id="fca7f-125">Version</span></span><br/>   | <span data-ttu-id="fca7f-126">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="fca7f-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fca7f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fca7f-127">Namespace</span></span><br/> | <span data-ttu-id="fca7f-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fca7f-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fca7f-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="fca7f-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fca7f-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fca7f-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fca7f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fca7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca7f-132">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fca7f-132">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fca7f-133">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fca7f-133">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





