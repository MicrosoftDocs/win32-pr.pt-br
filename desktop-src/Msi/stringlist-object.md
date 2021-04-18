---
description: O objeto StringList é uma coleção de cadeias de caracteres. O cliente deve verificar se o objeto StringList existe e não está vazio antes de fazer referência a suas propriedades.
ms.assetid: 7021320a-d01a-43e8-90a5-6105a11a4613
title: Objeto StringList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6493b9e1723d46ce290c7472bbcee7eb9ec34725
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785424"
---
# <a name="stringlist-object"></a><span data-ttu-id="bfd44-104">Objeto StringList</span><span class="sxs-lookup"><span data-stu-id="bfd44-104">StringList object</span></span>

<span data-ttu-id="bfd44-105">O objeto **StringList** é uma coleção de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bfd44-105">The **StringList** object is a collection of strings.</span></span> <span data-ttu-id="bfd44-106">O cliente deve verificar se o objeto **StringList** existe e não está vazio antes de fazer referência a suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bfd44-106">The client must verify that the **StringList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="bfd44-107">Membros</span><span class="sxs-lookup"><span data-stu-id="bfd44-107">Members</span></span>

<span data-ttu-id="bfd44-108">O objeto **StringList** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bfd44-108">The **StringList** object has these types of members:</span></span>

-   [<span data-ttu-id="bfd44-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bfd44-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfd44-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bfd44-110">Properties</span></span>

<span data-ttu-id="bfd44-111">O objeto **StringList** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bfd44-111">The **StringList** object has these properties.</span></span>



| <span data-ttu-id="bfd44-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bfd44-112">Property</span></span>                                     | <span data-ttu-id="bfd44-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfd44-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="bfd44-114">**Contar**</span><span class="sxs-lookup"><span data-stu-id="bfd44-114">**Count**</span></span>](stringlist-count.md)<br/> | <span data-ttu-id="bfd44-115">Retorna o número de itens no objeto **StringList** .</span><span class="sxs-lookup"><span data-stu-id="bfd44-115">Returns the number of items in the **StringList** object.</span></span><br/> |
| [<span data-ttu-id="bfd44-116">**Item**</span><span class="sxs-lookup"><span data-stu-id="bfd44-116">**Item**</span></span>](stringlist-item.md)<br/>   | <span data-ttu-id="bfd44-117">Retorna uma cadeia de caracteres na coleção de objetos **StringList** .</span><span class="sxs-lookup"><span data-stu-id="bfd44-117">Returns a string in the **StringList** object collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bfd44-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfd44-118">Requirements</span></span>



| <span data-ttu-id="bfd44-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd44-119">Requirement</span></span> | <span data-ttu-id="bfd44-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bfd44-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd44-121">Versão</span><span class="sxs-lookup"><span data-stu-id="bfd44-121">Version</span></span><br/> | <span data-ttu-id="bfd44-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bfd44-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bfd44-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bfd44-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bfd44-124">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="bfd44-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bfd44-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bfd44-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="bfd44-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd44-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bfd44-127">IID</span><span class="sxs-lookup"><span data-stu-id="bfd44-127">IID</span></span><br/>     | <span data-ttu-id="bfd44-128">IID \_ isastringlist é definida como 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bfd44-128">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="bfd44-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfd44-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd44-130">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="bfd44-130">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




