---
description: A propriedade item é uma propriedade somente leitura que retorna um registro em uma coleção de objetos Recordlist.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: Propriedade recordlist. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780506"
---
# <a name="recordlistitem-property"></a><span data-ttu-id="52b46-103">Propriedade recordlist. Item</span><span class="sxs-lookup"><span data-stu-id="52b46-103">RecordList.Item property</span></span>

<span data-ttu-id="52b46-104">A propriedade **Item** é uma propriedade somente leitura que retorna um registro em uma coleção de objetos [**recordlist**](recordlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="52b46-104">The **Item** property is a read-only property that returns a record in a [**RecordList**](recordlist-object.md) Object collection.</span></span>

<span data-ttu-id="52b46-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="52b46-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b46-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52b46-106">Syntax</span></span>


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a><span data-ttu-id="52b46-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52b46-107">Property value</span></span>

<span data-ttu-id="52b46-108">Número de índice do item com a coleção de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="52b46-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="52b46-109">O índice é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="52b46-109">Index is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="52b46-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="52b46-110">Remarks</span></span>

<span data-ttu-id="52b46-111">O cliente deve verificar se o objeto [**recordlist**](recordlist-object.md) existe e não está vazio antes de fazer referência à propriedade item.</span><span class="sxs-lookup"><span data-stu-id="52b46-111">The client must verify that the [**RecordList**](recordlist-object.md) object exists and is not empty before referencing the Item property.</span></span>

## <a name="requirements"></a><span data-ttu-id="52b46-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52b46-112">Requirements</span></span>



| <span data-ttu-id="52b46-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="52b46-113">Requirement</span></span> | <span data-ttu-id="52b46-114">Valor</span><span class="sxs-lookup"><span data-stu-id="52b46-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b46-115">Versão</span><span class="sxs-lookup"><span data-stu-id="52b46-115">Version</span></span><br/> | <span data-ttu-id="52b46-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52b46-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="52b46-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52b46-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="52b46-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="52b46-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="52b46-119">DLL</span><span class="sxs-lookup"><span data-stu-id="52b46-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="52b46-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52b46-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="52b46-121">IID</span><span class="sxs-lookup"><span data-stu-id="52b46-121">IID</span></span><br/>     | <span data-ttu-id="52b46-122">IID \_ IRecordList é definido como 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="52b46-122">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




