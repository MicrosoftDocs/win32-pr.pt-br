---
title: Propriedade currentItem IWMPControls
description: A propriedade currentItem Obtém ou define o item de mídia atual em uma lista de reprodução.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- Propriedade currentItem Windows Media Player
- Propriedade currentItem Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, Propriedade currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759929"
---
# <a name="iwmpcontrolscurrentitem-property"></a><span data-ttu-id="5bc1b-106">Propriedade IWMPControls:: currentItem</span><span class="sxs-lookup"><span data-stu-id="5bc1b-106">IWMPControls::currentItem property</span></span>

<span data-ttu-id="5bc1b-107">A propriedade **currentItem** Obtém ou define o item de mídia atual em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-107">The **currentItem** property gets or sets the current media item in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc1b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bc1b-108">Syntax</span></span>


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="5bc1b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5bc1b-109">Property value</span></span>

<span data-ttu-id="5bc1b-110">Uma interface **WMPLib. IWMPMedia** que representa o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-110">A **WMPLib.IWMPMedia** interface that represents the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc1b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bc1b-111">Remarks</span></span>

<span data-ttu-id="5bc1b-112">Essa propriedade funciona apenas com itens na lista de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-112">This property works only with items in the current playlist.</span></span> <span data-ttu-id="5bc1b-113">Não há suporte para a configuração **currentItem** para a interface de um item de mídia salvo.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-113">Setting **currentItem** to the interface of a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5bc1b-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bc1b-114">Examples</span></span>

<span data-ttu-id="5bc1b-115">O exemplo a seguir usa **currentItem** para definir o item de mídia atual do jogador como um item selecionado em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-115">The following example uses **currentItem** to set the player's current media item to an item selected from a list box.</span></span> <span data-ttu-id="5bc1b-116">A caixa de listagem foi preenchida com todos os itens na lista de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-116">The list box has been filled with all of the items in the current playlist.</span></span> <span data-ttu-id="5bc1b-117">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5bc1b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc1b-118">Requirements</span></span>



| <span data-ttu-id="5bc1b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc1b-119">Requirement</span></span> | <span data-ttu-id="5bc1b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5bc1b-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc1b-121">Versão</span><span class="sxs-lookup"><span data-stu-id="5bc1b-121">Version</span></span><br/>   | <span data-ttu-id="5bc1b-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5bc1b-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5bc1b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bc1b-123">Namespace</span></span><br/> | <span data-ttu-id="5bc1b-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5bc1b-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5bc1b-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="5bc1b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5bc1b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc1b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bc1b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc1b-128">**IWMPControlsInterface (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5bc1b-128">**IWMPControlsInterface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5bc1b-129">**IWMPMediaInterface (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5bc1b-129">**IWMPMediaInterface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5bc1b-130">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5bc1b-130">**IWMPPlaylistCollection.getByName(VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





