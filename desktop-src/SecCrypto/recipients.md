---
description: Objeto de destinatários – representa uma coleção de objetos de certificado.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Objeto de destinatários
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0f0f6474c6ed8883eb591591eff387fe387f7d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103734"
---
# <a name="recipients-object"></a><span data-ttu-id="f49f6-103">Objeto de destinatários</span><span class="sxs-lookup"><span data-stu-id="f49f6-103">Recipients object</span></span>

<span data-ttu-id="f49f6-104">\[O objeto **Recipients** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f49f6-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f49f6-105">Em vez disso, use a [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="f49f6-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f49f6-106">O objeto de **destinatários** representa uma coleção de objetos de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="f49f6-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="f49f6-107">Cada objeto representa um destinatário pretendido da mensagem envelopada.</span><span class="sxs-lookup"><span data-stu-id="f49f6-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="f49f6-108">Os dados em um objeto [**EnvelopedData**](envelopeddata.md) são criptografados com uma chave de sessão [*simétrica*](../secgloss/s-gly.md) e essa chave de sessão simétrica é criptografada para cada destinatário usando a chave pública do certificado do destinatário desejado.</span><span class="sxs-lookup"><span data-stu-id="f49f6-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="f49f6-109">Um destinatário com acesso à [*chave privada*](../secgloss/p-gly.md) associada à [*chave pública*](../secgloss/p-gly.md) de um certificado pode descriptografar a [*chave de sessão*](../secgloss/s-gly.md) e usar a chave de sessão descriptografada para descriptografar os dados reais.</span><span class="sxs-lookup"><span data-stu-id="f49f6-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f49f6-110">Quando usar</span><span class="sxs-lookup"><span data-stu-id="f49f6-110">When to use</span></span>

<span data-ttu-id="f49f6-111">O objeto **Recipients** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f49f6-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="f49f6-112">Adicionar ou remover um objeto de [**certificado**](certificate.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="f49f6-113">Recupere o número de certificados na coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="f49f6-114">Recupere um objeto de **destinatários** específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="f49f6-115">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="f49f6-116">Membros</span><span class="sxs-lookup"><span data-stu-id="f49f6-116">Members</span></span>

<span data-ttu-id="f49f6-117">O objeto de **destinatários** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f49f6-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="f49f6-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="f49f6-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="f49f6-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f49f6-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f49f6-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="f49f6-120">Methods</span></span>

<span data-ttu-id="f49f6-121">O objeto **Recipients** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f49f6-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="f49f6-122">Método</span><span class="sxs-lookup"><span data-stu-id="f49f6-122">Method</span></span>                              | <span data-ttu-id="f49f6-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f49f6-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="f49f6-124">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="f49f6-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="f49f6-125">Adiciona um objeto de [**certificado**](certificate.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="f49f6-126">**Limpar**</span><span class="sxs-lookup"><span data-stu-id="f49f6-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="f49f6-127">Remove todos os objetos de [**certificado**](certificate.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="f49f6-128">**Remover**</span><span class="sxs-lookup"><span data-stu-id="f49f6-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="f49f6-129">Remove um objeto de [**certificado**](certificate.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="f49f6-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f49f6-130">Properties</span></span>

<span data-ttu-id="f49f6-131">O objeto **Recipients** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f49f6-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="f49f6-132">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f49f6-132">Property</span></span>                                           | <span data-ttu-id="f49f6-133">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f49f6-133">Access type</span></span>          | <span data-ttu-id="f49f6-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="f49f6-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f49f6-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="f49f6-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="f49f6-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f49f6-136">Read-only</span></span><br/> | <span data-ttu-id="f49f6-137">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="f49f6-138">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="f49f6-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="f49f6-139">**Contagem**</span><span class="sxs-lookup"><span data-stu-id="f49f6-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="f49f6-140">O número de objetos na coleção de **destinatários** .</span><span class="sxs-lookup"><span data-stu-id="f49f6-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="f49f6-141">**Item**</span><span class="sxs-lookup"><span data-stu-id="f49f6-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="f49f6-142">Um objeto indexado na coleção.</span><span class="sxs-lookup"><span data-stu-id="f49f6-142">An indexed object in the collection.</span></span> <span data-ttu-id="f49f6-143">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="f49f6-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="f49f6-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="f49f6-144">Remarks</span></span>

<span data-ttu-id="f49f6-145">Não é possível criar o objeto de **destinatários** .</span><span class="sxs-lookup"><span data-stu-id="f49f6-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="f49f6-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f49f6-146">Requirements</span></span>



| <span data-ttu-id="f49f6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f49f6-147">Requirement</span></span> | <span data-ttu-id="f49f6-148">Valor</span><span class="sxs-lookup"><span data-stu-id="f49f6-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f49f6-149">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f49f6-149">Redistributable</span></span><br/> | <span data-ttu-id="f49f6-150">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f49f6-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f49f6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f49f6-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="f49f6-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f49f6-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f49f6-153">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f49f6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f49f6-154">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="f49f6-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
