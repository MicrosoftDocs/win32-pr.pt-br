---
description: Fornece acesso somente leitura às propriedades EKU (uso estendido de chave) de um certificado.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Objeto ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748047"
---
# <a name="extendedkeyusage-object"></a><span data-ttu-id="4107c-103">Objeto ExtendedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="4107c-103">ExtendedKeyUsage object</span></span>

<span data-ttu-id="4107c-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4107c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4107c-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4107c-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4107c-106">O objeto **ExtendedKeyUsage** fornece acesso somente leitura às propriedades EKU (uso estendido de chave) de um certificado.</span><span class="sxs-lookup"><span data-stu-id="4107c-106">The **ExtendedKeyUsage** object provides read-only access to the extended key usage (EKU) properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="4107c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4107c-107">Members</span></span>

<span data-ttu-id="4107c-108">O objeto **ExtendedKeyUsage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4107c-108">The **ExtendedKeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="4107c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4107c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4107c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4107c-110">Properties</span></span>

<span data-ttu-id="4107c-111">O objeto **ExtendedKeyUsage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4107c-111">The **ExtendedKeyUsage** object has these properties.</span></span>



| <span data-ttu-id="4107c-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4107c-112">Property</span></span>                                                     | <span data-ttu-id="4107c-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4107c-113">Access type</span></span>          | <span data-ttu-id="4107c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4107c-114">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4107c-115">**EKUs**</span><span class="sxs-lookup"><span data-stu-id="4107c-115">**EKUs**</span></span>](extendedkeyusage-ekus.md)<br/>             | <span data-ttu-id="4107c-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4107c-116">Read-only</span></span><br/> | <span data-ttu-id="4107c-117">Coleção [**EKUs**](ekus.md) que contém os objetos [**EKU**](eku.md) para o certificado.</span><span class="sxs-lookup"><span data-stu-id="4107c-117">[**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span><br/>                            |
| [<span data-ttu-id="4107c-118">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="4107c-118">**IsCritical**</span></span>](extendedkeyusage-iscritical.md)<br/> | <span data-ttu-id="4107c-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4107c-119">Read-only</span></span><br/> | <span data-ttu-id="4107c-120">Recupera um valor **booliano** que indica se a extensão EKU está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="4107c-120">Retrieves a **Boolean** value that indicates whether the EKU extension is marked critical.</span></span><br/>                                   |
| [<span data-ttu-id="4107c-121">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="4107c-121">**IsPresent**</span></span>](extendedkeyusage-ispresent.md)<br/>   | <span data-ttu-id="4107c-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4107c-122">Read-only</span></span><br/> | <span data-ttu-id="4107c-123">Recupera um valor **booliano** que indica se a extensão EKU está presente.</span><span class="sxs-lookup"><span data-stu-id="4107c-123">Retrieves a **Boolean** value that indicates whether the EKU extension is present.</span></span><br/> <span data-ttu-id="4107c-124">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="4107c-124">This is the default property.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4107c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4107c-125">Remarks</span></span>

<span data-ttu-id="4107c-126">O objeto **ExtendedKeyUsage** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="4107c-126">The **ExtendedKeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="4107c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4107c-127">Requirements</span></span>



| <span data-ttu-id="4107c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4107c-128">Requirement</span></span> | <span data-ttu-id="4107c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4107c-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4107c-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4107c-130">End of client support</span></span><br/> | <span data-ttu-id="4107c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4107c-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4107c-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4107c-132">End of server support</span></span><br/> | <span data-ttu-id="4107c-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4107c-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4107c-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4107c-134">Redistributable</span></span><br/>       | <span data-ttu-id="4107c-135">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4107c-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4107c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4107c-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4107c-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4107c-137"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4107c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4107c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4107c-139">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="4107c-139">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
