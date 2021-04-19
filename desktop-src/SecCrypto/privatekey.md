---
description: Representa a chave privada associada a um certificado.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Objeto PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764615"
---
# <a name="privatekey-object"></a><span data-ttu-id="4df19-103">Objeto PrivateKey</span><span class="sxs-lookup"><span data-stu-id="4df19-103">PrivateKey object</span></span>

<span data-ttu-id="4df19-104">\[O objeto **PrivateKey** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4df19-104">\[The **PrivateKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4df19-105">Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4df19-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4df19-106">O objeto **PrivateKey** representa a [*chave privada*](../secgloss/p-gly.md) associada a um certificado.</span><span class="sxs-lookup"><span data-stu-id="4df19-106">The **PrivateKey** object represents the [*private key*](../secgloss/p-gly.md) associated with a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4df19-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="4df19-107">When to use</span></span>

<span data-ttu-id="4df19-108">O objeto **PrivateKey** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="4df19-108">The **PrivateKey** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4df19-109">Recupere informações sobre a chave privada.</span><span class="sxs-lookup"><span data-stu-id="4df19-109">Retrieve information about the private key.</span></span>
-   <span data-ttu-id="4df19-110">Abra o contêiner de chave privada.</span><span class="sxs-lookup"><span data-stu-id="4df19-110">Open the private key container.</span></span>
-   <span data-ttu-id="4df19-111">Exclua a chave privada.</span><span class="sxs-lookup"><span data-stu-id="4df19-111">Delete the private key.</span></span>

## <a name="members"></a><span data-ttu-id="4df19-112">Membros</span><span class="sxs-lookup"><span data-stu-id="4df19-112">Members</span></span>

<span data-ttu-id="4df19-113">O objeto **PrivateKey** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4df19-113">The **PrivateKey** object has these types of members:</span></span>

-   [<span data-ttu-id="4df19-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="4df19-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="4df19-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4df19-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4df19-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="4df19-116">Methods</span></span>

<span data-ttu-id="4df19-117">O objeto **PrivateKey** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4df19-117">The **PrivateKey** object has these methods.</span></span>



| <span data-ttu-id="4df19-118">Método</span><span class="sxs-lookup"><span data-stu-id="4df19-118">Method</span></span>                                                  | <span data-ttu-id="4df19-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="4df19-119">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4df19-120">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="4df19-120">**Delete**</span></span>](privatekey-delete.md)                     | <span data-ttu-id="4df19-121">Exclui o contêiner de chave privada referenciado pelo objeto **PrivateKey** .</span><span class="sxs-lookup"><span data-stu-id="4df19-121">Deletes the private key container referenced by the **PrivateKey** object.</span></span><br/>                                                                                |
| [<span data-ttu-id="4df19-122">**Isacessível**</span><span class="sxs-lookup"><span data-stu-id="4df19-122">**IsAccessible**</span></span>](privatekey-isaccessible.md)         | <span data-ttu-id="4df19-123">Recupera um valor booliano que indica se a chave privada pode ser acessada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4df19-123">Retrieves a Boolean value that indicates whether the private key is accessible by the user.</span></span> <span data-ttu-id="4df19-124">Se for true, o usuário poderá acessar a chave privada.</span><span class="sxs-lookup"><span data-stu-id="4df19-124">If true, the user can access the private key.</span></span><br/>                 |
| [<span data-ttu-id="4df19-125">**IsExportable**</span><span class="sxs-lookup"><span data-stu-id="4df19-125">**IsExportable**</span></span>](privatekey-isexportable.md)         | <span data-ttu-id="4df19-126">Recupera um valor booliano que indica se a chave privada pode ser exportada.</span><span class="sxs-lookup"><span data-stu-id="4df19-126">Retrieves a Boolean value that indicates whether the private key can be exported.</span></span> <span data-ttu-id="4df19-127">Se for true, a chave privada poderá ser exportada.</span><span class="sxs-lookup"><span data-stu-id="4df19-127">If true, the private key can be exported.</span></span><br/>                               |
| [<span data-ttu-id="4df19-128">**IsHardwareDevice**</span><span class="sxs-lookup"><span data-stu-id="4df19-128">**IsHardwareDevice**</span></span>](privatekey-ishardwaredevice.md) | <span data-ttu-id="4df19-129">Recupera um valor booliano que indica se a chave privada está armazenada em um dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="4df19-129">Retrieves a Boolean value that indicates whether the private key is stored on a hardware device.</span></span> <span data-ttu-id="4df19-130">Se for true, a chave privada será armazenada em um dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="4df19-130">If true, the private key is stored on a hardware device.</span></span><br/> |
| [<span data-ttu-id="4df19-131">**Ismachinekeyset**</span><span class="sxs-lookup"><span data-stu-id="4df19-131">**IsMachineKeyset**</span></span>](privatekey-ismachinekeyset.md)   | <span data-ttu-id="4df19-132">Recupera um valor booliano que indica se a chave privada é uma chave de computador.</span><span class="sxs-lookup"><span data-stu-id="4df19-132">Retrieves a Boolean value that indicates whether the private key is a machine key.</span></span> <span data-ttu-id="4df19-133">Se for true, a chave privada será uma chave de computador.</span><span class="sxs-lookup"><span data-stu-id="4df19-133">If true, the private key is a machine key.</span></span><br/>                             |
| [<span data-ttu-id="4df19-134">**Isprotegeu**</span><span class="sxs-lookup"><span data-stu-id="4df19-134">**IsProtected**</span></span>](privatekey-isprotected.md)           | <span data-ttu-id="4df19-135">Recupera um valor booliano que indica se a chave privada está protegida.</span><span class="sxs-lookup"><span data-stu-id="4df19-135">Retrieves a Boolean value that indicates whether the private key is protected.</span></span> <span data-ttu-id="4df19-136">Se for true, a chave privada será protegida.</span><span class="sxs-lookup"><span data-stu-id="4df19-136">If true, the private key is protected.</span></span><br/>                                     |
| [<span data-ttu-id="4df19-137">**IsRemovable**</span><span class="sxs-lookup"><span data-stu-id="4df19-137">**IsRemovable**</span></span>](privatekey-isremovable.md)           | <span data-ttu-id="4df19-138">Recupera um valor booliano que indica se a chave privada está em um dispositivo removível.</span><span class="sxs-lookup"><span data-stu-id="4df19-138">Retrieves a Boolean value that indicates whether the private key is on a removable device.</span></span> <span data-ttu-id="4df19-139">Se for true, a chave privada estará em um dispositivo removível.</span><span class="sxs-lookup"><span data-stu-id="4df19-139">If true, the private key is on a removable device.</span></span><br/>             |
| [<span data-ttu-id="4df19-140">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="4df19-140">**Open**</span></span>](privatekey-open.md)                         | <span data-ttu-id="4df19-141">Acessa um contêiner de chave existente.</span><span class="sxs-lookup"><span data-stu-id="4df19-141">Accesses an existing key container.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="4df19-142">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4df19-142">Properties</span></span>

<span data-ttu-id="4df19-143">O objeto **PrivateKey** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4df19-143">The **PrivateKey** object has these properties.</span></span>



| <span data-ttu-id="4df19-144">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4df19-144">Property</span></span>                                                                 | <span data-ttu-id="4df19-145">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4df19-145">Access type</span></span>          | <span data-ttu-id="4df19-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="4df19-146">Description</span></span>                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4df19-147">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="4df19-147">**ContainerName**</span></span>](privatekey-containername.md)<br/>             | <span data-ttu-id="4df19-148">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4df19-148">Read-only</span></span><br/> | <span data-ttu-id="4df19-149">Recupera uma cadeia de caracteres que contém o nome do contêiner da chave privada.</span><span class="sxs-lookup"><span data-stu-id="4df19-149">Retrieves a string that contains the private key container name.</span></span> <span data-ttu-id="4df19-150">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="4df19-150">This is the default property.</span></span><br/> |
| [<span data-ttu-id="4df19-151">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="4df19-151">**KeySpec**</span></span>](privatekey-keyspec.md)<br/>                         | <span data-ttu-id="4df19-152">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4df19-152">Read-only</span></span><br/> | <span data-ttu-id="4df19-153">Recupera a especificação de chave.</span><span class="sxs-lookup"><span data-stu-id="4df19-153">Retrieves the key specification.</span></span><br/>                                                               |
| [<span data-ttu-id="4df19-154">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="4df19-154">**ProviderName**</span></span>](privatekey-providername.md)<br/>               | <span data-ttu-id="4df19-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4df19-155">Read-only</span></span><br/> | <span data-ttu-id="4df19-156">Recupera uma cadeia de caracteres que contém o nome do CSP.</span><span class="sxs-lookup"><span data-stu-id="4df19-156">Retrieves a string that contains the name of the CSP.</span></span><br/>                                          |
| [<span data-ttu-id="4df19-157">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="4df19-157">**ProviderType**</span></span>](privatekey-providertype.md)<br/>               | <span data-ttu-id="4df19-158">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4df19-158">Read-only</span></span><br/> | <span data-ttu-id="4df19-159">Recupera um valor de enumeração que especifica o tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="4df19-159">Retrieves an enumeration value that specifies the type of provider.</span></span><br/>                            |
| [<span data-ttu-id="4df19-160">**UniqueContainerName**</span><span class="sxs-lookup"><span data-stu-id="4df19-160">**UniqueContainerName**</span></span>](privatekey-uniquecontainername.md)<br/> | <span data-ttu-id="4df19-161">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4df19-161">Read-only</span></span><br/> | <span data-ttu-id="4df19-162">Recupera uma cadeia de caracteres que contém o nome exclusivo do contêiner de chave privada.</span><span class="sxs-lookup"><span data-stu-id="4df19-162">Retrieves a string that contains the unique private key container name.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4df19-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="4df19-163">Remarks</span></span>

<span data-ttu-id="4df19-164">O objeto **PrivateKey** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="4df19-164">The **PrivateKey** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="4df19-165">O ProgID do objeto **PrivateKey** é CAPICOM. PrivateKey. 1.</span><span class="sxs-lookup"><span data-stu-id="4df19-165">The ProgID for the **PrivateKey** object is CAPICOM.PrivateKey.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df19-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4df19-166">Requirements</span></span>



| <span data-ttu-id="4df19-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df19-167">Requirement</span></span> | <span data-ttu-id="4df19-168">Valor</span><span class="sxs-lookup"><span data-stu-id="4df19-168">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df19-169">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4df19-169">Redistributable</span></span><br/> | <span data-ttu-id="4df19-170">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4df19-170">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4df19-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4df19-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="4df19-172"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4df19-172"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
