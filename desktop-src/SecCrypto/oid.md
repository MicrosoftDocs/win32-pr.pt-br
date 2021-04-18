---
description: Representa um OID (identificador de objeto) que é usado por várias propriedades de CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Objeto OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778676"
---
# <a name="oid-object"></a><span data-ttu-id="5b4b9-103">Objeto OID</span><span class="sxs-lookup"><span data-stu-id="5b4b9-103">OID object</span></span>

<span data-ttu-id="5b4b9-104">\[O objeto **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-104">\[The **OID** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5b4b9-105">Em vez disso, use a [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5b4b9-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5b4b9-106">O objeto **OID** representa um OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) que é usado por várias propriedades CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-106">The **OID** object represents an [*object identifier*](../secgloss/o-gly.md) (OID) that is used by several CAPICOM properties.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5b4b9-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="5b4b9-107">When to use</span></span>

<span data-ttu-id="5b4b9-108">O objeto **OID** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="5b4b9-108">The **OID** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5b4b9-109">Defina ou recupere um nome de capicor e o nome de exibição para o OID.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-109">Set or retrieve a CAPICOM name and display name for the OID.</span></span>
-   <span data-ttu-id="5b4b9-110">Defina ou recupere o número pontilhado para o OID.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-110">Set or retrieve the dotted number for the OID.</span></span>

## <a name="members"></a><span data-ttu-id="5b4b9-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5b4b9-111">Members</span></span>

<span data-ttu-id="5b4b9-112">O objeto **OID** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b4b9-112">The **OID** object has these types of members:</span></span>

-   [<span data-ttu-id="5b4b9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b4b9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b4b9-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b4b9-114">Properties</span></span>

<span data-ttu-id="5b4b9-115">O objeto **OID** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-115">The **OID** object has these properties.</span></span>



| <span data-ttu-id="5b4b9-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5b4b9-116">Property</span></span>                                            | <span data-ttu-id="5b4b9-117">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5b4b9-117">Access type</span></span>           | <span data-ttu-id="5b4b9-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b4b9-118">Description</span></span>                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b4b9-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="5b4b9-119">**FriendlyName**</span></span>](oid-friendlyname.md)<br/> | <span data-ttu-id="5b4b9-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b4b9-120">Read/write</span></span><br/> | <span data-ttu-id="5b4b9-121">Define ou recupera o nome de exibição para o OID.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-121">Sets or retrieves the display name for the OID.</span></span><br/>                                       |
| [<span data-ttu-id="5b4b9-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5b4b9-122">**Name**</span></span>](oid-name.md)<br/>                 | <span data-ttu-id="5b4b9-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b4b9-123">Read/write</span></span><br/> | <span data-ttu-id="5b4b9-124">Define ou recupera o nome definido pelo CAPICOM para o OID.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-124">Sets or retrieves the CAPICOM-defined name for the OID.</span></span> <span data-ttu-id="5b4b9-125">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-125">This is the default property.</span></span><br/> |
| [<span data-ttu-id="5b4b9-126">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5b4b9-126">**Value**</span></span>](oid-value.md)<br/>               | <span data-ttu-id="5b4b9-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b4b9-127">Read/write</span></span><br/> | <span data-ttu-id="5b4b9-128">Define ou recupera o valor do número pontilhado OID do OID.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-128">Sets or retrieves the value of the OID dotted number of the OID.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="5b4b9-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b4b9-129">Remarks</span></span>

<span data-ttu-id="5b4b9-130">O objeto **OID** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-130">The **OID** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="5b4b9-131">O ProgID para o objeto **OID** é CAPICOM. OID. 1.</span><span class="sxs-lookup"><span data-stu-id="5b4b9-131">The ProgID for the **OID** object is CAPICOM.OID.1.</span></span>

<span data-ttu-id="5b4b9-132">As seguintes propriedades de objeto capicor retornam um objeto **OID** :</span><span class="sxs-lookup"><span data-stu-id="5b4b9-132">The following CAPICOM object properties return an **OID** object:</span></span>

-   [<span data-ttu-id="5b4b9-133">**PolicyInformation. OID**</span><span class="sxs-lookup"><span data-stu-id="5b4b9-133">**PolicyInformation.OID**</span></span>](policyinformation-oid.md)
-   [<span data-ttu-id="5b4b9-134">**Qualifier. OID**</span><span class="sxs-lookup"><span data-stu-id="5b4b9-134">**Qualifier.OID**</span></span>](qualifier-oid.md)
-   [<span data-ttu-id="5b4b9-135">**Extensão. OID**</span><span class="sxs-lookup"><span data-stu-id="5b4b9-135">**Extension.OID**</span></span>](extension-oid.md)
-   [<span data-ttu-id="5b4b9-136">**Modelo. OID**</span><span class="sxs-lookup"><span data-stu-id="5b4b9-136">**Template.OID**</span></span>](template-oid.md)

## <a name="requirements"></a><span data-ttu-id="5b4b9-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b4b9-137">Requirements</span></span>



| <span data-ttu-id="5b4b9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b4b9-138">Requirement</span></span> | <span data-ttu-id="5b4b9-139">Valor</span><span class="sxs-lookup"><span data-stu-id="5b4b9-139">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4b9-140">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5b4b9-140">Redistributable</span></span><br/> | <span data-ttu-id="5b4b9-141">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5b4b9-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5b4b9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5b4b9-142">DLL</span></span><br/>             | <dl> <span data-ttu-id="5b4b9-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b4b9-143"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
