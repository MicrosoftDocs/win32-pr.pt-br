---
description: Representa uma única extensão de certificado.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objeto de extensão (Mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779365"
---
# <a name="extension-object"></a><span data-ttu-id="4a697-103">Objeto de extensão</span><span class="sxs-lookup"><span data-stu-id="4a697-103">Extension object</span></span>

<span data-ttu-id="4a697-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a697-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4a697-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4a697-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4a697-106">O objeto de **extensão** representa uma única extensão de certificado.</span><span class="sxs-lookup"><span data-stu-id="4a697-106">The **Extension** object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4a697-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="4a697-107">When to use</span></span>

<span data-ttu-id="4a697-108">O objeto de **extensão** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="4a697-108">The **Extension** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4a697-109">Recupere o OID da extensão do certificado.</span><span class="sxs-lookup"><span data-stu-id="4a697-109">Retrieve the OID of the certificate extension.</span></span>
-   <span data-ttu-id="4a697-110">Recupere os dados de extensão do certificado representados por um objeto [**EncodedData**](encodeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="4a697-110">Retrieve the certificate extension data represented by an [**EncodedData**](encodeddata.md) object.</span></span>
-   <span data-ttu-id="4a697-111">Determine se a extensão do certificado está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="4a697-111">Determine whether the certificate extension is marked as critical.</span></span>

## <a name="members"></a><span data-ttu-id="4a697-112">Membros</span><span class="sxs-lookup"><span data-stu-id="4a697-112">Members</span></span>

<span data-ttu-id="4a697-113">O objeto de **extensão** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4a697-113">The **Extension** object has these types of members:</span></span>

-   [<span data-ttu-id="4a697-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4a697-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a697-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4a697-115">Properties</span></span>

<span data-ttu-id="4a697-116">O objeto de **extensão** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4a697-116">The **Extension** object has these properties.</span></span>



| <span data-ttu-id="4a697-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4a697-117">Property</span></span>                                                | <span data-ttu-id="4a697-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4a697-118">Access type</span></span>          | <span data-ttu-id="4a697-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a697-119">Description</span></span>                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a697-120">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="4a697-120">**EncodedData**</span></span>](extension-encodeddata.md)<br/> | <span data-ttu-id="4a697-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a697-121">Read-only</span></span><br/> | <span data-ttu-id="4a697-122">Recupera os dados codificados para a extensão.</span><span class="sxs-lookup"><span data-stu-id="4a697-122">Retrieves the encoded data for the extension.</span></span><br/>                                      |
| [<span data-ttu-id="4a697-123">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="4a697-123">**IsCritical**</span></span>](extension-iscritical.md)<br/>   | <span data-ttu-id="4a697-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a697-124">Read-only</span></span><br/> | <span data-ttu-id="4a697-125">Recupera um valor booliano que indica se a extensão está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="4a697-125">Retrieves a Boolean value that indicates whether the extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="4a697-126">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="4a697-126">**OID**</span></span>](extension-oid.md)<br/>                 | <span data-ttu-id="4a697-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a697-127">Read-only</span></span><br/> | <span data-ttu-id="4a697-128">Recupera o identificador de objeto para a extensão.</span><span class="sxs-lookup"><span data-stu-id="4a697-128">Retrieves the object identifier for the extension.</span></span> <span data-ttu-id="4a697-129">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="4a697-129">This is the default property.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="4a697-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a697-130">Remarks</span></span>

<span data-ttu-id="4a697-131">Não é possível criar o objeto de **extensão** .</span><span class="sxs-lookup"><span data-stu-id="4a697-131">The **Extension** object cannot be created.</span></span>

<span data-ttu-id="4a697-132">O objeto de **extensão** é usado pelo objeto da coleção de [**extensões**](extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="4a697-132">The **Extension** object is used by the [**Extensions**](extensions.md) collection object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a697-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a697-133">Requirements</span></span>



| <span data-ttu-id="4a697-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a697-134">Requirement</span></span> | <span data-ttu-id="4a697-135">Valor</span><span class="sxs-lookup"><span data-stu-id="4a697-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a697-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4a697-136">End of client support</span></span><br/> | <span data-ttu-id="4a697-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a697-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4a697-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4a697-138">End of server support</span></span><br/> | <span data-ttu-id="4a697-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a697-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4a697-140">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4a697-140">Redistributable</span></span><br/>       | <span data-ttu-id="4a697-141">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a697-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a697-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a697-142">Header</span></span><br/>                | <dl> <span data-ttu-id="4a697-143"><dt>Mmcobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-143"><dt>Mmcobj.h</dt></span></span> </dl>    |
| <span data-ttu-id="4a697-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4a697-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4a697-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
