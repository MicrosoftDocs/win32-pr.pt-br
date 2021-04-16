---
title: Método IWMPMedia isReadOnlyItem
description: O método isReadOnlyItem retorna um valor que indica se os atributos do item de mídia especificado podem ser editados.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- método isReadOnlyItem Windows Media Player
- método isReadOnlyItem Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método isReadOnlyItem
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750731"
---
# <a name="iwmpmediaisreadonlyitem-method"></a><span data-ttu-id="0215f-106">Método IWMPMedia:: isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="0215f-106">IWMPMedia::isReadOnlyItem method</span></span>

<span data-ttu-id="0215f-107">O método **isReadOnlyItem** retorna um valor que indica se os atributos do item de mídia especificado podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="0215f-107">The **isReadOnlyItem** method returns a value indicating whether the attributes of the specified media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="0215f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0215f-108">Syntax</span></span>


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a><span data-ttu-id="0215f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0215f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0215f-110">*bstrItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0215f-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0215f-111">Um **System. String** que é o nome do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="0215f-111">A **System.String** that is the name of the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0215f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0215f-112">Return value</span></span>

<span data-ttu-id="0215f-113">Um valor **System. Boolean** que indica se os atributos são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0215f-113">A **System.Boolean** value that indicates whether the attributes are read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="0215f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0215f-114">Remarks</span></span>

<span data-ttu-id="0215f-115">Se um atributo for somente leitura, ele não poderá ser definido com o método **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="0215f-115">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="0215f-116">Observe que esse método pode retornar valores diferentes para um atributo específico quando usado com versões diferentes do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0215f-116">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="0215f-117">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0215f-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="0215f-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0215f-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0215f-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0215f-119">Examples</span></span>

<span data-ttu-id="0215f-120">O exemplo a seguir usa **isReadOnlyItem** para preencher uma caixa de texto de várias linhas com informações sobre o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="0215f-120">The following example uses **isReadOnlyItem** to fill a multi-line text box with information about the current media item.</span></span> <span data-ttu-id="0215f-121">O código exibe cada atributo do item de mídia atual, juntamente com o texto que indica se o atributo é somente leitura ou leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0215f-121">The code displays each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="0215f-122">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="0215f-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a><span data-ttu-id="0215f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0215f-123">Requirements</span></span>



| <span data-ttu-id="0215f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0215f-124">Requirement</span></span> | <span data-ttu-id="0215f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0215f-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0215f-126">Versão</span><span class="sxs-lookup"><span data-stu-id="0215f-126">Version</span></span><br/>   | <span data-ttu-id="0215f-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0215f-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0215f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0215f-128">Namespace</span></span><br/> | <span data-ttu-id="0215f-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0215f-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0215f-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="0215f-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0215f-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0215f-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0215f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0215f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0215f-133">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0215f-133">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0215f-134">**IWMPMedia. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0215f-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





