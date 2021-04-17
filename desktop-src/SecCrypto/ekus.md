---
description: Representa uma coleção de objetos EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Objeto EKUs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755052"
---
# <a name="ekus-object"></a><span data-ttu-id="151a6-103">Objeto EKUs</span><span class="sxs-lookup"><span data-stu-id="151a6-103">EKUs object</span></span>

<span data-ttu-id="151a6-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="151a6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="151a6-105">Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="151a6-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="151a6-106">O objeto **EKUs** representa uma coleção de objetos [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="151a6-106">The **EKUs** object represents a collection of [**EKU**](eku.md) objects.</span></span> <span data-ttu-id="151a6-107">Cada objeto [**EKU**](eku.md) representa uma única propriedade EKU (uso estendido de chave) de um certificado.</span><span class="sxs-lookup"><span data-stu-id="151a6-107">Each [**EKU**](eku.md) object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="151a6-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="151a6-108">When to use</span></span>

<span data-ttu-id="151a6-109">A coleção **EKUs** é usada para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="151a6-109">The **EKUs** collection is used to perform the following tasks:</span></span>

-   <span data-ttu-id="151a6-110">Recupere o número de propriedades EKU na coleção.</span><span class="sxs-lookup"><span data-stu-id="151a6-110">Retrieve the number of EKU properties in the collection.</span></span>
-   <span data-ttu-id="151a6-111">Recupere um objeto [**EKU**](eku.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="151a6-111">Retrieve a specific [**EKU**](eku.md) object from the collection.</span></span>
-   <span data-ttu-id="151a6-112">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="151a6-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="151a6-113">Membros</span><span class="sxs-lookup"><span data-stu-id="151a6-113">Members</span></span>

<span data-ttu-id="151a6-114">O objeto **EKUs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="151a6-114">The **EKUs** object has these types of members:</span></span>

-   [<span data-ttu-id="151a6-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="151a6-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="151a6-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="151a6-116">Properties</span></span>

<span data-ttu-id="151a6-117">O objeto **EKUs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="151a6-117">The **EKUs** object has these properties.</span></span>



| <span data-ttu-id="151a6-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="151a6-118">Property</span></span>                                     | <span data-ttu-id="151a6-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="151a6-119">Access type</span></span>          | <span data-ttu-id="151a6-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="151a6-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="151a6-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="151a6-121">**\_NewEnum**</span></span>](ekus-newenum.md)<br/> | <span data-ttu-id="151a6-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="151a6-122">Read-only</span></span><br/> | <span data-ttu-id="151a6-123">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="151a6-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="151a6-124">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="151a6-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="151a6-125">**Contar**</span><span class="sxs-lookup"><span data-stu-id="151a6-125">**Count**</span></span>](ekus-count.md)<br/>       | <span data-ttu-id="151a6-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="151a6-126">Read-only</span></span><br/> | <span data-ttu-id="151a6-127">Recupera o número de objetos [**EKU**](eku.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="151a6-127">Retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="151a6-128">**Item**</span><span class="sxs-lookup"><span data-stu-id="151a6-128">**Item**</span></span>](ekus-item.md)<br/>         | <span data-ttu-id="151a6-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="151a6-129">Read-only</span></span><br/> | <span data-ttu-id="151a6-130">Recupera o objeto [**EKU**](eku.md) que representa a propriedade EKU indexada.</span><span class="sxs-lookup"><span data-stu-id="151a6-130">Retrieves the [**EKU**](eku.md) object that represents the indexed EKU property.</span></span> <span data-ttu-id="151a6-131">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="151a6-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="151a6-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="151a6-132">Remarks</span></span>

<span data-ttu-id="151a6-133">Essa coleção é recuperada pela propriedade [**ExtendedKeyUsage. EKUs**](extendedkeyusage-ekus.md) .</span><span class="sxs-lookup"><span data-stu-id="151a6-133">This collection is retrieved by the [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) property.</span></span>

<span data-ttu-id="151a6-134">O objeto **EKUs** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="151a6-134">The **EKUs** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="151a6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="151a6-135">Requirements</span></span>



| <span data-ttu-id="151a6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="151a6-136">Requirement</span></span> | <span data-ttu-id="151a6-137">Valor</span><span class="sxs-lookup"><span data-stu-id="151a6-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="151a6-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="151a6-138">End of client support</span></span><br/> | <span data-ttu-id="151a6-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="151a6-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="151a6-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="151a6-140">End of server support</span></span><br/> | <span data-ttu-id="151a6-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="151a6-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="151a6-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="151a6-142">Redistributable</span></span><br/>       | <span data-ttu-id="151a6-143">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="151a6-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="151a6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="151a6-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="151a6-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="151a6-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
