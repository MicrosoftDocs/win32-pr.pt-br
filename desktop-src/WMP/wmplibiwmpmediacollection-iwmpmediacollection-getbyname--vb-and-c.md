---
title: Método IWMPMediaCollection getByName
description: O método getByName retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia com o nome especificado.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- método getByName Windows Media Player
- método getByName Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755025"
---
# <a name="iwmpmediacollectiongetbyname-method"></a><span data-ttu-id="f44ae-106">Método IWMPMediaCollection:: getByName</span><span class="sxs-lookup"><span data-stu-id="f44ae-106">IWMPMediaCollection::getByName method</span></span>

<span data-ttu-id="f44ae-107">O `getByName` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="f44ae-107">The `getByName` method returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44ae-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f44ae-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="f44ae-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f44ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44ae-110">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f44ae-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44ae-111">O **System. String** que é o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="f44ae-111">The **System.String** that is the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f44ae-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f44ae-112">Return value</span></span>

<span data-ttu-id="f44ae-113">Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.</span><span class="sxs-lookup"><span data-stu-id="f44ae-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="f44ae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f44ae-114">Remarks</span></span>

<span data-ttu-id="f44ae-115">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f44ae-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="f44ae-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f44ae-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f44ae-117">Há duas maneiras de se recuperar uma interface **IWMPMediaCollection** , e o comportamento do `getByName` método depende de quais dessas duas maneiras você usa.</span><span class="sxs-lookup"><span data-stu-id="f44ae-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByName` method depends on which of those two ways you use.</span></span> <span data-ttu-id="f44ae-118">Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o `getByName` método retornará todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f44ae-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByName` method returns all the media items in the library.</span></span> <span data-ttu-id="f44ae-119">No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o `getByName` método retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor especificados.</span><span class="sxs-lookup"><span data-stu-id="f44ae-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByName` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="f44ae-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f44ae-120">Examples</span></span>

<span data-ttu-id="f44ae-121">O exemplo a seguir usa `getByName` para recuperar três itens da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f44ae-121">The following example uses `getByName` to retrieve three items from the library.</span></span> <span data-ttu-id="f44ae-122">Cada item é acrescentado à playlist atual.</span><span class="sxs-lookup"><span data-stu-id="f44ae-122">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="f44ae-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="f44ae-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a><span data-ttu-id="f44ae-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f44ae-124">Requirements</span></span>



| <span data-ttu-id="f44ae-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f44ae-125">Requirement</span></span> | <span data-ttu-id="f44ae-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f44ae-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44ae-127">Versão</span><span class="sxs-lookup"><span data-stu-id="f44ae-127">Version</span></span><br/>   | <span data-ttu-id="f44ae-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f44ae-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f44ae-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f44ae-129">Namespace</span></span><br/> | <span data-ttu-id="f44ae-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f44ae-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f44ae-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="f44ae-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f44ae-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f44ae-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44ae-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f44ae-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44ae-134">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f44ae-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f44ae-135">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f44ae-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





