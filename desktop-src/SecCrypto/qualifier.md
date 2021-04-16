---
description: Representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Objeto de qualificador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752531"
---
# <a name="qualifier-object"></a><span data-ttu-id="478fd-103">Objeto de qualificador</span><span class="sxs-lookup"><span data-stu-id="478fd-103">Qualifier object</span></span>

<span data-ttu-id="478fd-104">\[O objeto de **qualificador** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="478fd-104">\[The **Qualifier** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="478fd-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="478fd-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="478fd-106">O objeto de **qualificador** representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="478fd-106">The **Qualifier** object represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="478fd-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="478fd-107">When to use</span></span>

<span data-ttu-id="478fd-108">O objeto de **qualificador** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="478fd-108">The **Qualifier** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="478fd-109">Recupere o identificador de objeto do qualificador.</span><span class="sxs-lookup"><span data-stu-id="478fd-109">Retrieve the object identifier of the qualifier.</span></span>
-   <span data-ttu-id="478fd-110">Recupere o Uniform Resource Identifier (URI) que aponta para um CPS publicado pela [*autoridade de certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="478fd-110">Retrieve the Uniform Resource Identifier (URI) that points to a CPS published by the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="478fd-111">Recupere o nome da organização associada ao qualificador.</span><span class="sxs-lookup"><span data-stu-id="478fd-111">Retrieve the name of the organization associated with the qualifier.</span></span>
-   <span data-ttu-id="478fd-112">Recupere o nome e o conteúdo de um aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="478fd-112">Retrieve the name and content of a user notice.</span></span>

## <a name="members"></a><span data-ttu-id="478fd-113">Membros</span><span class="sxs-lookup"><span data-stu-id="478fd-113">Members</span></span>

<span data-ttu-id="478fd-114">O objeto de **qualificador** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="478fd-114">The **Qualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="478fd-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="478fd-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="478fd-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="478fd-116">Properties</span></span>

<span data-ttu-id="478fd-117">O objeto de **qualificador** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="478fd-117">The **Qualifier** object has these properties.</span></span>



| <span data-ttu-id="478fd-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="478fd-118">Property</span></span>                                                          | <span data-ttu-id="478fd-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="478fd-119">Access type</span></span>          | <span data-ttu-id="478fd-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="478fd-120">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="478fd-121">**CPSPointer**</span><span class="sxs-lookup"><span data-stu-id="478fd-121">**CPSPointer**</span></span>](qualifier-cpspointer.md)<br/>             | <span data-ttu-id="478fd-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="478fd-122">Read-only</span></span><br/> | <span data-ttu-id="478fd-123">Recupera uma cadeia de caracteres que contém o URI que aponta para um CPS publicado pela autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="478fd-123">Retrieves a string that contains the URI that points to a CPS published by the CA.</span></span><br/>                                       |
| [<span data-ttu-id="478fd-124">**ExplicitText**</span><span class="sxs-lookup"><span data-stu-id="478fd-124">**ExplicitText**</span></span>](qualifier-explicittext.md)<br/>         | <span data-ttu-id="478fd-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="478fd-125">Read-only</span></span><br/> | <span data-ttu-id="478fd-126">Recupera uma cadeia de caracteres que contém o conteúdo do aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="478fd-126">Retrieves a string that contains the content of the user notice.</span></span> <span data-ttu-id="478fd-127">Esta propriedade pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="478fd-127">This property may be empty.</span></span><br/>                             |
| [<span data-ttu-id="478fd-128">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="478fd-128">**NoticeNumbers**</span></span>](qualifier-noticenumbers.md)<br/>       | <span data-ttu-id="478fd-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="478fd-129">Read-only</span></span><br/> | <span data-ttu-id="478fd-130">Recupera um objeto **NoticeNumbers** que contém a coleção de números de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="478fd-130">Retrieves a **NoticeNumbers** object that contains the collection of user notice numbers.</span></span> <span data-ttu-id="478fd-131">Esta propriedade pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="478fd-131">This property may be empty.</span></span><br/>    |
| [<span data-ttu-id="478fd-132">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="478fd-132">**OID**</span></span>](qualifier-oid.md)<br/>                           | <span data-ttu-id="478fd-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="478fd-133">Read-only</span></span><br/> | <span data-ttu-id="478fd-134">Recupera um objeto [**OID**](oid.md) que identifica o qualificador.</span><span class="sxs-lookup"><span data-stu-id="478fd-134">Retrieves an [**OID**](oid.md) object that identifies the qualifier.</span></span> <span data-ttu-id="478fd-135">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="478fd-135">This is the default property.</span></span><br/>                      |
| [<span data-ttu-id="478fd-136">**OrganizationName**</span><span class="sxs-lookup"><span data-stu-id="478fd-136">**OrganizationName**</span></span>](qualifier-organizationname.md)<br/> | <span data-ttu-id="478fd-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="478fd-137">Read-only</span></span><br/> | <span data-ttu-id="478fd-138">Recupera uma cadeia de caracteres que contém o nome da organização associada ao qualificador.</span><span class="sxs-lookup"><span data-stu-id="478fd-138">Retrieves a string that contains the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="478fd-139">Esta propriedade pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="478fd-139">This property may be empty.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="478fd-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="478fd-140">Remarks</span></span>

<span data-ttu-id="478fd-141">Não é possível criar o objeto **qualificador** .</span><span class="sxs-lookup"><span data-stu-id="478fd-141">The **Qualifier** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="478fd-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="478fd-142">Requirements</span></span>



| <span data-ttu-id="478fd-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="478fd-143">Requirement</span></span> | <span data-ttu-id="478fd-144">Valor</span><span class="sxs-lookup"><span data-stu-id="478fd-144">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="478fd-145">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="478fd-145">Redistributable</span></span><br/> | <span data-ttu-id="478fd-146">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="478fd-146">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="478fd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="478fd-147">DLL</span></span><br/>             | <dl> <span data-ttu-id="478fd-148"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="478fd-148"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
