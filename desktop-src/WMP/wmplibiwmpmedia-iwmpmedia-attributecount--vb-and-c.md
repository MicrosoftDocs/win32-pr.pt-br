---
title: Propriedade IWMPMedia attributeCount
description: A propriedade attributeCount Obtém o número de atributos que podem ser consultados e/ou definidos para o item de mídia.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- Propriedade attributeCount Windows Media Player
- Propriedade attributeCount Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade attributeCount
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756667"
---
# <a name="iwmpmediaattributecount-property"></a><span data-ttu-id="7a806-106">Propriedade IWMPMedia:: attributeCount</span><span class="sxs-lookup"><span data-stu-id="7a806-106">IWMPMedia::attributeCount property</span></span>

<span data-ttu-id="7a806-107">A propriedade **attributeCount** Obtém o número de atributos que podem ser consultados e/ou definidos para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="7a806-107">The **attributeCount** property gets the number of attributes that can be queried and/or set for the media item.</span></span>

<span data-ttu-id="7a806-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7a806-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a806-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a806-109">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="7a806-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7a806-110">Property value</span></span>

<span data-ttu-id="7a806-111">Um **System. Int32** que é a contagem.</span><span class="sxs-lookup"><span data-stu-id="7a806-111">A **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a806-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a806-112">Remarks</span></span>

<span data-ttu-id="7a806-113">Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7a806-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="7a806-114">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7a806-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7a806-115">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7a806-115">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7a806-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a806-116">Examples</span></span>

<span data-ttu-id="7a806-117">O exemplo a seguir usa **attributeCount** para determinar o número de atributos disponíveis no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="7a806-117">The following example uses **attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="7a806-118">O código usa esse valor para exibir uma lista de nomes de atributos e valores em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="7a806-118">The code uses that value to display a list of attribute names and values in a text box.</span></span> <span data-ttu-id="7a806-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="7a806-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a><span data-ttu-id="7a806-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a806-120">Requirements</span></span>



| <span data-ttu-id="7a806-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a806-121">Requirement</span></span> | <span data-ttu-id="7a806-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7a806-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a806-123">Versão</span><span class="sxs-lookup"><span data-stu-id="7a806-123">Version</span></span><br/>   | <span data-ttu-id="7a806-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7a806-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7a806-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a806-125">Namespace</span></span><br/> | <span data-ttu-id="7a806-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7a806-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7a806-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="7a806-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7a806-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7a806-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a806-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a806-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a806-130">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7a806-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





