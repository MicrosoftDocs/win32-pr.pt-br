---
description: Representa uma coleção de objetos Extended.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Objeto ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752126"
---
# <a name="extendedproperties-object"></a><span data-ttu-id="43da2-103">Objeto ExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="43da2-103">ExtendedProperties object</span></span>

<span data-ttu-id="43da2-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="43da2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="43da2-105">Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="43da2-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="43da2-106">Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="43da2-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="43da2-107">O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]</span><span class="sxs-lookup"><span data-stu-id="43da2-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="43da2-108">O objeto **ExtendedProperties** representa uma coleção de objetos [**Extended**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="43da2-108">The **ExtendedProperties** object represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span> <span data-ttu-id="43da2-109">Cada objeto representa uma única propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="43da2-109">Each object represents a single extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="43da2-110">Quando usar</span><span class="sxs-lookup"><span data-stu-id="43da2-110">When to use</span></span>

<span data-ttu-id="43da2-111">O objeto **ExtendedProperties** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="43da2-111">The **ExtendedProperties** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="43da2-112">Adicionar ou remover um objeto [**Extended**](extendedproperty.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-112">Add or remove an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="43da2-113">Recupere o número de propriedades estendidas na coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-113">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="43da2-114">Recupera um objeto [**estendiproperty**](extendedproperty.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-114">Retrieve a specific [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="43da2-115">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="43da2-116">Membros</span><span class="sxs-lookup"><span data-stu-id="43da2-116">Members</span></span>

<span data-ttu-id="43da2-117">O objeto **ExtendedProperties** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43da2-117">The **ExtendedProperties** object has these types of members:</span></span>

-   [<span data-ttu-id="43da2-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="43da2-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="43da2-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43da2-119">Properties</span></span>](#extendedproperties-object)

### <a name="methods"></a><span data-ttu-id="43da2-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="43da2-120">Methods</span></span>

<span data-ttu-id="43da2-121">O objeto **ExtendedProperties** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="43da2-121">The **ExtendedProperties** object has these methods.</span></span>



| <span data-ttu-id="43da2-122">Método</span><span class="sxs-lookup"><span data-stu-id="43da2-122">Method</span></span>                                      | <span data-ttu-id="43da2-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="43da2-123">Description</span></span>                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43da2-124">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="43da2-124">**Add**</span></span>](extendedproperties-add.md)       | <span data-ttu-id="43da2-125">Adiciona um objeto [**estendiproperty**](extendedproperty.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-125">Adds an [**ExtendedProperty**](extendedproperty.md) object to the collection.</span></span><br/>      |
| [<span data-ttu-id="43da2-126">**Remover**</span><span class="sxs-lookup"><span data-stu-id="43da2-126">**Remove**</span></span>](extendedproperties-remove.md) | <span data-ttu-id="43da2-127">Remove um objeto [**estendiproperty**](extendedproperty.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-127">Removes an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="43da2-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43da2-128">Properties</span></span>

<span data-ttu-id="43da2-129">O objeto **ExtendedProperties** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="43da2-129">The **ExtendedProperties** object has these properties.</span></span>



| <span data-ttu-id="43da2-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="43da2-130">Property</span></span>                                                   | <span data-ttu-id="43da2-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="43da2-131">Access type</span></span>          | <span data-ttu-id="43da2-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="43da2-132">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43da2-133">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="43da2-133">**\_NewEnum**</span></span>](extendedproperties-newenum.md)<br/> | <span data-ttu-id="43da2-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43da2-134">Read-only</span></span><br/> | <span data-ttu-id="43da2-135">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-135">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="43da2-136">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="43da2-136">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="43da2-137">**Contar**</span><span class="sxs-lookup"><span data-stu-id="43da2-137">**Count**</span></span>](extendedproperties-count.md)<br/>       | <span data-ttu-id="43da2-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43da2-138">Read-only</span></span><br/> | <span data-ttu-id="43da2-139">Recupera o número de objetos [**Extended**](extendedproperty.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-139">Retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="43da2-140">**Item**</span><span class="sxs-lookup"><span data-stu-id="43da2-140">**Item**</span></span>](extendedproperties-item.md)<br/>         | <span data-ttu-id="43da2-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43da2-141">Read-only</span></span><br/> | <span data-ttu-id="43da2-142">Recupera um objeto [**estendiproperty**](extendedproperty.md) que representa a propriedade estendida indexada da coleção.</span><span class="sxs-lookup"><span data-stu-id="43da2-142">Retrieves an [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span> <span data-ttu-id="43da2-143">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="43da2-143">This is the default property.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="43da2-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="43da2-144">Remarks</span></span>

<span data-ttu-id="43da2-145">O objeto **ExtendedProperties** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="43da2-145">The **ExtendedProperties** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="43da2-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43da2-146">Requirements</span></span>



| <span data-ttu-id="43da2-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="43da2-147">Requirement</span></span> | <span data-ttu-id="43da2-148">Valor</span><span class="sxs-lookup"><span data-stu-id="43da2-148">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43da2-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="43da2-149">End of client support</span></span><br/> | <span data-ttu-id="43da2-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43da2-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="43da2-151">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="43da2-151">End of server support</span></span><br/> | <span data-ttu-id="43da2-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43da2-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="43da2-153">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="43da2-153">Redistributable</span></span><br/>       | <span data-ttu-id="43da2-154">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="43da2-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="43da2-155">DLL</span><span class="sxs-lookup"><span data-stu-id="43da2-155">DLL</span></span><br/>                   | <dl> <span data-ttu-id="43da2-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43da2-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
