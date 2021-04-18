---
title: Método getmarcadortime IWMPMedia
description: O método getmarcadortime retorna a hora do marcador no índice especificado.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- método getmarcadortime Windows Media Player
- método getmarcadortime Windows Media Player, interface IWMPMedia
- Interface IWMPMedia do Windows Media Player, método getmarcadortime
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df171977adeee3b597cab1f40469af1d975425c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755383"
---
# <a name="iwmpmediagetmarkertime-method"></a><span data-ttu-id="1d8d6-106">Método IWMPMedia:: getmarcadortime</span><span class="sxs-lookup"><span data-stu-id="1d8d6-106">IWMPMedia::getMarkerTime method</span></span>

<span data-ttu-id="1d8d6-107">O método **Getmarcadortime** retorna a hora do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-107">The **getMarkerTime** method returns the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8d6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d8d6-108">Syntax</span></span>


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a><span data-ttu-id="1d8d6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d8d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d8d6-110">*MarkerNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d8d6-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d8d6-111">Um **System. Int32** que é o índice de marcador.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d8d6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d8d6-112">Return value</span></span>

<span data-ttu-id="1d8d6-113">Um **sistema. Double** que é a hora do marcador.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-113">A **System.Double** that is the marker time.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d8d6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d8d6-114">Remarks</span></span>

<span data-ttu-id="1d8d6-115">Esse método retornará **NULL** se o marcador especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="1d8d6-116">Alguns itens de mídia não contêm marcadores.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-116">Some media items do not contain markers.</span></span> <span data-ttu-id="1d8d6-117">Use **markerCount** para descobrir quantos marcadores estão no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="1d8d6-118">Os números de índice de marcador começam em 1.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="1d8d6-119">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="1d8d6-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1d8d6-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1d8d6-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1d8d6-121">Examples</span></span>

<span data-ttu-id="1d8d6-122">O exemplo de código a seguir usa **Getmarcadortime** para preencher uma caixa de texto de várias linhas com o local de cada marcador.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-122">The following code example uses **getMarkerTime** to fill a multi-line text box with the location of each marker.</span></span> <span data-ttu-id="1d8d6-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="1d8d6-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

End If
```





## <a name="requirements"></a><span data-ttu-id="1d8d6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d8d6-124">Requirements</span></span>



| <span data-ttu-id="1d8d6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d8d6-125">Requirement</span></span> | <span data-ttu-id="1d8d6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1d8d6-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8d6-127">Versão</span><span class="sxs-lookup"><span data-stu-id="1d8d6-127">Version</span></span><br/>   | <span data-ttu-id="1d8d6-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="1d8d6-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1d8d6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d8d6-129">Namespace</span></span><br/> | <span data-ttu-id="1d8d6-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1d8d6-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1d8d6-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="1d8d6-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d8d6-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1d8d6-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d8d6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d8d6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8d6-134">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1d8d6-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d8d6-135">**IWMPMedia. markerCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1d8d6-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





