---
description: Representa a extensão de restrições básicas de um certificado.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Objeto BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766831"
---
# <a name="basicconstraints-object"></a><span data-ttu-id="d53bb-103">Objeto BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="d53bb-103">BasicConstraints object</span></span>

<span data-ttu-id="d53bb-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d53bb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d53bb-105">Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="d53bb-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="d53bb-106">O objeto **BasicConstraints** representa a extensão de restrições básicas de um certificado.</span><span class="sxs-lookup"><span data-stu-id="d53bb-106">The **BasicConstraints** object represents the basic constraints extension of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d53bb-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="d53bb-107">When to use</span></span>

<span data-ttu-id="d53bb-108">O objeto **BasicConstraints** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="d53bb-108">The **BasicConstraints** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d53bb-109">Determine se a extensão de restrições básicas está presente.</span><span class="sxs-lookup"><span data-stu-id="d53bb-109">Determine whether the basic constraints extension is present.</span></span>
-   <span data-ttu-id="d53bb-110">Determine se a extensão de restrições básicas está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="d53bb-110">Determine whether the basic constraints extension is marked critical.</span></span>
-   <span data-ttu-id="d53bb-111">Determine se o certificado está restrito às autoridades de certificação.</span><span class="sxs-lookup"><span data-stu-id="d53bb-111">Determine whether the certificate is constrained to certificate authorities.</span></span>
-   <span data-ttu-id="d53bb-112">Determine se a restrição de comprimento do caminho está presente e recupere o valor da restrição de comprimento do caminho.</span><span class="sxs-lookup"><span data-stu-id="d53bb-112">Determine whether the path length constraint is present and retrieve the path length constraint value.</span></span>

## <a name="members"></a><span data-ttu-id="d53bb-113">Membros</span><span class="sxs-lookup"><span data-stu-id="d53bb-113">Members</span></span>

<span data-ttu-id="d53bb-114">O objeto **BasicConstraints** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d53bb-114">The **BasicConstraints** object has these types of members:</span></span>

-   [<span data-ttu-id="d53bb-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d53bb-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d53bb-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d53bb-116">Properties</span></span>

<span data-ttu-id="d53bb-117">O objeto **BasicConstraints** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d53bb-117">The **BasicConstraints** object has these properties.</span></span>



| <span data-ttu-id="d53bb-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d53bb-118">Property</span></span>                                                                                     | <span data-ttu-id="d53bb-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="d53bb-119">Access type</span></span>          | <span data-ttu-id="d53bb-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d53bb-120">Description</span></span>                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d53bb-121">**IsCertificateAuthority**</span><span class="sxs-lookup"><span data-stu-id="d53bb-121">**IsCertificateAuthority**</span></span>](basicconstraints-iscertificateauthority.md)<br/>         | <span data-ttu-id="d53bb-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d53bb-122">Read-only</span></span><br/> | <span data-ttu-id="d53bb-123">Recupera um valor booliano que indica se o certificado é para uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="d53bb-123">Retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span><br/> |
| [<span data-ttu-id="d53bb-124">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="d53bb-124">**IsCritical**</span></span>](basicconstraints-iscritical.md)<br/>                                 | <span data-ttu-id="d53bb-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d53bb-125">Read-only</span></span><br/> | <span data-ttu-id="d53bb-126">Recupera um valor booliano que indica se a extensão de restrição básica está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="d53bb-126">Retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="d53bb-127">**IsPathLenConstraintPresent**</span><span class="sxs-lookup"><span data-stu-id="d53bb-127">**IsPathLenConstraintPresent**</span></span>](basicconstraints-ispathlenconstraintpresent.md)<br/> | <span data-ttu-id="d53bb-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d53bb-128">Read-only</span></span><br/> | <span data-ttu-id="d53bb-129">Recupera um valor booliano que indica se a restrição de comprimento de caminho do certificado está presente.</span><span class="sxs-lookup"><span data-stu-id="d53bb-129">Retrieves a Boolean value that indicates whether the certificate's path length constraint is present.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d53bb-130">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="d53bb-130">**IsPresent**</span></span>](basicconstraints-ispresent.md)<br/>                                   | <span data-ttu-id="d53bb-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d53bb-131">Read-only</span></span><br/> | <span data-ttu-id="d53bb-132">Recupera um valor booliano que indica se a extensão de restrições básica está presente.</span><span class="sxs-lookup"><span data-stu-id="d53bb-132">Retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="d53bb-133">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="d53bb-133">This is the default property.</span></span><br/>                                                                              |
| [<span data-ttu-id="d53bb-134">**PathLenConstraint**</span><span class="sxs-lookup"><span data-stu-id="d53bb-134">**PathLenConstraint**</span></span>](basicconstraints-pathlenconstraint.md)<br/>                   | <span data-ttu-id="d53bb-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d53bb-135">Read-only</span></span><br/> | <span data-ttu-id="d53bb-136">Recupera o valor da restrição de comprimento do caminho.</span><span class="sxs-lookup"><span data-stu-id="d53bb-136">Retrieves the value of the path length constraint.</span></span><br/>                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d53bb-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="d53bb-137">Remarks</span></span>

<span data-ttu-id="d53bb-138">O objeto **BasicConstraints** não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="d53bb-138">The **BasicConstraints** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d53bb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d53bb-139">Requirements</span></span>



| <span data-ttu-id="d53bb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d53bb-140">Requirement</span></span> | <span data-ttu-id="d53bb-141">Valor</span><span class="sxs-lookup"><span data-stu-id="d53bb-141">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d53bb-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d53bb-142">End of client support</span></span><br/> | <span data-ttu-id="d53bb-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d53bb-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d53bb-144">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d53bb-144">End of server support</span></span><br/> | <span data-ttu-id="d53bb-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d53bb-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d53bb-146">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d53bb-146">Redistributable</span></span><br/>       | <span data-ttu-id="d53bb-147">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d53bb-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d53bb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d53bb-148">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d53bb-149"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d53bb-149"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d53bb-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="d53bb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53bb-151">Objetos de criptografia</span><span class="sxs-lookup"><span data-stu-id="d53bb-151">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
