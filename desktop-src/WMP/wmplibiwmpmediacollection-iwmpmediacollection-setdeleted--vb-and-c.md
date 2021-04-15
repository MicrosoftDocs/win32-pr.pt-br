---
title: Método setdeleted IWMPMediaCollection
description: O método setdeled move o item de mídia especificado para a pasta itens excluídos. | Método setdeleted IWMPMediaCollection
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- método setdeled Media Player do Windows
- método setdeleted Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método setdeleted
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761055"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a><span data-ttu-id="5c6b1-107">Método IWMPMediaCollection:: setdeleted</span><span class="sxs-lookup"><span data-stu-id="5c6b1-107">IWMPMediaCollection::setDeleted method</span></span>

<span data-ttu-id="5c6b1-108">O `setDeleted` método move o item de mídia especificado para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-108">The `setDeleted` method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6b1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c6b1-109">Syntax</span></span>


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a><span data-ttu-id="5c6b1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c6b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c6b1-111">*pItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c6b1-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6b1-112">Uma interface **WMPLib. IWMPMedia** para o item a ser movido.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-112">A **WMPLib.IWMPMedia** interface for the item to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="5c6b1-113">*varfIsDeleted* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c6b1-113">*varfIsDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6b1-114">Um valor **System. Boolean** que especifica se o item deve ser movido para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-114">A **System.Boolean** value that specifies whether the item should be moved to the deleted items folder.</span></span> <span data-ttu-id="5c6b1-115">Esse valor deve ser sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-115">This value must always be **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c6b1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c6b1-116">Return value</span></span>

<span data-ttu-id="5c6b1-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c6b1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c6b1-118">Remarks</span></span>

<span data-ttu-id="5c6b1-119">Esse método não remove arquivos do computador do usuário, apenas os move para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-119">This method does not remove files from the user's computer, it just moves them to the deleted items folder.</span></span>

<span data-ttu-id="5c6b1-120">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-120">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="5c6b1-121">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5c6b1-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c6b1-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c6b1-122">Examples</span></span>

<span data-ttu-id="5c6b1-123">O exemplo a seguir usa `setDeleted` para mover um item de mídia específico para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-123">The following example uses `setDeleted` to move a particular media item to the deleted items folder.</span></span> <span data-ttu-id="5c6b1-124">O método **IsDeleted** testa primeiro se o item já foi excluído.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-124">The **isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="5c6b1-125">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="5c6b1-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="5c6b1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c6b1-126">Requirements</span></span>



| <span data-ttu-id="5c6b1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c6b1-127">Requirement</span></span> | <span data-ttu-id="5c6b1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5c6b1-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6b1-129">Versão</span><span class="sxs-lookup"><span data-stu-id="5c6b1-129">Version</span></span><br/>   | <span data-ttu-id="5c6b1-130">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5c6b1-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5c6b1-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c6b1-131">Namespace</span></span><br/> | <span data-ttu-id="5c6b1-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5c6b1-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5c6b1-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="5c6b1-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5c6b1-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5c6b1-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c6b1-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c6b1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c6b1-136">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5c6b1-136">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c6b1-137">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5c6b1-137">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





