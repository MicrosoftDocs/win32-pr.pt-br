---
title: Método IWMPMediaCollection getAttributeStringCollection
description: O método getAttributeStringCollection retorna uma interface IWMPStringCollection que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- método getAttributeStringCollection Windows Media Player
- método getAttributeStringCollection Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getAttributeStringCollection
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef25cd811890e82273fd5d634633e25e7ec460c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770317"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a><span data-ttu-id="433d7-106">Método IWMPMediaCollection:: getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="433d7-106">IWMPMediaCollection::getAttributeStringCollection method</span></span>

<span data-ttu-id="433d7-107">O método **getAttributeStringCollection** retorna uma interface **IWMPStringCollection** que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="433d7-107">The **getAttributeStringCollection** method returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="433d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="433d7-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a><span data-ttu-id="433d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="433d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="433d7-110">*bstrattribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="433d7-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="433d7-111">Um **System. String** que é o atributo para o qual os valores são recuperados.</span><span class="sxs-lookup"><span data-stu-id="433d7-111">A **System.String** that is the attribute for which the values are retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="433d7-112">*bstrMediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="433d7-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="433d7-113">Um **System. String** que é o tipo de mídia para o qual os valores são recuperados.</span><span class="sxs-lookup"><span data-stu-id="433d7-113">A **System.String** that is the media type for which the values are retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="433d7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="433d7-114">Return value</span></span>

<span data-ttu-id="433d7-115">Uma interface **WMPLib. IWMPStringCollection** para os valores recuperados.</span><span class="sxs-lookup"><span data-stu-id="433d7-115">A **WMPLib.IWMPStringCollection** interface for the retrieved values.</span></span>

## <a name="remarks"></a><span data-ttu-id="433d7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="433d7-116">Remarks</span></span>

<span data-ttu-id="433d7-117">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="433d7-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="433d7-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="433d7-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="433d7-119">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="433d7-119">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="433d7-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="433d7-120">Examples</span></span>

<span data-ttu-id="433d7-121">O exemplo a seguir usa **getAttributeStringCollection** para exibir uma lista de valores que correspondem a um atributo específico para itens de áudio na coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="433d7-121">The following example uses **getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="433d7-122">Uma caixa de listagem permite que o usuário selecione um atributo, como artista, gênero ou álbum, e uma caixa de texto de várias linhas exibe o resultado.</span><span class="sxs-lookup"><span data-stu-id="433d7-122">A list box allows the user to select an attribute, such as Artist, Genre, or Album and a multi-line text box displays the result.</span></span> <span data-ttu-id="433d7-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="433d7-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

End Sub
```





## <a name="requirements"></a><span data-ttu-id="433d7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="433d7-124">Requirements</span></span>



| <span data-ttu-id="433d7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="433d7-125">Requirement</span></span> | <span data-ttu-id="433d7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="433d7-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433d7-127">Versão</span><span class="sxs-lookup"><span data-stu-id="433d7-127">Version</span></span><br/>   | <span data-ttu-id="433d7-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="433d7-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="433d7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="433d7-129">Namespace</span></span><br/> | <span data-ttu-id="433d7-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="433d7-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="433d7-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="433d7-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="433d7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="433d7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433d7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="433d7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433d7-134">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="433d7-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="433d7-135">**Interface IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="433d7-135">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





