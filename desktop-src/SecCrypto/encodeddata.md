---
description: Representa um bloco de dados codificados ASN. 1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Objeto EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768437"
---
# <a name="encodeddata-object"></a><span data-ttu-id="5070f-103">Objeto EncodedData</span><span class="sxs-lookup"><span data-stu-id="5070f-103">EncodedData object</span></span>

<span data-ttu-id="5070f-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5070f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5070f-105">Em vez disso, use a [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5070f-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5070f-106">O objeto **EncodedData** representa um bloco de dados codificados pelo ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="5070f-106">The **EncodedData** object represents a block of ASN.1 encoded data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5070f-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="5070f-107">When to use</span></span>

<span data-ttu-id="5070f-108">O objeto **EncodedData** é retornado por várias propriedades de objeto CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="5070f-108">The **EncodedData** object is returned by several CAPICOM object properties.</span></span> <span data-ttu-id="5070f-109">Quando retornado, esse objeto é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="5070f-109">When returned, this object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5070f-110">Obtenha uma representação de cadeia de caracteres dos dados codificados.</span><span class="sxs-lookup"><span data-stu-id="5070f-110">Obtain a string representation of the encoded data.</span></span>
-   <span data-ttu-id="5070f-111">Obtenha o objeto decodificador, se ele existir, que está associado aos dados codificados.</span><span class="sxs-lookup"><span data-stu-id="5070f-111">Obtain the decoder object, if it exists, that is associated with the encoded data.</span></span>
-   <span data-ttu-id="5070f-112">Determine o tipo de dados codificados.</span><span class="sxs-lookup"><span data-stu-id="5070f-112">Determine the type of encoded data.</span></span>

## <a name="members"></a><span data-ttu-id="5070f-113">Membros</span><span class="sxs-lookup"><span data-stu-id="5070f-113">Members</span></span>

<span data-ttu-id="5070f-114">O objeto **EncodedData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5070f-114">The **EncodedData** object has these types of members:</span></span>

-   [<span data-ttu-id="5070f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="5070f-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="5070f-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5070f-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5070f-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="5070f-117">Methods</span></span>

<span data-ttu-id="5070f-118">O objeto **EncodedData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5070f-118">The **EncodedData** object has these methods.</span></span>



| <span data-ttu-id="5070f-119">Método</span><span class="sxs-lookup"><span data-stu-id="5070f-119">Method</span></span>                                 | <span data-ttu-id="5070f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="5070f-120">Description</span></span>                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="5070f-121">**Decodificador**</span><span class="sxs-lookup"><span data-stu-id="5070f-121">**Decoder**</span></span>](encodeddata-decoder.md) | <span data-ttu-id="5070f-122">Obtém um objeto decodificador, se houver.</span><span class="sxs-lookup"><span data-stu-id="5070f-122">Obtains a decoder object, if one exists.</span></span><br/>             |
| [<span data-ttu-id="5070f-123">**Formatar**</span><span class="sxs-lookup"><span data-stu-id="5070f-123">**Format**</span></span>](encodeddata-format.md)   | <span data-ttu-id="5070f-124">Retorna uma representação de cadeia de caracteres dos dados codificados.</span><span class="sxs-lookup"><span data-stu-id="5070f-124">Returns a string representation of the encoded data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5070f-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5070f-125">Properties</span></span>

<span data-ttu-id="5070f-126">O objeto **EncodedData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5070f-126">The **EncodedData** object has these properties.</span></span>



| <span data-ttu-id="5070f-127">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5070f-127">Property</span></span>                                      | <span data-ttu-id="5070f-128">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5070f-128">Access type</span></span>          | <span data-ttu-id="5070f-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="5070f-129">Description</span></span>                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="5070f-130">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5070f-130">**Value**</span></span>](encodeddata-value.md)<br/> | <span data-ttu-id="5070f-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5070f-131">Read-only</span></span><br/> | <span data-ttu-id="5070f-132">Recupera os dados codificados.</span><span class="sxs-lookup"><span data-stu-id="5070f-132">Retrieves the encoded data.</span></span> <span data-ttu-id="5070f-133">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="5070f-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5070f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="5070f-134">Remarks</span></span>

<span data-ttu-id="5070f-135">O único tipo de dados codificado com suporte é [**CertificatePolicies**](certificatepolicies.md).</span><span class="sxs-lookup"><span data-stu-id="5070f-135">The only supported type of encoded data is [**CertificatePolicies**](certificatepolicies.md).</span></span>

<span data-ttu-id="5070f-136">O objeto **EncodedData** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="5070f-136">The **EncodedData** object cannot be created.</span></span>

<span data-ttu-id="5070f-137">As seguintes propriedades de objeto capicor retornam um objeto **EncodedData** :</span><span class="sxs-lookup"><span data-stu-id="5070f-137">The following CAPICOM object properties return an **EncodedData** object:</span></span>

-   <span data-ttu-id="5070f-138">**PublicKey. EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="5070f-138">**PublicKey.EncodedKey**</span></span>
-   <span data-ttu-id="5070f-139">**PublicKey. EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="5070f-139">**PublicKey.EncodedParameters**</span></span>
-   <span data-ttu-id="5070f-140">**Extensão. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="5070f-140">**Extension.EncodedData**</span></span>
-   <span data-ttu-id="5070f-141">**Policy. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="5070f-141">**Policy.EncodedData**</span></span>

## <a name="requirements"></a><span data-ttu-id="5070f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5070f-142">Requirements</span></span>



| <span data-ttu-id="5070f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5070f-143">Requirement</span></span> | <span data-ttu-id="5070f-144">Valor</span><span class="sxs-lookup"><span data-stu-id="5070f-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5070f-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5070f-145">End of client support</span></span><br/> | <span data-ttu-id="5070f-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5070f-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5070f-147">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5070f-147">End of server support</span></span><br/> | <span data-ttu-id="5070f-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5070f-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5070f-149">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5070f-149">Redistributable</span></span><br/>       | <span data-ttu-id="5070f-150">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5070f-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5070f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="5070f-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5070f-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5070f-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
