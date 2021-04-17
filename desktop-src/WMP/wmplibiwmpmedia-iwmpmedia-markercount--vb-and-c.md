---
title: Propriedade IWMPMedia markerCount
description: A propriedade markerCount Obtém o número de marcadores no item de mídia.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- Propriedade markerCount Windows Media Player
- Propriedade markerCount Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade markerCount
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769264"
---
# <a name="iwmpmediamarkercount-property"></a><span data-ttu-id="ee58c-106">Propriedade IWMPMedia:: markerCount</span><span class="sxs-lookup"><span data-stu-id="ee58c-106">IWMPMedia::markerCount property</span></span>

<span data-ttu-id="ee58c-107">A propriedade **markerCount** Obtém o número de marcadores no item de mídia.</span><span class="sxs-lookup"><span data-stu-id="ee58c-107">The **markerCount** property gets the number of markers in the media item.</span></span>

<span data-ttu-id="ee58c-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ee58c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee58c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee58c-109">Syntax</span></span>


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ee58c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ee58c-110">Property value</span></span>

<span data-ttu-id="ee58c-111">Um **System. Int32** que é a contagem de marcadores.</span><span class="sxs-lookup"><span data-stu-id="ee58c-111">A **System.Int32** that is the marker count.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee58c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee58c-112">Remarks</span></span>

<span data-ttu-id="ee58c-113">Essa propriedade retornará zero se um arquivo não tiver marcadores ou se o item de mídia não for o mesmo que o especificado em AxWindowsMediaPlayer. currentMedia.</span><span class="sxs-lookup"><span data-stu-id="ee58c-113">This property returns zero if a file has no markers, or if the media item is not the same as the one specified in AxWindowsMediaPlayer.currentMedia.</span></span>

<span data-ttu-id="ee58c-114">Os números de marcador começam em 1.</span><span class="sxs-lookup"><span data-stu-id="ee58c-114">Marker numbers start at 1.</span></span>

<span data-ttu-id="ee58c-115">Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ee58c-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="ee58c-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ee58c-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ee58c-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee58c-117">Examples</span></span>

<span data-ttu-id="ee58c-118">O exemplo a seguir usa **markerCount** para recuperar o número de marcadores no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="ee58c-118">The following example uses **markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="ee58c-119">Esse valor é usado como o limite superior para uma estrutura de loop, que itera na lista de marcadores para recuperar cada nome de marcador e exibi-lo em uma caixa de texto de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="ee58c-119">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name and display it in a multi-line text box.</span></span> <span data-ttu-id="ee58c-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="ee58c-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a><span data-ttu-id="ee58c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee58c-121">Requirements</span></span>



| <span data-ttu-id="ee58c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee58c-122">Requirement</span></span> | <span data-ttu-id="ee58c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ee58c-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee58c-124">Versão</span><span class="sxs-lookup"><span data-stu-id="ee58c-124">Version</span></span><br/>   | <span data-ttu-id="ee58c-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ee58c-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ee58c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee58c-126">Namespace</span></span><br/> | <span data-ttu-id="ee58c-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ee58c-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ee58c-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="ee58c-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ee58c-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ee58c-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee58c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee58c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee58c-131">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee58c-131">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee58c-132">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee58c-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





