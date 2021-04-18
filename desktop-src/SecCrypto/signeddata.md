---
description: Fornece propriedades e métodos para estabelecer o conteúdo a ser assinado com uma assinatura digital, assinar ou coassinar dados digitalmente e verificar a assinatura digital de dados assinados. A mensagem assinada está no \# formato PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Objeto SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788102"
---
# <a name="signeddata-object"></a><span data-ttu-id="58eb2-104">Objeto SignedData</span><span class="sxs-lookup"><span data-stu-id="58eb2-104">SignedData object</span></span>

<span data-ttu-id="58eb2-105">\[O objeto **SignedData** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="58eb2-105">\[The **SignedData** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58eb2-106">Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="58eb2-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="58eb2-107">O objeto **SignedData** fornece propriedades e métodos para estabelecer o conteúdo a ser assinado com uma [*assinatura digital*](../secgloss/d-gly.md), para assinar ou coassinar dados digitalmente e para verificar a assinatura digital de dados assinados.</span><span class="sxs-lookup"><span data-stu-id="58eb2-107">The **SignedData** object provides properties and methods to establish the content to be signed with a [*digital signature*](../secgloss/d-gly.md), to sign or cosign data digitally, and to verify the digital signature of signed data.</span></span> <span data-ttu-id="58eb2-108">A mensagem assinada está no \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="58eb2-108">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="58eb2-109">Uma assinatura de dados, se verificada, comprova a associação entre um signatário e dados e mostra que os dados não foram alterados de nenhuma forma após a criação da assinatura.</span><span class="sxs-lookup"><span data-stu-id="58eb2-109">A data signature, if verified, proves the association between a signer and data and shows that the data was not changed in any way after the signature was created.</span></span>

## <a name="members"></a><span data-ttu-id="58eb2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="58eb2-110">Members</span></span>

<span data-ttu-id="58eb2-111">O objeto **SignedData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58eb2-111">The **SignedData** object has these types of members:</span></span>

-   [<span data-ttu-id="58eb2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="58eb2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="58eb2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58eb2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="58eb2-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="58eb2-114">Methods</span></span>

<span data-ttu-id="58eb2-115">O objeto **SignedData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="58eb2-115">The **SignedData** object has these methods.</span></span>



| <span data-ttu-id="58eb2-116">Método</span><span class="sxs-lookup"><span data-stu-id="58eb2-116">Method</span></span>                              | <span data-ttu-id="58eb2-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="58eb2-117">Description</span></span>                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="58eb2-118">**Coassinar**</span><span class="sxs-lookup"><span data-stu-id="58eb2-118">**CoSign**</span></span>](signeddata-cosign.md) | <span data-ttu-id="58eb2-119">Assina uma mensagem já assinada.</span><span class="sxs-lookup"><span data-stu-id="58eb2-119">Cosigns an already signed message.</span></span><br/>                       |
| [<span data-ttu-id="58eb2-120">**Assinar**</span><span class="sxs-lookup"><span data-stu-id="58eb2-120">**Sign**</span></span>](signeddata-sign.md)     | <span data-ttu-id="58eb2-121">Cria uma assinatura digital no conteúdo a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="58eb2-121">Creates a digital signature on the content to be signed.</span></span><br/> |
| [<span data-ttu-id="58eb2-122">**Verificar**</span><span class="sxs-lookup"><span data-stu-id="58eb2-122">**Verify**</span></span>](signeddata-verify.md) | <span data-ttu-id="58eb2-123">Determina a validade de uma assinatura ou assinaturas.</span><span class="sxs-lookup"><span data-stu-id="58eb2-123">Determines the validity of a signature or signatures.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="58eb2-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58eb2-124">Properties</span></span>

<span data-ttu-id="58eb2-125">O objeto **SignedData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58eb2-125">The **SignedData** object has these properties.</span></span>



| <span data-ttu-id="58eb2-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="58eb2-126">Property</span></span>                                                   | <span data-ttu-id="58eb2-127">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="58eb2-127">Access type</span></span>           | <span data-ttu-id="58eb2-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="58eb2-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58eb2-129">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="58eb2-129">**Certificates**</span></span>](signeddata-certificates.md)<br/> | <span data-ttu-id="58eb2-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58eb2-130">Read-only</span></span><br/>  | <span data-ttu-id="58eb2-131">Recupera a coleção de [**certificados**](certificates.md) dos dados assinados.</span><span class="sxs-lookup"><span data-stu-id="58eb2-131">Retrieves the [**Certificates**](certificates.md) collection of the signed data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="58eb2-132">**Disputa**</span><span class="sxs-lookup"><span data-stu-id="58eb2-132">**Content**</span></span>](signeddata-content.md)<br/>           | <span data-ttu-id="58eb2-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="58eb2-133">Read/write</span></span><br/> | <span data-ttu-id="58eb2-134">Dados a serem assinados.</span><span class="sxs-lookup"><span data-stu-id="58eb2-134">Data to be signed.</span></span> <span data-ttu-id="58eb2-135">Essa propriedade deve ser inicializada antes que o método [**Sign**](signeddata-sign.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="58eb2-135">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span><br/> <span data-ttu-id="58eb2-136">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer assinatura associada ao objeto antes da alteração da propriedade é perdida.</span><span class="sxs-lookup"><span data-stu-id="58eb2-136">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span><br/> <span data-ttu-id="58eb2-137">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="58eb2-137">This is the default property.</span></span><br/> |
| [<span data-ttu-id="58eb2-138">**Signatários**</span><span class="sxs-lookup"><span data-stu-id="58eb2-138">**Signers**</span></span>](signeddata-signers.md)<br/>           | <span data-ttu-id="58eb2-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58eb2-139">Read-only</span></span><br/>  | <span data-ttu-id="58eb2-140">Recupera a coleção de [**assinantes**](signers.md) que representa os criadores de assinatura dos dados.</span><span class="sxs-lookup"><span data-stu-id="58eb2-140">Retrieves the [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="58eb2-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="58eb2-141">Remarks</span></span>

<span data-ttu-id="58eb2-142">O objeto **SignedData** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="58eb2-142">The **SignedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="58eb2-143">O ProgID do objeto **SignedData** é CAPICOM. SignedData. 1.</span><span class="sxs-lookup"><span data-stu-id="58eb2-143">The ProgID for the **SignedData** object is CAPICOM.SignedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="58eb2-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58eb2-144">Requirements</span></span>



| <span data-ttu-id="58eb2-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="58eb2-145">Requirement</span></span> | <span data-ttu-id="58eb2-146">Valor</span><span class="sxs-lookup"><span data-stu-id="58eb2-146">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58eb2-147">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="58eb2-147">Redistributable</span></span><br/> | <span data-ttu-id="58eb2-148">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="58eb2-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="58eb2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="58eb2-149">DLL</span></span><br/>             | <dl> <span data-ttu-id="58eb2-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58eb2-150"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58eb2-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="58eb2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58eb2-152">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="58eb2-152">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
