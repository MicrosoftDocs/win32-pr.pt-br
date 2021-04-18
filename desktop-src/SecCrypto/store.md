---
description: Fornece propriedades e métodos que você pode usar para escolher, gerenciar e usar repositórios de certificados e os certificados nesses armazenamentos.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Armazenar objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750493"
---
# <a name="store-object"></a><span data-ttu-id="09bde-103">Armazenar objeto</span><span class="sxs-lookup"><span data-stu-id="09bde-103">Store object</span></span>

<span data-ttu-id="09bde-104">\[O objeto **Store** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="09bde-104">\[The **Store** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09bde-105">Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="09bde-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="09bde-106">O objeto **Store** fornece propriedades e métodos que você pode usar para escolher, gerenciar e usar [*repositórios de certificados*](../secgloss/c-gly.md) e os certificados nesses armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="09bde-106">The **Store** object provides properties and methods that you can use to choose, manage, and use [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="09bde-107">O CAPICOM pode usar armazenamentos de usuário, máquina local, memória e Active Directory atuais.</span><span class="sxs-lookup"><span data-stu-id="09bde-107">CAPICOM can use Current-User, Local-Machine, memory, and Active Directory stores.</span></span> <span data-ttu-id="09bde-108">Além disso, os repositórios oferecem suporte a repositórios de certificados baseados em cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="09bde-108">Also, stores support smart card–based certificate stores.</span></span> <span data-ttu-id="09bde-109">Os desenvolvedores devem estar cientes de que alguns métodos podem falhar com algumas lojas se forem tentadas operações para as quais o usuário não tem direitos.</span><span class="sxs-lookup"><span data-stu-id="09bde-109">Developers should be aware that some methods may fail with some stores if operations are attempted for which the user does not have rights.</span></span>

## <a name="members"></a><span data-ttu-id="09bde-110">Membros</span><span class="sxs-lookup"><span data-stu-id="09bde-110">Members</span></span>

<span data-ttu-id="09bde-111">O objeto **Store** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="09bde-111">The **Store** object has these types of members:</span></span>

-   [<span data-ttu-id="09bde-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="09bde-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="09bde-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09bde-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="09bde-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="09bde-114">Methods</span></span>

<span data-ttu-id="09bde-115">O objeto **Store** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="09bde-115">The **Store** object has these methods.</span></span>



| <span data-ttu-id="09bde-116">Método</span><span class="sxs-lookup"><span data-stu-id="09bde-116">Method</span></span>                         | <span data-ttu-id="09bde-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="09bde-117">Description</span></span>                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09bde-118">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="09bde-118">**Add**</span></span>](store-add.md)       | <span data-ttu-id="09bde-119">Adiciona um objeto de [**certificado**](certificate.md) ao repositório de certificados aberto.</span><span class="sxs-lookup"><span data-stu-id="09bde-119">Adds a [**Certificate**](certificate.md) object to the open certificate store.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="09bde-120">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="09bde-120">**Close**</span></span>](store-close.md)   | <span data-ttu-id="09bde-121">Fecha um repositório de certificados aberto.</span><span class="sxs-lookup"><span data-stu-id="09bde-121">Closes an open certificate store.</span></span><br/> <span data-ttu-id="09bde-122">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para o método [**Close**](store-close.md) .</span><span class="sxs-lookup"><span data-stu-id="09bde-122">**CAPICOM 2.0.0.3 and earlier:** The [**Close**](store-close.md) method is not supported.</span></span><br/>                                                               |
| [<span data-ttu-id="09bde-123">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="09bde-123">**Delete**</span></span>](store-delete.md) | <span data-ttu-id="09bde-124">Exclui o repositório de certificados representado pelo objeto de [**armazenamento**](certificate.md) atual.</span><span class="sxs-lookup"><span data-stu-id="09bde-124">Deletes the certificate store represented by the current [**Store**](certificate.md) object.</span></span><br/> <span data-ttu-id="09bde-125">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para o método [**delete**](store-delete.md) .</span><span class="sxs-lookup"><span data-stu-id="09bde-125">**CAPICOM 2.0.0.3 and earlier:** The [**Delete**](store-delete.md) method is not supported.</span></span><br/> |
| [<span data-ttu-id="09bde-126">**Exportação**</span><span class="sxs-lookup"><span data-stu-id="09bde-126">**Export**</span></span>](store-export.md) | <span data-ttu-id="09bde-127">Exporta o repositório de um [*blob*](../secgloss/b-gly.md)codificado.</span><span class="sxs-lookup"><span data-stu-id="09bde-127">Exports the store of an encoded [*BLOB*](../secgloss/b-gly.md).</span></span><br/>                                                                                                       |
| [<span data-ttu-id="09bde-128">**Importar**</span><span class="sxs-lookup"><span data-stu-id="09bde-128">**Import**</span></span>](store-import.md) | <span data-ttu-id="09bde-129">Importa um repositório exportado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="09bde-129">Imports a previously exported store.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="09bde-130">**Carregar**</span><span class="sxs-lookup"><span data-stu-id="09bde-130">**Load**</span></span>](store-load.md)     | <span data-ttu-id="09bde-131">Importa objetos de [**certificado**](certificate.md) de um arquivo para o repositório.</span><span class="sxs-lookup"><span data-stu-id="09bde-131">Imports [**Certificate**](certificate.md) objects from a file into the store.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="09bde-132">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="09bde-132">**Open**</span></span>](store-open.md)     | <span data-ttu-id="09bde-133">Abre um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="09bde-133">Opens a certificate store.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="09bde-134">**Remover**</span><span class="sxs-lookup"><span data-stu-id="09bde-134">**Remove**</span></span>](store-remove.md) | <span data-ttu-id="09bde-135">Remove um objeto de [**certificado**](certificate.md) de um armazenamento aberto.</span><span class="sxs-lookup"><span data-stu-id="09bde-135">Removes a [**Certificate**](certificate.md) object from an open store.</span></span><br/>                                                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="09bde-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09bde-136">Properties</span></span>

