---
description: A propriedade item é uma propriedade somente leitura que retorna uma cadeia de caracteres na coleção de objetos StringList.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Propriedade StringList. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749983"
---
# <a name="stringlistitem-property"></a><span data-ttu-id="c3ce9-103">Propriedade StringList. Item</span><span class="sxs-lookup"><span data-stu-id="c3ce9-103">StringList.Item property</span></span>

<span data-ttu-id="c3ce9-104">A propriedade **Item** é uma propriedade somente leitura que retorna uma cadeia de caracteres na coleção de [**objetos StringList**](stringlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c3ce9-104">The **Item** property is a read-only property that returns a string in the [**StringList Object**](stringlist-object.md) collection.</span></span>

<span data-ttu-id="c3ce9-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c3ce9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ce9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3ce9-106">Syntax</span></span>


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a><span data-ttu-id="c3ce9-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c3ce9-107">Property value</span></span>

<span data-ttu-id="c3ce9-108">Número de índice do item com a coleção de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3ce9-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="c3ce9-109">Este parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c3ce9-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ce9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3ce9-110">Remarks</span></span>

<span data-ttu-id="c3ce9-111">O cliente deve verificar se o [**objeto StringList**](stringlist-object.md) existe e não está vazio antes de fazer referência à propriedade **Item** .</span><span class="sxs-lookup"><span data-stu-id="c3ce9-111">The client must verify that the [**StringList Object**](stringlist-object.md) exists and is not empty before referencing the **Item** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ce9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ce9-112">Requirements</span></span>



| <span data-ttu-id="c3ce9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ce9-113">Requirement</span></span> | <span data-ttu-id="c3ce9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c3ce9-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ce9-115">Versão</span><span class="sxs-lookup"><span data-stu-id="c3ce9-115">Version</span></span><br/> | <span data-ttu-id="c3ce9-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3ce9-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c3ce9-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3ce9-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c3ce9-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3ce9-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c3ce9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c3ce9-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3ce9-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3ce9-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c3ce9-121">IID</span><span class="sxs-lookup"><span data-stu-id="c3ce9-121">IID</span></span><br/>     | <span data-ttu-id="c3ce9-122">IID \_ isastringlist é definida como 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c3ce9-122">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




