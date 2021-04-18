---
description: Fornece a funcionalidade para o hash de uma cadeia de caracteres.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Objeto HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778685"
---
# <a name="hasheddata-object"></a><span data-ttu-id="0ecea-103">Objeto HashedData</span><span class="sxs-lookup"><span data-stu-id="0ecea-103">HashedData object</span></span>

<span data-ttu-id="0ecea-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0ecea-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0ecea-105">Em vez disso, use a [**classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="0ecea-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0ecea-106">O objeto **HashedData** fornece a funcionalidade para o hash de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0ecea-106">The **HashedData** object provides functionality for hashing a string.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0ecea-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="0ecea-107">When to use</span></span>

<span data-ttu-id="0ecea-108">O objeto **HashedData** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0ecea-108">The **HashedData** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="0ecea-109">Especifique a cadeia de caracteres de conteúdo que contém os dados a serem codificados em hash.</span><span class="sxs-lookup"><span data-stu-id="0ecea-109">Specify the content string that contains the data to be hashed.</span></span>
-   <span data-ttu-id="0ecea-110">Aplique um algoritmo de hash especificado à cadeia de caracteres de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0ecea-110">Apply a specified hash algorithm to the content string.</span></span>

## <a name="members"></a><span data-ttu-id="0ecea-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0ecea-111">Members</span></span>

<span data-ttu-id="0ecea-112">O objeto **HashedData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0ecea-112">The **HashedData** object has these types of members:</span></span>

-   [<span data-ttu-id="0ecea-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ecea-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="0ecea-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ecea-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0ecea-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ecea-115">Methods</span></span>

<span data-ttu-id="0ecea-116">O objeto **HashedData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0ecea-116">The **HashedData** object has these methods.</span></span>



| <span data-ttu-id="0ecea-117">Método</span><span class="sxs-lookup"><span data-stu-id="0ecea-117">Method</span></span>                          | <span data-ttu-id="0ecea-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ecea-118">Description</span></span>                                        |
|:--------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="0ecea-119">**Tralha**</span><span class="sxs-lookup"><span data-stu-id="0ecea-119">**Hash**</span></span>](hasheddata-hash.md) | <span data-ttu-id="0ecea-120">Cria um hash da cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="0ecea-120">Creates a hash of the specified string.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0ecea-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ecea-121">Properties</span></span>

<span data-ttu-id="0ecea-122">O objeto **HashedData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0ecea-122">The **HashedData** object has these properties.</span></span>



| <span data-ttu-id="0ecea-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0ecea-123">Property</span></span>                                             | <span data-ttu-id="0ecea-124">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="0ecea-124">Access type</span></span>           | <span data-ttu-id="0ecea-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ecea-125">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ecea-126">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="0ecea-126">**Algorithm**</span></span>](hasheddata-algorithm.md)<br/> | <span data-ttu-id="0ecea-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0ecea-127">Read/write</span></span><br/> | <span data-ttu-id="0ecea-128">Define ou recupera o tipo de algoritmo de hash usado.</span><span class="sxs-lookup"><span data-stu-id="0ecea-128">Sets or retrieves the type of hashing algorithm used.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="0ecea-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0ecea-129">**Value**</span></span>](hasheddata-value.md)<br/>         | <span data-ttu-id="0ecea-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ecea-130">Read-only</span></span><br/>  | <span data-ttu-id="0ecea-131">Recupera os dados com hash após chamadas bem-sucedidas para o método de [**hash**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="0ecea-131">Retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="0ecea-132">O hash é retornado no formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="0ecea-132">The hash is returned in hexadecimal format.</span></span> <span data-ttu-id="0ecea-133">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="0ecea-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ecea-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ecea-134">Remarks</span></span>

<span data-ttu-id="0ecea-135">Para criar o hash de uma grande quantidade de dados, chame o método de [**hash**](hasheddata-hash.md) para cada dado.</span><span class="sxs-lookup"><span data-stu-id="0ecea-135">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="0ecea-136">O hash de cada parte dos dados é concatenado à propriedade [**Value**](hasheddata-value.md) até que a propriedade seja lida.</span><span class="sxs-lookup"><span data-stu-id="0ecea-136">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="0ecea-137">O conteúdo da propriedade **Value** é redefinido quando a propriedade é lida.</span><span class="sxs-lookup"><span data-stu-id="0ecea-137">The contents of the **Value** property are reset when the property is read.</span></span>

<span data-ttu-id="0ecea-138">O objeto **HashedData** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="0ecea-138">The **HashedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="0ecea-139">O ProgID do objeto **HashedData** é "CAPICOM. HashedData. 1 ".</span><span class="sxs-lookup"><span data-stu-id="0ecea-139">The ProgID for the **HashedData** object is "CAPICOM.HashedData.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="0ecea-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ecea-140">Requirements</span></span>



| <span data-ttu-id="0ecea-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ecea-141">Requirement</span></span> | <span data-ttu-id="0ecea-142">Valor</span><span class="sxs-lookup"><span data-stu-id="0ecea-142">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ecea-143">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0ecea-143">End of client support</span></span><br/> | <span data-ttu-id="0ecea-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ecea-144">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0ecea-145">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0ecea-145">End of server support</span></span><br/> | <span data-ttu-id="0ecea-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ecea-146">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0ecea-147">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0ecea-147">Redistributable</span></span><br/>       | <span data-ttu-id="0ecea-148">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ecea-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0ecea-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0ecea-149">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0ecea-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ecea-150"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
