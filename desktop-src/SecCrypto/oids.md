---
description: Representa uma coleção de objetos OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Objeto OIDs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770451"
---
# <a name="oids-object"></a><span data-ttu-id="63184-103">Objeto OIDs</span><span class="sxs-lookup"><span data-stu-id="63184-103">OIDs object</span></span>

<span data-ttu-id="63184-104">\[O objeto **OIDs** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="63184-104">\[The **OIDs** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="63184-105">Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="63184-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="63184-106">O objeto **OIDs** representa uma coleção de objetos [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="63184-106">The **OIDs** object represents a collection of [**OID**](oid.md) objects.</span></span> <span data-ttu-id="63184-107">Cada objeto de [**OID**](oid.md) representa um único identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="63184-107">Each [**OID**](oid.md) object represents a single object identifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="63184-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="63184-108">When to use</span></span>

<span data-ttu-id="63184-109">O objeto **OIDs** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="63184-109">The **OIDs** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="63184-110">Adicionar ou remover um objeto [**OID**](oid.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-110">Add or remove an [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="63184-111">Limpe todos os objetos [**OID**](oid.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-111">Clear all the [**OID**](oid.md) objects from the collection.</span></span>
-   <span data-ttu-id="63184-112">Recupere o número de identificadores de objeto na coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-112">Retrieve the number of object identifiers in the collection.</span></span>
-   <span data-ttu-id="63184-113">Recupere um objeto [**OID**](oid.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-113">Retrieve a specific [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="63184-114">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="63184-115">Membros</span><span class="sxs-lookup"><span data-stu-id="63184-115">Members</span></span>

<span data-ttu-id="63184-116">O objeto **OIDs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="63184-116">The **OIDs** object has these types of members:</span></span>

-   [<span data-ttu-id="63184-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="63184-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="63184-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63184-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63184-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="63184-119">Methods</span></span>

<span data-ttu-id="63184-120">O objeto **OIDs** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="63184-120">The **OIDs** object has these methods.</span></span>



| <span data-ttu-id="63184-121">Método</span><span class="sxs-lookup"><span data-stu-id="63184-121">Method</span></span>                        | <span data-ttu-id="63184-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="63184-122">Description</span></span>                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="63184-123">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="63184-123">**Add**</span></span>](oids-add.md)       | <span data-ttu-id="63184-124">Adiciona um objeto [**OID**](oid.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-124">Adds an [**OID**](oid.md) object to the collection.</span></span><br/>              |
| [<span data-ttu-id="63184-125">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="63184-125">**Clear**</span></span>](oids-clear.md)   | <span data-ttu-id="63184-126">Limpa todos os objetos [**OID**](oid.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-126">Clears all [**OID**](oid.md) objects from the collection.</span></span><br/>        |
| [<span data-ttu-id="63184-127">**Remover**</span><span class="sxs-lookup"><span data-stu-id="63184-127">**Remove**</span></span>](oids-remove.md) | <span data-ttu-id="63184-128">Remove um objeto [**OID**](oid.md) indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-128">Removes an indexed [**OID**](oid.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="63184-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63184-129">Properties</span></span>

<span data-ttu-id="63184-130">O objeto **OIDs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="63184-130">The **OIDs** object has these properties.</span></span>



| <span data-ttu-id="63184-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="63184-131">Property</span></span>                                     | <span data-ttu-id="63184-132">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="63184-132">Access type</span></span>          | <span data-ttu-id="63184-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="63184-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63184-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="63184-134">**\_NewEnum**</span></span>](oids-newenum.md)<br/> | <span data-ttu-id="63184-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63184-135">Read-only</span></span><br/> | <span data-ttu-id="63184-136">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="63184-137">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="63184-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="63184-138">**Contar**</span><span class="sxs-lookup"><span data-stu-id="63184-138">**Count**</span></span>](oids-count.md)<br/>       | <span data-ttu-id="63184-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63184-139">Read-only</span></span><br/> | <span data-ttu-id="63184-140">Recupera o número de objetos [**OID**](oid.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-140">Retrieves the number of [**OID**](oid.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="63184-141">**Item**</span><span class="sxs-lookup"><span data-stu-id="63184-141">**Item**</span></span>](oids-item.md)<br/>         | <span data-ttu-id="63184-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63184-142">Read-only</span></span><br/> | <span data-ttu-id="63184-143">Recupera um objeto [**OID**](oid.md) indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="63184-143">Retrieves an indexed [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="63184-144">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="63184-144">This is the default property.</span></span><br/>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="63184-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="63184-145">Remarks</span></span>

<span data-ttu-id="63184-146">Não é possível criar o objeto **OIDs** .</span><span class="sxs-lookup"><span data-stu-id="63184-146">The **OIDs** object cannot be created.</span></span>

<span data-ttu-id="63184-147">O objeto **OIDs** é usado pelas seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="63184-147">The **OIDs** object is used by the following properties:</span></span>

-   [<span data-ttu-id="63184-148">**CertificateStatus.ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="63184-148">**CertificateStatus.ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md)
-   [<span data-ttu-id="63184-149">**CertificateStatus.CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="63184-149">**CertificateStatus.CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a><span data-ttu-id="63184-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63184-150">Requirements</span></span>



| <span data-ttu-id="63184-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="63184-151">Requirement</span></span> | <span data-ttu-id="63184-152">Valor</span><span class="sxs-lookup"><span data-stu-id="63184-152">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63184-153">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="63184-153">Redistributable</span></span><br/> | <span data-ttu-id="63184-154">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="63184-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="63184-155">DLL</span><span class="sxs-lookup"><span data-stu-id="63184-155">DLL</span></span><br/>             | <dl> <span data-ttu-id="63184-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63184-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