<span data-ttu-id="09bde-137">O objeto **Store** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="09bde-137">The **Store** object has these properties.</span></span>



| <span data-ttu-id="09bde-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="09bde-138">Property</span></span>                                              | <span data-ttu-id="09bde-139">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="09bde-139">Access type</span></span>          | <span data-ttu-id="09bde-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="09bde-140">Description</span></span>                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09bde-141">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="09bde-141">**Certificates**</span></span>](store-certificates.md)<br/> | <span data-ttu-id="09bde-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09bde-142">Read-only</span></span><br/> | <span data-ttu-id="09bde-143">Recupera a coleção de [**certificados**](certificates.md) do repositório.</span><span class="sxs-lookup"><span data-stu-id="09bde-143">Retrieves the [**Certificates**](certificates.md) collection of the store.</span></span> <span data-ttu-id="09bde-144">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="09bde-144">This is the default property.</span></span><br/>                                                                                  |
| [<span data-ttu-id="09bde-145">**Local**</span><span class="sxs-lookup"><span data-stu-id="09bde-145">**Location**</span></span>](store-location.md)<br/>         | <span data-ttu-id="09bde-146">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09bde-146">Read-only</span></span><br/> | <span data-ttu-id="09bde-147">Recupera o local do repositório de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="09bde-147">Retrieves the location of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="09bde-148">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para a propriedade [**Location**](store-location.md) .</span><span class="sxs-lookup"><span data-stu-id="09bde-148">**CAPICOM 2.0.0.3 and earlier:** The [**Location**](store-location.md) property is not supported.</span></span><br/> |
| [<span data-ttu-id="09bde-149">**Nome**</span><span class="sxs-lookup"><span data-stu-id="09bde-149">**Name**</span></span>](store-name.md)<br/>                 | <span data-ttu-id="09bde-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09bde-150">Read-only</span></span><br/> | <span data-ttu-id="09bde-151">Recupera o nome do repositório de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="09bde-151">Retrieves the name of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="09bde-152">**CAPICOM 2.0.0.3 e anteriores:** Não há suporte para a propriedade [**Name**](store-name.md) .</span><span class="sxs-lookup"><span data-stu-id="09bde-152">**CAPICOM 2.0.0.3 and earlier:** The [**Name**](store-name.md) property is not supported.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="09bde-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="09bde-153">Remarks</span></span>

<span data-ttu-id="09bde-154">O objeto **Store** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="09bde-154">The **Store** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="09bde-155">O ProgID do objeto de **armazenamento** é CAPICOM. Store. 2.</span><span class="sxs-lookup"><span data-stu-id="09bde-155">The ProgID for the **Store** object is CAPICOM.Store.2.</span></span>

<span data-ttu-id="09bde-156">**CAPICOM 1. *x*:** o ProgID do objeto da **loja** é CAPICOM. Store. 1.</span><span class="sxs-lookup"><span data-stu-id="09bde-156">**CAPICOM 1.*x*:** The ProgID for the **Store** object is CAPICOM.Store.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="09bde-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09bde-157">Requirements</span></span>



| <span data-ttu-id="09bde-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="09bde-158">Requirement</span></span> | <span data-ttu-id="09bde-159">Valor</span><span class="sxs-lookup"><span data-stu-id="09bde-159">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09bde-160">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="09bde-160">Redistributable</span></span><br/> | <span data-ttu-id="09bde-161">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="09bde-161">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="09bde-162">DLL</span><span class="sxs-lookup"><span data-stu-id="09bde-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="09bde-163"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09bde-163"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09bde-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="09bde-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09bde-165">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="09bde-165">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
