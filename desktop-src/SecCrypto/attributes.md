---
description: Representa uma coleção de objetos de atributo.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Objeto Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756157"
---
# <a name="attributes-object"></a><span data-ttu-id="08b0b-103">Objeto Attributes</span><span class="sxs-lookup"><span data-stu-id="08b0b-103">Attributes object</span></span>

<span data-ttu-id="08b0b-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08b0b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="08b0b-105">Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="08b0b-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="08b0b-106">O objeto **Attributes** representa uma coleção de objetos [**Attribute**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="08b0b-106">The **Attributes** object represents a collection of [**Attribute**](attribute.md) objects.</span></span> <span data-ttu-id="08b0b-107">Cada objeto de [**atributo**](attribute.md) representa um único atributo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="08b0b-107">Each [**Attribute**](attribute.md) object represents a single attribute of a message.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="08b0b-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="08b0b-108">When to use</span></span>

<span data-ttu-id="08b0b-109">O objeto **Attributes** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="08b0b-109">The **Attributes** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="08b0b-110">Adicionar ou remover um objeto de [**atributo**](attribute.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-110">Add or remove a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="08b0b-111">Limpe a coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-111">Clear the collection.</span></span>
-   <span data-ttu-id="08b0b-112">Recupere o número de atributos na coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-112">Retrieve the number of attributes in the collection.</span></span>
-   <span data-ttu-id="08b0b-113">Recupere um objeto de [**atributo**](attribute.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-113">Retrieve a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="08b0b-114">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="08b0b-115">Membros</span><span class="sxs-lookup"><span data-stu-id="08b0b-115">Members</span></span>

<span data-ttu-id="08b0b-116">O objeto **Attributes** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08b0b-116">The **Attributes** object has these types of members:</span></span>

-   [<span data-ttu-id="08b0b-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="08b0b-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="08b0b-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08b0b-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08b0b-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="08b0b-119">Methods</span></span>

<span data-ttu-id="08b0b-120">O objeto **Attributes** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="08b0b-120">The **Attributes** object has these methods.</span></span>



| <span data-ttu-id="08b0b-121">Método</span><span class="sxs-lookup"><span data-stu-id="08b0b-121">Method</span></span>                              | <span data-ttu-id="08b0b-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="08b0b-122">Description</span></span>                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="08b0b-123">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="08b0b-123">**Add**</span></span>](attributes-add.md)       | <span data-ttu-id="08b0b-124">Adiciona um objeto de [**atributo**](attribute.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-124">Adds an [**Attribute**](attribute.md) object to the collection.</span></span><br/>       |
| [<span data-ttu-id="08b0b-125">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="08b0b-125">**Clear**</span></span>](attributes-clear.md)   | <span data-ttu-id="08b0b-126">Limpa todos os objetos de [**atributo**](attribute.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-126">Clears all [**Attribute**](attribute.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="08b0b-127">**Remover**</span><span class="sxs-lookup"><span data-stu-id="08b0b-127">**Remove**</span></span>](attributes-remove.md) | <span data-ttu-id="08b0b-128">Remove um objeto de [**atributo**](attribute.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-128">Removes an [**Attribute**](attribute.md) object from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="08b0b-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08b0b-129">Properties</span></span>

<span data-ttu-id="08b0b-130">O objeto **Attributes** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08b0b-130">The **Attributes** object has these properties.</span></span>



| <span data-ttu-id="08b0b-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="08b0b-131">Property</span></span>                                           | <span data-ttu-id="08b0b-132">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="08b0b-132">Access type</span></span>          | <span data-ttu-id="08b0b-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="08b0b-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08b0b-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="08b0b-134">**\_NewEnum**</span></span>](attributes-newenum.md)<br/> | <span data-ttu-id="08b0b-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08b0b-135">Read-only</span></span><br/> | <span data-ttu-id="08b0b-136">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="08b0b-137">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="08b0b-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="08b0b-138">**Contar**</span><span class="sxs-lookup"><span data-stu-id="08b0b-138">**Count**</span></span>](attributes-count.md)<br/>       | <span data-ttu-id="08b0b-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08b0b-139">Read-only</span></span><br/> | <span data-ttu-id="08b0b-140">Recupera o número de objetos de [**atributo**](attribute.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="08b0b-140">Retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="08b0b-141">**Item**</span><span class="sxs-lookup"><span data-stu-id="08b0b-141">**Item**</span></span>](attributes-item.md)<br/>         | <span data-ttu-id="08b0b-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08b0b-142">Read-only</span></span><br/> | <span data-ttu-id="08b0b-143">Recupera o objeto de [**atributo**](attribute.md) que representa o atributo indexado.</span><span class="sxs-lookup"><span data-stu-id="08b0b-143">Retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="08b0b-144">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="08b0b-144">This is the default property.</span></span><br/>                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="08b0b-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="08b0b-145">Remarks</span></span>

<span data-ttu-id="08b0b-146">Não é possível criar o objeto **Attributes** .</span><span class="sxs-lookup"><span data-stu-id="08b0b-146">The **Attributes** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b0b-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08b0b-147">Requirements</span></span>



| <span data-ttu-id="08b0b-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b0b-148">Requirement</span></span> | <span data-ttu-id="08b0b-149">Valor</span><span class="sxs-lookup"><span data-stu-id="08b0b-149">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08b0b-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="08b0b-150">End of client support</span></span><br/> | <span data-ttu-id="08b0b-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08b0b-151">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="08b0b-152">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="08b0b-152">End of server support</span></span><br/> | <span data-ttu-id="08b0b-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08b0b-153">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="08b0b-154">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="08b0b-154">Redistributable</span></span><br/>       | <span data-ttu-id="08b0b-155">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="08b0b-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08b0b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="08b0b-156">DLL</span></span><br/>                   | <dl> <span data-ttu-id="08b0b-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b0b-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b0b-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="08b0b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b0b-159">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="08b0b-159">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
