---
title: Método GetMarkerName de IWMPMedia
description: O método getmarcadorname retorna o nome do marcador no índice especificado.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- método GetMarkerName do Windows Media Player
- método getmarkname Windows Media Player, interface IWMPMedia
- Interface IWMPMedia do Windows Media Player, método getmarcadorname
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764603"
---
# <a name="iwmpmediagetmarkername-method"></a><span data-ttu-id="d64e7-106">Método IWMPMedia:: GetMarkerName</span><span class="sxs-lookup"><span data-stu-id="d64e7-106">IWMPMedia::getMarkerName method</span></span>

<span data-ttu-id="d64e7-107">O método **Getmarcadorname** retorna o nome do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="d64e7-107">The **getMarkerName** method returns the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64e7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d64e7-108">Syntax</span></span>


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a><span data-ttu-id="d64e7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d64e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64e7-110">*MarkerNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d64e7-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d64e7-111">Um **System. Int32** que é o índice de marcador.</span><span class="sxs-lookup"><span data-stu-id="d64e7-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64e7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d64e7-112">Return value</span></span>

<span data-ttu-id="d64e7-113">Um **System. String** que é o nome do marcador.</span><span class="sxs-lookup"><span data-stu-id="d64e7-113">A **System.String** that is the marker name.</span></span>

## <a name="remarks"></a><span data-ttu-id="d64e7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d64e7-114">Remarks</span></span>

<span data-ttu-id="d64e7-115">Esse método retornará **NULL** se o marcador especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="d64e7-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="d64e7-116">Alguns itens de mídia não contêm marcadores.</span><span class="sxs-lookup"><span data-stu-id="d64e7-116">Some media items do not contain markers.</span></span> <span data-ttu-id="d64e7-117">Use **markerCount** para descobrir quantos marcadores estão no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="d64e7-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="d64e7-118">Os números de índice de marcador começam em 1.</span><span class="sxs-lookup"><span data-stu-id="d64e7-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="d64e7-119">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d64e7-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="d64e7-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d64e7-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d64e7-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d64e7-121">Examples</span></span>

<span data-ttu-id="d64e7-122">O exemplo de código a seguir usa **Getmarcadorname** para preencher uma caixa de texto de várias linhas com os nomes dos marcadores no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="d64e7-122">The following code example uses **getMarkerName** to fill a multi-line text box with the names of the markers in the current media item.</span></span> <span data-ttu-id="d64e7-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="d64e7-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a><span data-ttu-id="d64e7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d64e7-124">Requirements</span></span>



| <span data-ttu-id="d64e7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d64e7-125">Requirement</span></span> | <span data-ttu-id="d64e7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d64e7-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d64e7-127">Versão</span><span class="sxs-lookup"><span data-stu-id="d64e7-127">Version</span></span><br/>   | <span data-ttu-id="d64e7-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="d64e7-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d64e7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="d64e7-129">Namespace</span></span><br/> | <span data-ttu-id="d64e7-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d64e7-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d64e7-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="d64e7-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d64e7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d64e7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d64e7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d64e7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64e7-134">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d64e7-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d64e7-135">**IWMPMedia. markerCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d64e7-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





