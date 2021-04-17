---
description: Representa uma coleção de objetos de signatário.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Objeto de assinantes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787450"
---
# <a name="signers-object"></a><span data-ttu-id="633fe-103">Objeto de assinantes</span><span class="sxs-lookup"><span data-stu-id="633fe-103">Signers object</span></span>

<span data-ttu-id="633fe-104">\[O objeto de **assinantes** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="633fe-104">\[The **Signers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="633fe-105">Em vez disso, use uma coleção de objetos CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="633fe-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="633fe-106">Para obter mais informações, consulte a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="633fe-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="633fe-107">O **objeto de** signatários representa uma coleção de objetos de [**assinante**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="633fe-107">The **Signers** object represents a collection of [**Signer**](signer.md) objects.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="633fe-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="633fe-108">When to use</span></span>

<span data-ttu-id="633fe-109">O objeto de **assinantes** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="633fe-109">The **Signers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="633fe-110">Recupere o número de certificados na coleção.</span><span class="sxs-lookup"><span data-stu-id="633fe-110">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="633fe-111">Recupere um objeto de **assinantes** específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="633fe-111">Retrieve a specific **Signers** object from the collection.</span></span>
-   <span data-ttu-id="633fe-112">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="633fe-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="633fe-113">Membros</span><span class="sxs-lookup"><span data-stu-id="633fe-113">Members</span></span>

<span data-ttu-id="633fe-114">O objeto de **assinantes** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="633fe-114">The **Signers** object has these types of members:</span></span>

-   [<span data-ttu-id="633fe-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="633fe-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="633fe-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="633fe-116">Properties</span></span>

<span data-ttu-id="633fe-117">O objeto de **assinantes** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="633fe-117">The **Signers** object has these properties.</span></span>



| <span data-ttu-id="633fe-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="633fe-118">Property</span></span>                                        | <span data-ttu-id="633fe-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="633fe-119">Access type</span></span>          | <span data-ttu-id="633fe-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="633fe-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="633fe-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="633fe-121">**\_NewEnum**</span></span>](signers-newenum.md)<br/> | <span data-ttu-id="633fe-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633fe-122">Read-only</span></span><br/> | <span data-ttu-id="633fe-123">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="633fe-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="633fe-124">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="633fe-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="633fe-125">**Contar**</span><span class="sxs-lookup"><span data-stu-id="633fe-125">**Count**</span></span>](signers-count.md)<br/>       | <span data-ttu-id="633fe-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633fe-126">Read-only</span></span><br/> | <span data-ttu-id="633fe-127">Número de objetos de [**signatário**](signer.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="633fe-127">Number of [**Signer**](signer.md) objects in the collection.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="633fe-128">**Item**</span><span class="sxs-lookup"><span data-stu-id="633fe-128">**Item**</span></span>](signers-item.md)<br/>         | <span data-ttu-id="633fe-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633fe-129">Read-only</span></span><br/> | <span data-ttu-id="633fe-130">Recupera o objeto de [**signatário**](signer.md) que representa o assinante indexado.</span><span class="sxs-lookup"><span data-stu-id="633fe-130">Retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="633fe-131">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="633fe-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="633fe-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="633fe-132">Remarks</span></span>

<span data-ttu-id="633fe-133">Não é possível criar o objeto de **assinantes** .</span><span class="sxs-lookup"><span data-stu-id="633fe-133">The **Signers** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="633fe-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="633fe-134">Requirements</span></span>



| <span data-ttu-id="633fe-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="633fe-135">Requirement</span></span> | <span data-ttu-id="633fe-136">Valor</span><span class="sxs-lookup"><span data-stu-id="633fe-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="633fe-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="633fe-137">Redistributable</span></span><br/> | <span data-ttu-id="633fe-138">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="633fe-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="633fe-139">DLL</span><span class="sxs-lookup"><span data-stu-id="633fe-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="633fe-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="633fe-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633fe-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="633fe-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633fe-142">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="633fe-142">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
