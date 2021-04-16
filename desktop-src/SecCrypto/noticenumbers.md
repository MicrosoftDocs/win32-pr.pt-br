---
description: Representa uma coleção de objetos de extensão.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Objeto NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779356"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="e2ab4-103">Objeto NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="e2ab4-103">NoticeNumbers object</span></span>

<span data-ttu-id="e2ab4-104">\[O objeto **NoticeNumbers** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e2ab4-105">Para obter mais informações, consulte [**qualificador**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="e2ab4-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="e2ab4-106">O objeto **NoticeNumbers** representa uma coleção de objetos de [**extensão**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="e2ab4-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="e2ab4-107">Cada objeto de [**extensão**](extension.md) representa um número de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e2ab4-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="e2ab4-108">When to use</span></span>

<span data-ttu-id="e2ab4-109">O objeto **NoticeNumbers** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="e2ab4-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e2ab4-110">Recupere o número de objetos de [**extensão**](extension.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="e2ab4-111">Recupere um objeto de [**extensão**](extension.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="e2ab4-112">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="e2ab4-113">Membros</span><span class="sxs-lookup"><span data-stu-id="e2ab4-113">Members</span></span>

<span data-ttu-id="e2ab4-114">O objeto **NoticeNumbers** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2ab4-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="e2ab4-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2ab4-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2ab4-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2ab4-116">Properties</span></span>

<span data-ttu-id="e2ab4-117">O objeto **NoticeNumbers** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="e2ab4-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e2ab4-118">Property</span></span>                                              | <span data-ttu-id="e2ab4-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="e2ab4-119">Access type</span></span>          | <span data-ttu-id="e2ab4-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2ab4-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2ab4-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e2ab4-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="e2ab4-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ab4-122">Read-only</span></span><br/> | <span data-ttu-id="e2ab4-123">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e2ab4-124">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e2ab4-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="e2ab4-125">**Contar**</span><span class="sxs-lookup"><span data-stu-id="e2ab4-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="e2ab4-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ab4-126">Read-only</span></span><br/> | <span data-ttu-id="e2ab4-127">Recupera o número de objetos de [**extensão**](extension.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="e2ab4-128">**Item**</span><span class="sxs-lookup"><span data-stu-id="e2ab4-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="e2ab4-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2ab4-129">Read-only</span></span><br/> | <span data-ttu-id="e2ab4-130">Recupera o objeto de [**extensão**](extension.md) que representa o número de aviso indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="e2ab4-131">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="e2ab4-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2ab4-132">Remarks</span></span>

<span data-ttu-id="e2ab4-133">O objeto **NoticeNumbers** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="e2ab4-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="e2ab4-134">O objeto NoticeNumbers é usado na propriedade [**Qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .</span><span class="sxs-lookup"><span data-stu-id="e2ab4-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ab4-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2ab4-135">Requirements</span></span>



| <span data-ttu-id="e2ab4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2ab4-136">Requirement</span></span> | <span data-ttu-id="e2ab4-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e2ab4-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ab4-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e2ab4-138">Redistributable</span></span><br/> | <span data-ttu-id="e2ab4-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2ab4-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e2ab4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e2ab4-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="e2ab4-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2ab4-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
