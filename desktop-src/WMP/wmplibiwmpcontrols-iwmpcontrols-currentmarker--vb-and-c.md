---
title: Propriedade IWMPControls currentMarker
description: A propriedade currentMarker Obtém ou define o número do marcador atual.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- Propriedade currentMarker Windows Media Player
- Propriedade currentMarker Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, Propriedade currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796291"
---
# <a name="iwmpcontrolscurrentmarker-property"></a><span data-ttu-id="5b5f6-106">Propriedade IWMPControls:: currentMarker</span><span class="sxs-lookup"><span data-stu-id="5b5f6-106">IWMPControls::currentMarker property</span></span>

<span data-ttu-id="5b5f6-107">A propriedade **currentMarker** Obtém ou define o número do marcador atual.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-107">The **currentMarker** property gets or sets the current marker number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5f6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b5f6-108">Syntax</span></span>


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5b5f6-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5b5f6-109">Property value</span></span>

<span data-ttu-id="5b5f6-110">Um **System. Int32** que é o número do marcador.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-110">A **System.Int32** that is the marker number.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5f6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b5f6-111">Remarks</span></span>

<span data-ttu-id="5b5f6-112">A definição de **currentMarker** faz com que a reprodução seja iniciada a partir do marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-112">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="5b5f6-113">Antes de tentar definir **currentMarker**, determine se um arquivo tem marcadores e quantos deles tem usando **IWMPMedia. markerCount**.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-113">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **IWMPMedia.markerCount**.</span></span> <span data-ttu-id="5b5f6-114">Se um arquivo não tiver marcadores, definir **currentMarker** como qualquer coisa, exceto zero, resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-114">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="5b5f6-115">A definição de **currentMarker** como um número maior que **markerCount** também resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-115">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="5b5f6-116">A propriedade **currentMarker** sempre retorna o marcador atual ou último, o que significa que a posição real do arquivo pode ser no marcador atual ou antes do próximo marcador.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-116">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="5b5f6-117">Os marcadores são numerados começando em 1, portanto, se um arquivo tiver marcadores, você poderá definir **currentMarker** como zero para alterar a posição do arquivo para zero.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-117">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="5b5f6-118">Até que o item de mídia atual seja definido (usando **AxWindowsMediaPlayer. URL** ou **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-118">Until the current media item is set (using **AxWindowsMediaPlayer.URL** or **AxWindowsMediaPlayer.currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="5b5f6-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b5f6-119">Examples</span></span>

<span data-ttu-id="5b5f6-120">O exemplo a seguir usa **currentMarker** para iniciar a reprodução de vídeo do marcador que corresponde à propriedade SelectedIndex de uma caixa de listagem que foi preenchida com identificadores de marcador.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-120">The following example uses **currentMarker** to start video playback from the marker that corresponds to the SelectedIndex property of a list box which has been filled with marker identifiers.</span></span> <span data-ttu-id="5b5f6-121">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="5b5f6-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5b5f6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5f6-122">Requirements</span></span>



| <span data-ttu-id="5b5f6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5f6-123">Requirement</span></span> | <span data-ttu-id="5b5f6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5b5f6-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5f6-125">Versão</span><span class="sxs-lookup"><span data-stu-id="5b5f6-125">Version</span></span><br/>   | <span data-ttu-id="5b5f6-126">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5b5f6-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5b5f6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b5f6-127">Namespace</span></span><br/> | <span data-ttu-id="5b5f6-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5b5f6-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5b5f6-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="5b5f6-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5b5f6-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5b5f6-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5f6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b5f6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5f6-132">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5b5f6-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b5f6-133">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5b5f6-133">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b5f6-134">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5b5f6-134">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b5f6-135">**IWMPMedia. markerCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5b5f6-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





