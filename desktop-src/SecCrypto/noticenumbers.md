---
description: Objeto NoticeNumbers – representa uma coleção de objetos de extensão.
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
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090754"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="a4b5c-103">Objeto NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="a4b5c-103">NoticeNumbers object</span></span>

<span data-ttu-id="a4b5c-104">\[O objeto **NoticeNumbers** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4b5c-105">Para obter mais informações, consulte [**qualificador**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="a4b5c-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="a4b5c-106">O objeto **NoticeNumbers** representa uma coleção de objetos de [**extensão**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b5c-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="a4b5c-107">Cada objeto de [**extensão**](extension.md) representa um número de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a4b5c-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="a4b5c-108">When to use</span></span>

<span data-ttu-id="a4b5c-109">O objeto **NoticeNumbers** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="a4b5c-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="a4b5c-110">Recupere o número de objetos de [**extensão**](extension.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="a4b5c-111">Recupere um objeto de [**extensão**](extension.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="a4b5c-112">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="a4b5c-113">Membros</span><span class="sxs-lookup"><span data-stu-id="a4b5c-113">Members</span></span>

<span data-ttu-id="a4b5c-114">O objeto **NoticeNumbers** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a4b5c-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="a4b5c-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a4b5c-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4b5c-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a4b5c-116">Properties</span></span>

<span data-ttu-id="a4b5c-117">O objeto **NoticeNumbers** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="a4b5c-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a4b5c-118">Property</span></span>                                              | <span data-ttu-id="a4b5c-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="a4b5c-119">Access type</span></span>          | <span data-ttu-id="a4b5c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4b5c-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4b5c-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="a4b5c-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="a4b5c-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4b5c-122">Read-only</span></span><br/> | <span data-ttu-id="a4b5c-123">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="a4b5c-124">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a4b5c-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="a4b5c-125">**Contagem**</span><span class="sxs-lookup"><span data-stu-id="a4b5c-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="a4b5c-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4b5c-126">Read-only</span></span><br/> | <span data-ttu-id="a4b5c-127">Recupera o número de objetos de [**extensão**](extension.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="a4b5c-128">**Item**</span><span class="sxs-lookup"><span data-stu-id="a4b5c-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="a4b5c-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4b5c-129">Read-only</span></span><br/> | <span data-ttu-id="a4b5c-130">Recupera o objeto de [**extensão**](extension.md) que representa o número de aviso indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="a4b5c-131">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="a4b5c-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4b5c-132">Remarks</span></span>

<span data-ttu-id="a4b5c-133">O objeto **NoticeNumbers** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="a4b5c-134">O objeto NoticeNumbers é usado na propriedade [**Qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b5c-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b5c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b5c-135">Requirements</span></span>



| <span data-ttu-id="a4b5c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b5c-136">Requirement</span></span> | <span data-ttu-id="a4b5c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a4b5c-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b5c-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a4b5c-138">Redistributable</span></span><br/> | <span data-ttu-id="a4b5c-139">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4b5c-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a4b5c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b5c-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="a4b5c-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5c-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
