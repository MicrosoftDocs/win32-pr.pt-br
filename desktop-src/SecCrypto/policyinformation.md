---
description: Fornece acesso às informações de política de uma extensão.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Objeto PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755040"
---
# <a name="policyinformation-object"></a><span data-ttu-id="330a8-103">Objeto PolicyInformation</span><span class="sxs-lookup"><span data-stu-id="330a8-103">PolicyInformation object</span></span>

<span data-ttu-id="330a8-104">\[O objeto **PolicyInformation** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="330a8-104">\[The **PolicyInformation** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="330a8-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="330a8-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="330a8-106">O objeto **PolicyInformation** fornece acesso às informações de política de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="330a8-106">The **PolicyInformation** object provides access to the policy information of an extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="330a8-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="330a8-107">When to use</span></span>

<span data-ttu-id="330a8-108">O objeto **PolicyInformation** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="330a8-108">The **PolicyInformation** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="330a8-109">Recupere a OID da política.</span><span class="sxs-lookup"><span data-stu-id="330a8-109">Retrieve the policy OID.</span></span>
-   <span data-ttu-id="330a8-110">Recupere uma coleção dos qualificadores da política.</span><span class="sxs-lookup"><span data-stu-id="330a8-110">Retrieve a collection of the policy's qualifiers.</span></span>

## <a name="members"></a><span data-ttu-id="330a8-111">Membros</span><span class="sxs-lookup"><span data-stu-id="330a8-111">Members</span></span>

<span data-ttu-id="330a8-112">O objeto **PolicyInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="330a8-112">The **PolicyInformation** object has these types of members:</span></span>

-   [<span data-ttu-id="330a8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="330a8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="330a8-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="330a8-114">Properties</span></span>

<span data-ttu-id="330a8-115">O objeto **PolicyInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="330a8-115">The **PolicyInformation** object has these properties.</span></span>



| <span data-ttu-id="330a8-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="330a8-116">Property</span></span>                                                      | <span data-ttu-id="330a8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="330a8-117">Description</span></span>                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="330a8-118">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="330a8-118">**OID**</span></span>](policyinformation-oid.md)<br/>               | <span data-ttu-id="330a8-119">Recupera o OID da política, como um objeto [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="330a8-119">Retrieves the policy's OID, as an [**OID**](oid.md) object.</span></span> <span data-ttu-id="330a8-120">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="330a8-120">This is the default property.</span></span><br/>       |
| [<span data-ttu-id="330a8-121">**Qualificadores**</span><span class="sxs-lookup"><span data-stu-id="330a8-121">**Qualifiers**</span></span>](policyinformation-qualifiers.md)<br/> | <span data-ttu-id="330a8-122">Recupera uma coleção de qualificadores de política, como um objeto de [**qualificadores**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="330a8-122">Retrieves a collection of the policy's qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="330a8-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="330a8-123">Remarks</span></span>

<span data-ttu-id="330a8-124">O objeto **PolicyInformation** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="330a8-124">The **PolicyInformation** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="330a8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="330a8-125">Requirements</span></span>



| <span data-ttu-id="330a8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="330a8-126">Requirement</span></span> | <span data-ttu-id="330a8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="330a8-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="330a8-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="330a8-128">Redistributable</span></span><br/> | <span data-ttu-id="330a8-129">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="330a8-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="330a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="330a8-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="330a8-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="330a8-131"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
