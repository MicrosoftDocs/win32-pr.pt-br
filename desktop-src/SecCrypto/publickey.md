---
description: O objeto PublicKey representa uma chave pública em um objeto de certificado.
title: Objeto PublicKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748864"
---
# <a name="publickey-object"></a><span data-ttu-id="14755-103">Objeto PublicKey</span><span class="sxs-lookup"><span data-stu-id="14755-103">PublicKey object</span></span>

<span data-ttu-id="14755-104">\[O objeto **PublicKey** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="14755-104">\[The **PublicKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14755-105">Em vez disso, use a [**Propriedade X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="14755-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="14755-106">O objeto **PublicKey** representa uma chave pública em um objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="14755-106">The **PublicKey** object represents a public key in a [**Certificate**](certificate.md) object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="14755-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="14755-107">When to use</span></span>

<span data-ttu-id="14755-108">O objeto **PublicKey** é usado para recuperar dados sobre a chave pública.</span><span class="sxs-lookup"><span data-stu-id="14755-108">The **PublicKey** object is used to retrieve data about the public key.</span></span>

## <a name="members"></a><span data-ttu-id="14755-109">Membros</span><span class="sxs-lookup"><span data-stu-id="14755-109">Members</span></span>

<span data-ttu-id="14755-110">O objeto **PublicKey** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="14755-110">The **PublicKey** object has these types of members:</span></span>

-   [<span data-ttu-id="14755-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="14755-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14755-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="14755-112">Properties</span></span>

<span data-ttu-id="14755-113">O objeto **PublicKey** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="14755-113">The **PublicKey** object has these properties.</span></span>



| <span data-ttu-id="14755-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="14755-114">Property</span></span>                                                            | <span data-ttu-id="14755-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="14755-115">Access type</span></span>          | <span data-ttu-id="14755-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="14755-116">Description</span></span>                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14755-117">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="14755-117">**Algorithm**</span></span>](publickey-algorithm.md)<br/>                 | <span data-ttu-id="14755-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="14755-118">Read-only</span></span><br/> | <span data-ttu-id="14755-119">Recupera o objeto [**OID**](oid.md) que identifica o algoritmo usado pela chave pública.</span><span class="sxs-lookup"><span data-stu-id="14755-119">Retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="14755-120">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="14755-120">This is the default property.</span></span><br/> |
| [<span data-ttu-id="14755-121">**EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="14755-121">**EncodedKey**</span></span>](publickey-encodedkey.md)<br/>               | <span data-ttu-id="14755-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="14755-122">Read-only</span></span><br/> | <span data-ttu-id="14755-123">Recupera um objeto [**EncodedData**](encodeddata.md) que fornece acesso ao valor da chave pública.</span><span class="sxs-lookup"><span data-stu-id="14755-123">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span><br/>                 |
| [<span data-ttu-id="14755-124">**EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="14755-124">**EncodedParameters**</span></span>](publickey-encodedparameters.md)<br/> | <span data-ttu-id="14755-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="14755-125">Read-only</span></span><br/> | <span data-ttu-id="14755-126">Recupera um objeto [**EncodedData**](encodeddata.md) que fornece acesso aos parâmetros do algoritmo de chave pública.</span><span class="sxs-lookup"><span data-stu-id="14755-126">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span><br/>  |
| [<span data-ttu-id="14755-127">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="14755-127">**Length**</span></span>](publickey-length.md)<br/>                       | <span data-ttu-id="14755-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="14755-128">Read-only</span></span><br/> | <span data-ttu-id="14755-129">Recupera o comprimento da chave pública em bits.</span><span class="sxs-lookup"><span data-stu-id="14755-129">Retrieves the length of the public key in bits.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="14755-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="14755-130">Remarks</span></span>

<span data-ttu-id="14755-131">Não é possível criar o objeto **PublicKey** .</span><span class="sxs-lookup"><span data-stu-id="14755-131">The **PublicKey** object cannot be created.</span></span>

<span data-ttu-id="14755-132">O objeto **PublicKey** é usado pelo método [**Certificate. PublicKey**](certificate-publickey.md) .</span><span class="sxs-lookup"><span data-stu-id="14755-132">The **PublicKey** object is used by the [**Certificate.PublicKey**](certificate-publickey.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="14755-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14755-133">Requirements</span></span>



| <span data-ttu-id="14755-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="14755-134">Requirement</span></span> | <span data-ttu-id="14755-135">Valor</span><span class="sxs-lookup"><span data-stu-id="14755-135">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14755-136">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="14755-136">Redistributable</span></span><br/> | <span data-ttu-id="14755-137">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="14755-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14755-138">DLL</span><span class="sxs-lookup"><span data-stu-id="14755-138">DLL</span></span><br/>             | <dl> <span data-ttu-id="14755-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14755-139"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
