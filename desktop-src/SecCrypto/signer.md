---
description: Estabelece o signatário de um objeto SignedData ou SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Objeto de signatário
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758269"
---
# <a name="signer-object"></a><span data-ttu-id="2a1b3-103">Objeto de signatário</span><span class="sxs-lookup"><span data-stu-id="2a1b3-103">Signer object</span></span>

<span data-ttu-id="2a1b3-104">\[O objeto de **signatário** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-104">\[The **Signer** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2a1b3-105">Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2a1b3-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2a1b3-106">O objeto de **signatário** estabelece o signatário de um objeto [**SignedData**](signeddata.md) ou [**SignedCode**](signedcode.md) .</span><span class="sxs-lookup"><span data-stu-id="2a1b3-106">The **Signer** object establishes the signer of a [**SignedData**](signeddata.md) or [**SignedCode**](signedcode.md) object.</span></span> <span data-ttu-id="2a1b3-107">O [**certificado**](certificate.md) do objeto de **signatário** deve ter uma chave privada disponível que pode ser usada para assinar dados.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-107">The [**Certificate**](certificate.md) of the **Signer** object must have an available private key that can be used to sign data.</span></span>

## <a name="members"></a><span data-ttu-id="2a1b3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2a1b3-108">Members</span></span>

<span data-ttu-id="2a1b3-109">O objeto de **signatário** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2a1b3-109">The **Signer** object has these types of members:</span></span>

-   [<span data-ttu-id="2a1b3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2a1b3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2a1b3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a1b3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2a1b3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2a1b3-112">Methods</span></span>

<span data-ttu-id="2a1b3-113">O objeto de **signatário** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-113">The **Signer** object has these methods.</span></span>



| <span data-ttu-id="2a1b3-114">Método</span><span class="sxs-lookup"><span data-stu-id="2a1b3-114">Method</span></span>                      | <span data-ttu-id="2a1b3-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a1b3-115">Description</span></span>                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="2a1b3-116">**Carregar**</span><span class="sxs-lookup"><span data-stu-id="2a1b3-116">**Load**</span></span>](signer-load.md) | <span data-ttu-id="2a1b3-117">Carrega um certificado de autenticação de um arquivo PFX especificado.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-117">Loads a signing certificate from a specified PFX file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2a1b3-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a1b3-118">Properties</span></span>

<span data-ttu-id="2a1b3-119">O objeto de **signatário** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-119">The **Signer** object has these properties.</span></span>



| <span data-ttu-id="2a1b3-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2a1b3-120">Property</span></span>                                                                     | <span data-ttu-id="2a1b3-121">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="2a1b3-121">Access type</span></span>           | <span data-ttu-id="2a1b3-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a1b3-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a1b3-123">**AuthenticatedAttributes**</span><span class="sxs-lookup"><span data-stu-id="2a1b3-123">**AuthenticatedAttributes**</span></span>](signer-authenticatedattributes.md)<br/> | <span data-ttu-id="2a1b3-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2a1b3-124">Read-only</span></span><br/>  | <span data-ttu-id="2a1b3-125">A coleção de atributos autenticados.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-125">The collection of authenticated attributes.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2a1b3-126">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="2a1b3-126">**Certificate**</span></span>](signer-certificate.md)<br/>                         | <span data-ttu-id="2a1b3-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2a1b3-127">Read/write</span></span><br/> | <span data-ttu-id="2a1b3-128">O objeto de [**certificado**](certificate.md) que representa o certificado de um signatário dos dados.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-128">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span><br/> <span data-ttu-id="2a1b3-129">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-129">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span><br/> <span data-ttu-id="2a1b3-130">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-130">This is the default property.</span></span><br/> |
| [<span data-ttu-id="2a1b3-131">**Cadeia**</span><span class="sxs-lookup"><span data-stu-id="2a1b3-131">**Chain**</span></span>](signer-chain.md)<br/>                                     | <span data-ttu-id="2a1b3-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2a1b3-132">Read-only</span></span><br/>  | <span data-ttu-id="2a1b3-133">A cadeia do signatário.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-133">The chain of the signer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="2a1b3-134">**Opções**</span><span class="sxs-lookup"><span data-stu-id="2a1b3-134">**Options**</span></span>](signer-options.md)<br/>                                 | <span data-ttu-id="2a1b3-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2a1b3-135">Read/write</span></span><br/> | <span data-ttu-id="2a1b3-136">Define ou recupera a opção de certificado do signatário.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-136">Sets or retrieves the signer's certificate option.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="2a1b3-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a1b3-137">Remarks</span></span>

<span data-ttu-id="2a1b3-138">O objeto de **signatário** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-138">The **Signer** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="2a1b3-139">O ProgID do objeto de **signatário** é CAPICOM. Signatário. 2.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-139">The ProgID for the **Signer** object is CAPICOM.Signer.2.</span></span>

<span data-ttu-id="2a1b3-140">**CAPICOM 1. *x*:** o ProgID do objeto de **signatário** é CAPICOM. Signatário. 1.</span><span class="sxs-lookup"><span data-stu-id="2a1b3-140">**CAPICOM 1.*x*:** The ProgID for the **Signer** object is CAPICOM.Signer.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a1b3-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a1b3-141">Requirements</span></span>



| <span data-ttu-id="2a1b3-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a1b3-142">Requirement</span></span> | <span data-ttu-id="2a1b3-143">Valor</span><span class="sxs-lookup"><span data-stu-id="2a1b3-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1b3-144">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2a1b3-144">Redistributable</span></span><br/> | <span data-ttu-id="2a1b3-145">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a1b3-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2a1b3-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2a1b3-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="2a1b3-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a1b3-147"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a1b3-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a1b3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1b3-149">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="2a1b3-149">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
