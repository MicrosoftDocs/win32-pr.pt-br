---
title: IWMPPlaylist. Item (VB e C)
description: A Propriedade Item (o \_ método get item em C \) Obtém uma interface para o item de mídia no índice especificado.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- IWMPPlaylist. Item (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760251"
---
# <a name="iwmpplaylistitem-vb-and-c"></a><span data-ttu-id="4dc85-104">IWMPPlaylist. Item (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="4dc85-104">IWMPPlaylist.Item (VB and C#)</span></span>

<span data-ttu-id="4dc85-105">A propriedade **Item** (o método **Get \_ Item** em C#) Obtém uma interface para o item de mídia no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4dc85-105">The **Item** property (the **get\_Item** method in C#) gets an interface to the media item at the specified index.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a><span data-ttu-id="4dc85-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4dc85-106">Parameters</span></span>

<span data-ttu-id="4dc85-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="4dc85-107">*lIndex*</span></span>

<span data-ttu-id="4dc85-108">Um **System. Int32** que é o índice do item de mídia na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4dc85-108">A **System.Int32** that is the index of the media item in the playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="4dc85-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4dc85-109">Property Value</span></span>

<span data-ttu-id="4dc85-110">Uma interface **WMPLib. IWMPMedia** que fornece acesso ao item de mídia no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4dc85-110">An **WMPLib.IWMPMedia** interface that provides access to the media item at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dc85-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dc85-111">Remarks</span></span>

<span data-ttu-id="4dc85-112">**IWMPPlaylist. Item** é uma propriedade somente leitura no Visual Basic que usa um parâmetro, enquanto em C# ele é referido como o método **IWMPPlaylist. get \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="4dc85-112">**IWMPPlaylist.Item** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_Item** method.</span></span>

## <a name="examples"></a><span data-ttu-id="4dc85-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4dc85-113">Examples</span></span>

<span data-ttu-id="4dc85-114">O exemplo a seguir usa a propriedade **Item** (o método **Get \_ Item** em C#) para recuperar um item de mídia de uma lista de reprodução com base em uma seleção de usuário.</span><span class="sxs-lookup"><span data-stu-id="4dc85-114">The following example uses the **Item** property (the **get\_Item** method in C#) to retrieve a media item from a playlist based on a user selection.</span></span> <span data-ttu-id="4dc85-115">Uma caixa de listagem foi criada com o nome weblist e preenchida com os títulos da lista de reprodução chamado audioPlaylist.</span><span class="sxs-lookup"><span data-stu-id="4dc85-115">A list box was created with the name weblist, and filled with the titles from the playlist called audioPlaylist.</span></span> <span data-ttu-id="4dc85-116">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="4dc85-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4dc85-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dc85-117">Requirements</span></span>



| <span data-ttu-id="4dc85-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dc85-118">Requirement</span></span> | <span data-ttu-id="4dc85-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4dc85-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc85-120">Versão</span><span class="sxs-lookup"><span data-stu-id="4dc85-120">Version</span></span><br/>   | <span data-ttu-id="4dc85-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4dc85-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4dc85-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="4dc85-122">Namespace</span></span><br/> | <span data-ttu-id="4dc85-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4dc85-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4dc85-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="4dc85-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4dc85-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4dc85-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dc85-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dc85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc85-127">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4dc85-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dc85-128">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4dc85-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dc85-129">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4dc85-129">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dc85-130">**IWMPPlaylist. removeItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4dc85-130">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dc85-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4dc85-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dc85-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4dc85-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





