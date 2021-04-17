---
description: Representa uma coleção de qualificadores.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Objeto Qualifiers (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784143"
---
# <a name="qualifiers-object"></a><span data-ttu-id="404fd-103">Objeto Qualifiers</span><span class="sxs-lookup"><span data-stu-id="404fd-103">Qualifiers object</span></span>

<span data-ttu-id="404fd-104">\[O objeto **Qualifiers** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="404fd-104">\[The **Qualifiers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="404fd-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="404fd-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="404fd-106">O objeto **Qualifiers** representa uma coleção de qualificadores.</span><span class="sxs-lookup"><span data-stu-id="404fd-106">The **Qualifiers** object represents a collection of qualifiers.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="404fd-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="404fd-107">When to use</span></span>

<span data-ttu-id="404fd-108">O objeto **Qualifiers** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="404fd-108">The **Qualifiers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="404fd-109">Recupere uma propriedade estendida específica da coleção.</span><span class="sxs-lookup"><span data-stu-id="404fd-109">Retrieve a specific extended property from the collection.</span></span>
-   <span data-ttu-id="404fd-110">Recupere o número de propriedades estendidas na coleção.</span><span class="sxs-lookup"><span data-stu-id="404fd-110">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="404fd-111">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="404fd-111">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="404fd-112">Membros</span><span class="sxs-lookup"><span data-stu-id="404fd-112">Members</span></span>

<span data-ttu-id="404fd-113">O objeto **Qualifiers** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="404fd-113">The **Qualifiers** object has these types of members:</span></span>

-   [<span data-ttu-id="404fd-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="404fd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="404fd-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="404fd-115">Properties</span></span>

<span data-ttu-id="404fd-116">O objeto **Qualifiers** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="404fd-116">The **Qualifiers** object has these properties.</span></span>



| <span data-ttu-id="404fd-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="404fd-117">Property</span></span>                                           | <span data-ttu-id="404fd-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="404fd-118">Access type</span></span>          | <span data-ttu-id="404fd-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="404fd-119">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="404fd-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="404fd-120">**\_NewEnum**</span></span>](qualifiers-newenum.md)<br/> | <span data-ttu-id="404fd-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="404fd-121">Read-only</span></span><br/> | <span data-ttu-id="404fd-122">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="404fd-122">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="404fd-123">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="404fd-123">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="404fd-124">**Contar**</span><span class="sxs-lookup"><span data-stu-id="404fd-124">**Count**</span></span>](qualifiers-count.md)<br/>       | <span data-ttu-id="404fd-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="404fd-125">Read-only</span></span><br/> | <span data-ttu-id="404fd-126">Recupera o número de qualificadores na coleção.</span><span class="sxs-lookup"><span data-stu-id="404fd-126">Retrieves the number of qualifiers in the collection.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="404fd-127">**Item**</span><span class="sxs-lookup"><span data-stu-id="404fd-127">**Item**</span></span>](qualifiers-item.md)<br/>         | <span data-ttu-id="404fd-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="404fd-128">Read-only</span></span><br/> | <span data-ttu-id="404fd-129">Recupera um objeto de [**qualificador**](qualifier.md) que representa o qualificador indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="404fd-129">Retrieves a [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span> <span data-ttu-id="404fd-130">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="404fd-130">This is the default property.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="404fd-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="404fd-131">Remarks</span></span>

<span data-ttu-id="404fd-132">Não é possível criar o objeto **Qualifiers** .</span><span class="sxs-lookup"><span data-stu-id="404fd-132">The **Qualifiers** object cannot be created.</span></span>

<span data-ttu-id="404fd-133">A propriedade de objeto [**PolicyInformation. Qualifiers**](policyinformation-qualifiers.md) capicor retorna um objeto **Qualifiers** .</span><span class="sxs-lookup"><span data-stu-id="404fd-133">The [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) CAPICOM object property returns a **Qualifiers** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="404fd-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="404fd-134">Requirements</span></span>



| <span data-ttu-id="404fd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="404fd-135">Requirement</span></span> | <span data-ttu-id="404fd-136">Valor</span><span class="sxs-lookup"><span data-stu-id="404fd-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="404fd-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="404fd-137">Redistributable</span></span><br/> | <span data-ttu-id="404fd-138">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="404fd-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="404fd-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="404fd-139">Header</span></span><br/>          | <dl> <span data-ttu-id="404fd-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="404fd-140"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="404fd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="404fd-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="404fd-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="404fd-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
