---
title: Método GetAttributeName de IWMPMedia
description: O método GetAttributeName retorna o nome do atributo correspondente ao índice especificado.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- método GetAttributeName do Windows Media Player
- método GetAttributeName Windows Media Player, interface IWMPMedia
- Interface IWMPMedia do Windows Media Player, método GetAttributeName
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756847"
---
# <a name="iwmpmediagetattributename-method"></a><span data-ttu-id="3e8af-106">Método IWMPMedia:: GetAttributeName</span><span class="sxs-lookup"><span data-stu-id="3e8af-106">IWMPMedia::getAttributeName method</span></span>

<span data-ttu-id="3e8af-107">O método **GetAttributeName** retorna o nome do atributo correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="3e8af-107">The **getAttributeName** method returns the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8af-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e8af-108">Syntax</span></span>


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a><span data-ttu-id="3e8af-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e8af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8af-110">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e8af-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e8af-111">Um **System. Int32** que é o índice.</span><span class="sxs-lookup"><span data-stu-id="3e8af-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8af-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e8af-112">Return value</span></span>

<span data-ttu-id="3e8af-113">Um **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="3e8af-113">A **System.String** that is the attribute name.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e8af-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e8af-114">Remarks</span></span>

<span data-ttu-id="3e8af-115">O nome do atributo retornado pode ser usado em conjunto com **getItemInfo** para recuperar o valor de um atributo nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="3e8af-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="3e8af-116">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3e8af-116">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="3e8af-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3e8af-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3e8af-118">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3e8af-118">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3e8af-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e8af-119">Examples</span></span>

<span data-ttu-id="3e8af-120">O exemplo a seguir usa **GetAttributeName** para preencher uma caixa de texto de várias linhas com o índice e o nome de cada atributo para o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="3e8af-120">The following example uses **getAttributeName** to fill a multi-line text box with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="3e8af-121">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="3e8af-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a><span data-ttu-id="3e8af-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e8af-122">Requirements</span></span>



| <span data-ttu-id="3e8af-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e8af-123">Requirement</span></span> | <span data-ttu-id="3e8af-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3e8af-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8af-125">Versão</span><span class="sxs-lookup"><span data-stu-id="3e8af-125">Version</span></span><br/>   | <span data-ttu-id="3e8af-126">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="3e8af-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3e8af-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e8af-127">Namespace</span></span><br/> | <span data-ttu-id="3e8af-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3e8af-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3e8af-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="3e8af-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3e8af-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3e8af-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8af-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e8af-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8af-132">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3e8af-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3e8af-133">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3e8af-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





