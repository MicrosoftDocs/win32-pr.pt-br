---
title: Propriedade de nome IWMPMedia
description: A propriedade Name Obtém ou define o nome do item de mídia.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- Propriedade de nome Windows Media Player
- Propriedade Name Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade Name
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757456"
---
# <a name="iwmpmedianame-property"></a><span data-ttu-id="57d2a-106">Propriedade IWMPMedia:: Name</span><span class="sxs-lookup"><span data-stu-id="57d2a-106">IWMPMedia::name property</span></span>

<span data-ttu-id="57d2a-107">A propriedade **Name** Obtém ou define o nome do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="57d2a-107">The **name** property gets or sets the name of the media item.</span></span>

<span data-ttu-id="57d2a-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="57d2a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57d2a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="57d2a-109">Syntax</span></span>


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a><span data-ttu-id="57d2a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="57d2a-110">Property value</span></span>

<span data-ttu-id="57d2a-111">Um **System. String** que é o nome do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="57d2a-111">A **System.String** that is the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="57d2a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="57d2a-112">Remarks</span></span>

<span data-ttu-id="57d2a-113">Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="57d2a-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="57d2a-114">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="57d2a-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="57d2a-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57d2a-115">Examples</span></span>

<span data-ttu-id="57d2a-116">O exemplo a seguir usa **Name** para alterar o nome do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="57d2a-116">The following example uses **name** to change the name of the current media item.</span></span> <span data-ttu-id="57d2a-117">Uma caixa de texto permite que o usuário insira um novo nome e o nome seja alterado em resposta ao evento de clique de um botão.</span><span class="sxs-lookup"><span data-stu-id="57d2a-117">A text box allows the user to enter a new name, and the name is changed in response to the Click event of a button.</span></span> <span data-ttu-id="57d2a-118">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="57d2a-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a><span data-ttu-id="57d2a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57d2a-119">Requirements</span></span>



| <span data-ttu-id="57d2a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57d2a-120">Requirement</span></span> | <span data-ttu-id="57d2a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="57d2a-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57d2a-122">Versão</span><span class="sxs-lookup"><span data-stu-id="57d2a-122">Version</span></span><br/>   | <span data-ttu-id="57d2a-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="57d2a-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="57d2a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="57d2a-124">Namespace</span></span><br/> | <span data-ttu-id="57d2a-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="57d2a-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="57d2a-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="57d2a-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="57d2a-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="57d2a-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57d2a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="57d2a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d2a-129">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="57d2a-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





