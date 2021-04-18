---
title: Método de item IWMPCdromCollection
description: O método Item retorna uma interface IWMPCdrom no índice fornecido.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Método de item Windows Media Player
- Método de item Windows Media Player, interface IWMPCdromCollection
- Interface IWMPCdromCollection do Windows Media Player, método de item
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791343"
---
# <a name="iwmpcdromcollectionitem-method"></a><span data-ttu-id="52933-106">Método IWMPCdromCollection:: item</span><span class="sxs-lookup"><span data-stu-id="52933-106">IWMPCdromCollection::Item method</span></span>

<span data-ttu-id="52933-107">O método **Item** retorna uma interface **IWMPCdrom** no índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="52933-107">The **Item** method returns an **IWMPCdrom** interface at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="52933-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52933-108">Syntax</span></span>


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="52933-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52933-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52933-110">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52933-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52933-111">Um **System. Int32** que é o índice.</span><span class="sxs-lookup"><span data-stu-id="52933-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52933-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52933-112">Return value</span></span>

<span data-ttu-id="52933-113">Uma interface **WMPLib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="52933-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="52933-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="52933-114">Remarks</span></span>

<span data-ttu-id="52933-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="52933-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="52933-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="52933-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="52933-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52933-117">Examples</span></span>

<span data-ttu-id="52933-118">O exemplo a seguir usa **Item** para exibir o especificador de unidade e o nome da lista de reprodução de cada CD disponível no computador em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="52933-118">The following example uses **Item** to display the drive specifier and playlist name from each CD available on the computer in a list box.</span></span> <span data-ttu-id="52933-119">Se a unidade realmente contiver conteúdo de DVD, o Windows XP ou posterior será necessário.</span><span class="sxs-lookup"><span data-stu-id="52933-119">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="52933-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="52933-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a><span data-ttu-id="52933-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52933-121">Requirements</span></span>



| <span data-ttu-id="52933-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="52933-122">Requirement</span></span> | <span data-ttu-id="52933-123">Valor</span><span class="sxs-lookup"><span data-stu-id="52933-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52933-124">Versão</span><span class="sxs-lookup"><span data-stu-id="52933-124">Version</span></span><br/>   | <span data-ttu-id="52933-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="52933-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="52933-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="52933-126">Namespace</span></span><br/> | <span data-ttu-id="52933-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="52933-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="52933-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="52933-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="52933-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="52933-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52933-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="52933-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52933-131">**Interface IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="52933-131">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52933-132">**Interface IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="52933-132">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52933-133">**IWMPCdromCollection. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="52933-133">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52933-134">**IWMPCdromCollection. getByDriveSpecifier (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="52933-134">**IWMPCdromCollection.getByDriveSpecifier (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52933-135">**IWMPPlaylist.name (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="52933-135">**IWMPPlaylist.name (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52933-136">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="52933-136">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52933-137">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="52933-137">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





