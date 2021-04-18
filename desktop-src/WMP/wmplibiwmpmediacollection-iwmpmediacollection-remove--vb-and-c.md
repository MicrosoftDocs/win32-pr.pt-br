---
title: Método de remoção de IWMPMediaCollection
description: O método remove remove um item especificado da coleção de mídia.
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- remover método Windows Media Player
- método de remoção do Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, remover método
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d341f8974255dab5e3cdce356a9b221eddff193c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796134"
---
# <a name="iwmpmediacollectionremove-method"></a><span data-ttu-id="47853-106">Método IWMPMediaCollection:: Remove</span><span class="sxs-lookup"><span data-stu-id="47853-106">IWMPMediaCollection::remove method</span></span>

<span data-ttu-id="47853-107">O `remove` método Remove um item especificado da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="47853-107">The `remove` method removes a specified item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="47853-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47853-108">Syntax</span></span>


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="47853-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47853-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47853-110">*pItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47853-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47853-111">Uma interface **WMPLib. IWMPMedia** que identifica o item a ser removido.</span><span class="sxs-lookup"><span data-stu-id="47853-111">A **WMPLib.IWMPMedia** interface that identifies the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="47853-112">*varfDeleteFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47853-112">*varfDeleteFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47853-113">Um valor **System. Boolean** que especifica se o método deve remover o item especificado da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="47853-113">A **System.Boolean** value that specifies whether the method should remove the specified item from the library.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47853-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47853-114">Return value</span></span>

<span data-ttu-id="47853-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="47853-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47853-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="47853-116">Remarks</span></span>

<span data-ttu-id="47853-117">Esse método exclui um item da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="47853-117">This method deletes an item from the library.</span></span> <span data-ttu-id="47853-118">Esse método não exclui arquivos do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="47853-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="47853-119">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="47853-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="47853-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="47853-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47853-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47853-121">Examples</span></span>

<span data-ttu-id="47853-122">O exemplo a seguir, depois de solicitar o usuário, exclui permanentemente o primeiro item de mídia na coleção de mídia usando `remove` .</span><span class="sxs-lookup"><span data-stu-id="47853-122">The following example, after prompting the user, permanently deletes the first media item in the media collection by using `remove`.</span></span> <span data-ttu-id="47853-123">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="47853-123">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a><span data-ttu-id="47853-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47853-124">Requirements</span></span>



| <span data-ttu-id="47853-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="47853-125">Requirement</span></span> | <span data-ttu-id="47853-126">Valor</span><span class="sxs-lookup"><span data-stu-id="47853-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47853-127">Versão</span><span class="sxs-lookup"><span data-stu-id="47853-127">Version</span></span><br/>   | <span data-ttu-id="47853-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="47853-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="47853-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="47853-129">Namespace</span></span><br/> | <span data-ttu-id="47853-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="47853-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="47853-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="47853-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="47853-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="47853-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47853-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="47853-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47853-134">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="47853-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="47853-135">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="47853-135">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="47853-136">**IWMPMediaCollection. Add (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="47853-136">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





