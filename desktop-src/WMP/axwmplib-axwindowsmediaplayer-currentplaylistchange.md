---
title: Evento CurrentPlaylistChange do objeto AxWindowsMediaPlayer
description: O evento CurrentPlaylistChange ocorre quando algo é alterado na playlist atual. | Evento CurrentPlaylistChange do objeto AxWindowsMediaPlayer
ms.assetid: 1f9c99a4-7d10-48bf-b5ff-b1c1d6753b20
keywords:
- Evento CurrentPlaylistChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99f34f0e02d03352a61bbfca6767295d63d59a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810586"
---
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d4cb1-105">Evento CurrentPlaylistChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d4cb1-105">CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d4cb1-106">O evento CurrentPlaylistChange ocorre quando algo é alterado na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-106">The CurrentPlaylistChange event occurs when something changes within the current playlist.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistChange(
  object sender,
  _WMPOCXEvents_CurrentPlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistChangeEvent
) Handles player.CurrentPlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="d4cb1-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="d4cb1-107">Event Data</span></span>

<span data-ttu-id="d4cb1-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEventHandler**.</span></span> <span data-ttu-id="d4cb1-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d4cb1-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4cb1-110">Property</span></span> | <span data-ttu-id="d4cb1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4cb1-111">Description</span></span>                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cb1-112">alterar</span><span class="sxs-lookup"><span data-stu-id="d4cb1-112">change</span></span>   | <span data-ttu-id="d4cb1-113">Valor de enumeração WMPLib. WMPPlaylistChangeEventTypeAn que indica o tipo de alteração ocorrida na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-113">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4cb1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4cb1-114">Remarks</span></span>

<span data-ttu-id="d4cb1-115">Esse evento não ocorre quando uma playlist diferente se torna a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-115">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="d4cb1-116">Ocorre somente quando uma alteração ocorre na playlist atual, como um item de mídia que está sendo anexado à playlist.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-116">It occurs only when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="d4cb1-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4cb1-117">Examples</span></span>

<span data-ttu-id="d4cb1-118">O exemplo a seguir exibe os nomes de todos os itens de mídia na playlist atual em resposta ao evento CurrentPlaylistChange.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-118">The following example displays the names of all the media items in the current playlist in response to the CurrentPlaylistChange Event.</span></span> <span data-ttu-id="d4cb1-119">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="d4cb1-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentPlaylistChange event.
player.CurrentPlaylistChange += new AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEventHandler(player_CurrentPlaylistChange);  


private void player_CurrentPlaylistChange(object sender, AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent e)
{
    switch(e.change)
    {
        // Only update the list for the move, delete, insert, and append event types.
        case WMPLib.WMPPlaylistChangeEventType.wmplcMove:    // Value = 3
        case WMPLib.WMPPlaylistChangeEventType.wmplcDelete:  // Value = 4
        case WMPLib.WMPPlaylistChangeEventType.wmplcInsert:  // Value = 5
        case WMPLib.WMPPlaylistChangeEventType.wmplcAppend:  // Value = 6

        // Create a string array large enough to hold all of the media item names.
        int count = player.currentPlaylist.count;
        string[] mediaItems = new string[count];

        // Clear any previous contents of the text box.
        playlistItems.Clear();

        // Loop through the playlist and store each media item name.
        for (int i = 0; i < count; i++)
        {
            mediaItems[i] = player.currentPlaylist.get_Item(i).name;
        }

        // Display the media item names.
        playlistItems.Lines = mediaItems;
        break;
      
        default:
            break;
    }
}
```


```VB

Public Sub player_CurrentPlaylistChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent) Handles player.CurrentPlaylistChange

    Select Case e.change

        &#39; Only update the list for the move, delete, insert, and append event types.
        Case WMPLib.WMPPlaylistChangeEventType.wmplcMove   &#39; Value = 3
        Case WMPLib.WMPPlaylistChangeEventType.wmplcDelete &#39; Value = 4
        Case WMPLib.WMPPlaylistChangeEventType.wmplcInsert &#39; Value = 5
        Case WMPLib.WMPPlaylistChangeEventType.wmplcAppend &#39; Value = 6

            &#39; Create a string array large enough to hold all of the media item names.
            Dim count As Integer = player.currentPlaylist.count
            Dim mediaItems(count) As String

            &#39; Clear any previous contents of the text box.
            playlistItems.Clear()

            &#39; Loop through the playlist and store each media item name.
            For i As Integer = 0 To (count - 1)

                mediaItems(i) = player.currentPlaylist.Item(i).name

            Next i

            &#39; Display the media item names.
            playlistItems.Lines = mediaItems
    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d4cb1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4cb1-120">Requirements</span></span>



| <span data-ttu-id="d4cb1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4cb1-121">Requirement</span></span> | <span data-ttu-id="d4cb1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d4cb1-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cb1-123">Versão</span><span class="sxs-lookup"><span data-stu-id="d4cb1-123">Version</span></span><br/>   | <span data-ttu-id="d4cb1-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="d4cb1-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d4cb1-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4cb1-125">Namespace</span></span><br/> | <span data-ttu-id="d4cb1-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d4cb1-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d4cb1-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="d4cb1-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d4cb1-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d4cb1-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4cb1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4cb1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4cb1-130">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d4cb1-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d4cb1-131">**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d4cb1-131">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d4cb1-132">**Evento AxWindowsMediaPlayer. PlaylistChange (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d4cb1-132">**AxWindowsMediaPlayer.PlaylistChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[<span data-ttu-id="d4cb1-133">**WMPPlaylistChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="d4cb1-133">**WMPPlaylistChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





