---
description: Uma coleção de objetos PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Objeto CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784154"
---
# <a name="certificatepolicies-object"></a><span data-ttu-id="315e5-103">Objeto CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="315e5-103">CertificatePolicies object</span></span>

<span data-ttu-id="315e5-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="315e5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="315e5-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para as políticas de certificado para recuperar as políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="315e5-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="315e5-106">O objeto **CertificatePolicies** representa uma coleção de objetos [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="315e5-106">The **CertificatePolicies** object represents a collection of [**PolicyInformation**](policyinformation.md) objects.</span></span> <span data-ttu-id="315e5-107">Cada objeto [**PolicyInformation**](policyinformation.md) representa uma única política de certificado.</span><span class="sxs-lookup"><span data-stu-id="315e5-107">Each [**PolicyInformation**](policyinformation.md) object represents a single certificate policy.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="315e5-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="315e5-108">When to use</span></span>

<span data-ttu-id="315e5-109">O objeto **CertificatePolicies** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="315e5-109">The **CertificatePolicies** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="315e5-110">Recupere o número de políticas de certificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="315e5-110">Retrieve the number of certificate policies in the collection.</span></span>
-   <span data-ttu-id="315e5-111">Recupere um objeto [**PolicyInformation**](policyinformation.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="315e5-111">Retrieve a specific [**PolicyInformation**](policyinformation.md) object from the collection.</span></span>
-   <span data-ttu-id="315e5-112">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="315e5-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="315e5-113">Membros</span><span class="sxs-lookup"><span data-stu-id="315e5-113">Members</span></span>

<span data-ttu-id="315e5-114">O objeto **CertificatePolicies** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="315e5-114">The **CertificatePolicies** object has these types of members:</span></span>

-   [<span data-ttu-id="315e5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="315e5-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="315e5-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="315e5-116">Properties</span></span>

<span data-ttu-id="315e5-117">O objeto **CertificatePolicies** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="315e5-117">The **CertificatePolicies** object has these properties.</span></span>



| <span data-ttu-id="315e5-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="315e5-118">Property</span></span>                                                    | <span data-ttu-id="315e5-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="315e5-119">Access type</span></span>          | <span data-ttu-id="315e5-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="315e5-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="315e5-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="315e5-121">**\_NewEnum**</span></span>](certificatepolicies-newenum.md)<br/> | <span data-ttu-id="315e5-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="315e5-122">Read-only</span></span><br/> | <span data-ttu-id="315e5-123">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="315e5-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="315e5-124">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="315e5-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="315e5-125">**Contar**</span><span class="sxs-lookup"><span data-stu-id="315e5-125">**Count**</span></span>](certificatepolicies-count.md)<br/>       | <span data-ttu-id="315e5-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="315e5-126">Read-only</span></span><br/> | <span data-ttu-id="315e5-127">Recupera o número de objetos [**PolicyInformation**](policyinformation.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="315e5-127">Retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="315e5-128">**Item**</span><span class="sxs-lookup"><span data-stu-id="315e5-128">**Item**</span></span>](certificatepolicies-item.md)<br/>         | <span data-ttu-id="315e5-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="315e5-129">Read-only</span></span><br/> | <span data-ttu-id="315e5-130">Recupera um objeto [**PolicyInformation**](policyinformation.md) que representa a política de certificado indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="315e5-130">Retrieves a [**PolicyInformation**](policyinformation.md) object that represents the indexed certificate policy of the collection.</span></span> <span data-ttu-id="315e5-131">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="315e5-131">This is the default property.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="315e5-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="315e5-132">Remarks</span></span>

<span data-ttu-id="315e5-133">O objeto **CertificatePolicies** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="315e5-133">The **CertificatePolicies** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="315e5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="315e5-134">Requirements</span></span>



| <span data-ttu-id="315e5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="315e5-135">Requirement</span></span> | <span data-ttu-id="315e5-136">Valor</span><span class="sxs-lookup"><span data-stu-id="315e5-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="315e5-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="315e5-137">End of client support</span></span><br/> | <span data-ttu-id="315e5-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="315e5-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="315e5-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="315e5-139">End of server support</span></span><br/> | <span data-ttu-id="315e5-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="315e5-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="315e5-141">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="315e5-141">Redistributable</span></span><br/>       | <span data-ttu-id="315e5-142">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="315e5-142">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="315e5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="315e5-143">DLL</span></span><br/>                   | <dl> <span data-ttu-id="315e5-144"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315e5-144"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
