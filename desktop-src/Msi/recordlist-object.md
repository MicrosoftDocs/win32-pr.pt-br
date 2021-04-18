---
description: O objeto Recordlist é uma coleção de objetos Record. Você deve verificar se o objeto Recordlist existe e não está vazio antes de fazer referência a suas propriedades.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Objeto recordlist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810316"
---
# <a name="recordlist-object"></a><span data-ttu-id="7f898-104">Objeto recordlist</span><span class="sxs-lookup"><span data-stu-id="7f898-104">RecordList object</span></span>

<span data-ttu-id="7f898-105">O objeto **recordlist** é uma coleção de objetos [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="7f898-105">The **RecordList** object is a collection of [**Record**](record-object.md) objects.</span></span> <span data-ttu-id="7f898-106">Você deve verificar se o objeto **recordlist** existe e não está vazio antes de fazer referência a suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7f898-106">You must verify that the **RecordList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="7f898-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7f898-107">Members</span></span>

<span data-ttu-id="7f898-108">O objeto **recordlist** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7f898-108">The **RecordList** object has these types of members:</span></span>

-   [<span data-ttu-id="7f898-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7f898-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f898-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7f898-110">Properties</span></span>

<span data-ttu-id="7f898-111">O objeto **recordlist** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7f898-111">The **RecordList** object has these properties.</span></span>



| <span data-ttu-id="7f898-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7f898-112">Property</span></span>                                     | <span data-ttu-id="7f898-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f898-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="7f898-114">**Contar**</span><span class="sxs-lookup"><span data-stu-id="7f898-114">**Count**</span></span>](recordlist-count.md)<br/> | <span data-ttu-id="7f898-115">Retorna o número de itens no objeto **recordlist** .</span><span class="sxs-lookup"><span data-stu-id="7f898-115">Returns the number of items in the **RecordList** object.</span></span><br/> |
| [<span data-ttu-id="7f898-116">**Item**</span><span class="sxs-lookup"><span data-stu-id="7f898-116">**Item**</span></span>](recordlist-item.md)<br/>   | <span data-ttu-id="7f898-117">Retorna um registro em uma coleção de objetos **recordlist** .</span><span class="sxs-lookup"><span data-stu-id="7f898-117">Returns a record in a **RecordList** object collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="7f898-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f898-118">Requirements</span></span>



| <span data-ttu-id="7f898-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f898-119">Requirement</span></span> | <span data-ttu-id="7f898-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7f898-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f898-121">Versão</span><span class="sxs-lookup"><span data-stu-id="7f898-121">Version</span></span><br/> | <span data-ttu-id="7f898-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7f898-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7f898-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7f898-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7f898-124">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f898-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7f898-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7f898-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f898-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f898-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7f898-127">IID</span><span class="sxs-lookup"><span data-stu-id="7f898-127">IID</span></span><br/>     | <span data-ttu-id="7f898-128">IID \_ IRecordList é definido como 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7f898-128">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="7f898-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f898-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f898-130">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="7f898-130">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="7f898-131">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7f898-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




