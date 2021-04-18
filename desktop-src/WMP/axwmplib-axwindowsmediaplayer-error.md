---
title: Evento de erro do objeto AxWindowsMediaPlayer
description: O evento de erro ocorre quando o controle do Windows Media Player tem uma condição de erro.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Evento de erro do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794520"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="bc86d-104">Evento de erro do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="bc86d-104">Error Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="bc86d-105">O evento de erro ocorre quando o controle do Windows Media Player tem uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="bc86d-105">The Error event occurs when the Windows Media Player control has an error condition.</span></span>

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a><span data-ttu-id="bc86d-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="bc86d-106">Event Data</span></span>

<span data-ttu-id="bc86d-107">Este evento não contém dados.</span><span class="sxs-lookup"><span data-stu-id="bc86d-107">This event does not contain data.</span></span>

## <a name="examples"></a><span data-ttu-id="bc86d-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc86d-108">Examples</span></span>

<span data-ttu-id="bc86d-109">O exemplo a seguir cria um manipulador de eventos para o evento de erro exibir o texto de descrição para o primeiro erro na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="bc86d-109">The following example creates an event handler for the Error event to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="bc86d-110">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="bc86d-110">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="bc86d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc86d-111">Requirements</span></span>



| <span data-ttu-id="bc86d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc86d-112">Requirement</span></span> | <span data-ttu-id="bc86d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="bc86d-113">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc86d-114">Versão</span><span class="sxs-lookup"><span data-stu-id="bc86d-114">Version</span></span><br/>   | <span data-ttu-id="bc86d-115">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="bc86d-115">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="bc86d-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc86d-116">Namespace</span></span><br/> | <span data-ttu-id="bc86d-117">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="bc86d-117">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="bc86d-118">Assembly</span><span class="sxs-lookup"><span data-stu-id="bc86d-118">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bc86d-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bc86d-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc86d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc86d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc86d-121">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc86d-121">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc86d-122">**IWMPError. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc86d-122">**IWMPError.Item (VB and C#)**</span></span>](iwmperror-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc86d-123">**IWMPErrorItem. errorDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="bc86d-123">**IWMPErrorItem.errorDescription (VB and C#)**</span></span>](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





