---
description: A propriedade Children do objeto item recupera uma coleção de objetos item. Os itens nesta coleção representam itens que são filhos diretos deste item na árvore hierárquica. Somente leitura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Propriedade Item. Children
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798298"
---
# <a name="itemchildren-property"></a><span data-ttu-id="013dc-105">Propriedade Item. Children</span><span class="sxs-lookup"><span data-stu-id="013dc-105">Item.Children property</span></span>

<span data-ttu-id="013dc-106">A propriedade **Children** do objeto [**Item**](-wia-item.md) recupera uma coleção de objetos **Item** .</span><span class="sxs-lookup"><span data-stu-id="013dc-106">The **Children** property of the [**Item**](-wia-item.md) object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="013dc-107">Os itens nesta coleção representam itens que são filhos diretos deste item na árvore hierárquica.</span><span class="sxs-lookup"><span data-stu-id="013dc-107">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <span data-ttu-id="013dc-108">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="013dc-108">Read-only.</span></span>

<span data-ttu-id="013dc-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="013dc-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="013dc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="013dc-110">Syntax</span></span>


```JScript
propVal = Item.Children
```



## <a name="property-value"></a><span data-ttu-id="013dc-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="013dc-111">Property value</span></span>

<span data-ttu-id="013dc-112">Variável que recebe os objetos.</span><span class="sxs-lookup"><span data-stu-id="013dc-112">Variable that receives the objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="013dc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="013dc-113">Remarks</span></span>

<span data-ttu-id="013dc-114">Use essa propriedade para navegar na árvore hierárquica de objetos de [**Item**](-wia-item.md) que representam um dispositivo, as pastas e os arquivos que residem no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="013dc-114">Use this property to navigate the hierarchical tree of [**Item**](-wia-item.md) objects that represent a device, the folders and the files that reside on the device.</span></span>

<span data-ttu-id="013dc-115">A propriedade **Children** é uma coleção de objetos [**Item**](-wia-item.md) somente do nível diretamente abaixo desse objeto **Item** na árvore.</span><span class="sxs-lookup"><span data-stu-id="013dc-115">The **Children** property is a collection of [**Item**](-wia-item.md) objects only from the level directly beneath this **Item** object in the tree.</span></span> <span data-ttu-id="013dc-116">Para navegar por níveis adicionais na árvore, use essa propriedade recursivamente.</span><span class="sxs-lookup"><span data-stu-id="013dc-116">To navigate further levels down the tree, use this property recursively.</span></span>

<span data-ttu-id="013dc-117">Se o item não puder ou não tiver nenhum item filho, essa propriedade retornará uma coleção vazia.</span><span class="sxs-lookup"><span data-stu-id="013dc-117">If the item cannot or does not have any child items, this property returns an empty collection.</span></span>

> [!Note]  
> <span data-ttu-id="013dc-118">Esta coleção é baseada em 0.</span><span class="sxs-lookup"><span data-stu-id="013dc-118">This collection is 0-based.</span></span>

 

## <a name="examples"></a><span data-ttu-id="013dc-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="013dc-119">Examples</span></span>

<span data-ttu-id="013dc-120">O exemplo a seguir demonstra o uso da propriedade **Children** para recuperar e enumerar uma coleção de itens filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="013dc-120">The following example demonstrates the use of the **Children** property to retrieve and enumerate a collection of the child items of a device.</span></span> <span data-ttu-id="013dc-121">Se o dispositivo for uma câmera digital, a coleção normalmente conterá itens de pasta e de imagem.</span><span class="sxs-lookup"><span data-stu-id="013dc-121">If the device is a digital camera, the collection typically contains folder and image items.</span></span> <span data-ttu-id="013dc-122">Se o dispositivo for um scanner, a coleção normalmente conterá itens que representam ambientes de verificação.</span><span class="sxs-lookup"><span data-stu-id="013dc-122">If the device is a scanner, the collection typically contains items that represent scanning beds.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="013dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="013dc-123">Requirements</span></span>



| <span data-ttu-id="013dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="013dc-124">Requirement</span></span> | <span data-ttu-id="013dc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="013dc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="013dc-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="013dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="013dc-127">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="013dc-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="013dc-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="013dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="013dc-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="013dc-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="013dc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="013dc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="013dc-131"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="013dc-131"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




