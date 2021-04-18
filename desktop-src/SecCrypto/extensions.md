---
description: Representa uma coleção de objetos de extensão.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Objeto de extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766825"
---
# <a name="extensions-object"></a><span data-ttu-id="b12a2-103">Objeto de extensões</span><span class="sxs-lookup"><span data-stu-id="b12a2-103">Extensions object</span></span>

<span data-ttu-id="b12a2-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b12a2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b12a2-105">Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b12a2-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b12a2-106">O objeto **Extensions** representa uma coleção de objetos de [**extensão**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="b12a2-106">The **Extensions** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="b12a2-107">Cada objeto de [**extensão**](extension.md) representa uma única extensão de certificado.</span><span class="sxs-lookup"><span data-stu-id="b12a2-107">Each [**Extension**](extension.md) object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b12a2-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="b12a2-108">When to use</span></span>

<span data-ttu-id="b12a2-109">O objeto de **extensões** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="b12a2-109">The **Extensions** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b12a2-110">Recupere o número de extensões de certificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="b12a2-110">Retrieve the number of certificate extensions in the collection.</span></span>
-   <span data-ttu-id="b12a2-111">Recupere um objeto de [**extensão**](extension.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="b12a2-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="b12a2-112">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="b12a2-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="b12a2-113">Membros</span><span class="sxs-lookup"><span data-stu-id="b12a2-113">Members</span></span>

<span data-ttu-id="b12a2-114">O objeto de **extensões** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b12a2-114">The **Extensions** object has these types of members:</span></span>

-   [<span data-ttu-id="b12a2-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b12a2-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b12a2-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b12a2-116">Properties</span></span>

<span data-ttu-id="b12a2-117">O objeto de **extensões** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b12a2-117">The **Extensions** object has these properties.</span></span>



| <span data-ttu-id="b12a2-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b12a2-118">Property</span></span>                                           | <span data-ttu-id="b12a2-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b12a2-119">Access type</span></span>          | <span data-ttu-id="b12a2-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b12a2-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b12a2-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b12a2-121">**\_NewEnum**</span></span>](extensions-newenum.md)<br/> | <span data-ttu-id="b12a2-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b12a2-122">Read-only</span></span><br/> | <span data-ttu-id="b12a2-123">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="b12a2-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="b12a2-124">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="b12a2-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="b12a2-125">**Contar**</span><span class="sxs-lookup"><span data-stu-id="b12a2-125">**Count**</span></span>](extensions-count.md)<br/>       | <span data-ttu-id="b12a2-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b12a2-126">Read-only</span></span><br/> | <span data-ttu-id="b12a2-127">Recupera o número de objetos de [**extensão**](extension.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="b12a2-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="b12a2-128">**Item**</span><span class="sxs-lookup"><span data-stu-id="b12a2-128">**Item**</span></span>](extensions-item.md)<br/>         | <span data-ttu-id="b12a2-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b12a2-129">Read-only</span></span><br/> | <span data-ttu-id="b12a2-130">Recupera o objeto de [**extensão**](extension.md) que representa a extensão de certificado indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="b12a2-130">Retrieves the [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span> <span data-ttu-id="b12a2-131">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="b12a2-131">This is the default property.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="b12a2-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="b12a2-132">Remarks</span></span>

<span data-ttu-id="b12a2-133">O objeto **Extensions** é retornado pelo método [**Certificate. Extensions**](certificate-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="b12a2-133">The **Extensions** object is returned by the [**Certificate.Extensions**](certificate-extensions.md) method.</span></span>

<span data-ttu-id="b12a2-134">Não é possível criar o objeto de **extensões** .</span><span class="sxs-lookup"><span data-stu-id="b12a2-134">The **Extensions** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12a2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b12a2-135">Requirements</span></span>



| <span data-ttu-id="b12a2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b12a2-136">Requirement</span></span> | <span data-ttu-id="b12a2-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b12a2-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b12a2-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b12a2-138">End of client support</span></span><br/> | <span data-ttu-id="b12a2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b12a2-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b12a2-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b12a2-140">End of server support</span></span><br/> | <span data-ttu-id="b12a2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b12a2-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b12a2-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b12a2-142">Redistributable</span></span><br/>       | <span data-ttu-id="b12a2-143">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b12a2-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b12a2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b12a2-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b12a2-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b12a2-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
