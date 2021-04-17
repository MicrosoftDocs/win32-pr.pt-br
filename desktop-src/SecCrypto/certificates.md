---
description: Representa uma coleção de objetos de certificado.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Objeto de certificados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751073"
---
# <a name="certificates-object"></a><span data-ttu-id="e6cb6-103">Objeto de certificados</span><span class="sxs-lookup"><span data-stu-id="e6cb6-103">Certificates object</span></span>

<span data-ttu-id="e6cb6-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e6cb6-105">Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e6cb6-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e6cb6-106">O objeto **Certificates** representa uma coleção de objetos de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="e6cb6-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="e6cb6-107">Cada objeto de [**certificado**](certificate.md) representa um único [*certificado digital*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e6cb6-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="e6cb6-108">O objeto **Certificates** expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="e6cb6-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="e6cb6-109">**ICertificates2**: introduzido no capicom 2,0.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="e6cb6-110">**ICertificates**: introduzido no capicom 1,0.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e6cb6-111">Quando usar</span><span class="sxs-lookup"><span data-stu-id="e6cb6-111">When to use</span></span>

<span data-ttu-id="e6cb6-112">O objeto **Certificates** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="e6cb6-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e6cb6-113">Adicionar ou remover um objeto de [**certificado**](certificate.md) de ou para a coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="e6cb6-114">Gere um subconjunto da coleção encontrando um conjunto de certificados ou exibindo uma caixa de diálogo para selecionar os certificados.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="e6cb6-115">Limpe todos os objetos de [**certificado**](certificate.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="e6cb6-116">Recupere o número de certificados na coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="e6cb6-117">Recupere um objeto de [**certificado**](certificate.md) específico da coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="e6cb6-118">Iterar pela coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="e6cb6-119">Membros</span><span class="sxs-lookup"><span data-stu-id="e6cb6-119">Members</span></span>

<span data-ttu-id="e6cb6-120">O objeto **Certificates** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e6cb6-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="e6cb6-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6cb6-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6cb6-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6cb6-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6cb6-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6cb6-123">Methods</span></span>

<span data-ttu-id="e6cb6-124">O objeto **Certificates** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="e6cb6-125">Método</span><span class="sxs-lookup"><span data-stu-id="e6cb6-125">Method</span></span>                                | <span data-ttu-id="e6cb6-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6cb6-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6cb6-127">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="e6cb6-128">Adiciona um objeto de [**certificado**](certificate.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="e6cb6-129">(Herdado de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="e6cb6-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="e6cb6-130">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="e6cb6-131">Remove todos os objetos de [**certificado**](certificate.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="e6cb6-132">(Herdado de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="e6cb6-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="e6cb6-133">**Localizar**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="e6cb6-134">Retorna um objeto **Certificates** que contém todos os certificados que correspondem aos critérios de pesquisa especificados.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="e6cb6-135">(Herdado de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="e6cb6-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="e6cb6-136">**Remover**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="e6cb6-137">Remove um único objeto de [**certificado**](certificate.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="e6cb6-138">(Herdado de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="e6cb6-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="e6cb6-139">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="e6cb6-140">Salva os certificados em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="e6cb6-141">(Herdado de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="e6cb6-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="e6cb6-142">**Não**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="e6cb6-143">Exibe uma caixa de diálogo para selecionar certificados e retorna uma coleção desses certificados selecionados.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="e6cb6-144">(Herdado de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="e6cb6-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="e6cb6-145">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6cb6-145">Properties</span></span>

<span data-ttu-id="e6cb6-146">O objeto **Certificates** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="e6cb6-147">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e6cb6-147">Property</span></span>                                             | <span data-ttu-id="e6cb6-148">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="e6cb6-148">Access type</span></span>          | <span data-ttu-id="e6cb6-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6cb6-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6cb6-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="e6cb6-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb6-151">Read-only</span></span><br/> | <span data-ttu-id="e6cb6-152">Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e6cb6-153">Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e6cb6-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="e6cb6-154">**Contar**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="e6cb6-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb6-155">Read-only</span></span><br/> | <span data-ttu-id="e6cb6-156">Recupera o número de objetos de [**certificado**](certificate.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="e6cb6-157">**Item**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="e6cb6-158">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb6-158">Read-only</span></span><br/> | <span data-ttu-id="e6cb6-159">Recupera um objeto de [**certificado**](certificate.md) que representa o certificado indexado da coleção.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="e6cb6-160">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-160">This is the default property.</span></span><br/> <span data-ttu-id="e6cb6-161">(Herdado de **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="e6cb6-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="e6cb6-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6cb6-162">Remarks</span></span>

<span data-ttu-id="e6cb6-163">O objeto **Certificates** pode ser criado e é seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="e6cb6-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="e6cb6-164">O ProgID do objeto de **certificados** é "CAPICOM. Certificados. 2 ".</span><span class="sxs-lookup"><span data-stu-id="e6cb6-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="e6cb6-165">**CAPICOM 1. *x*:** o ProgID para o objeto de **certificados** é "CAPICOM. Certificates. 1 ".</span><span class="sxs-lookup"><span data-stu-id="e6cb6-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="e6cb6-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6cb6-166">Requirements</span></span>



| <span data-ttu-id="e6cb6-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6cb6-167">Requirement</span></span> | <span data-ttu-id="e6cb6-168">Valor</span><span class="sxs-lookup"><span data-stu-id="e6cb6-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cb6-169">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e6cb6-169">End of client support</span></span><br/> | <span data-ttu-id="e6cb6-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6cb6-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e6cb6-171">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e6cb6-171">End of server support</span></span><br/> | <span data-ttu-id="e6cb6-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6cb6-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e6cb6-173">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e6cb6-173">Redistributable</span></span><br/>       | <span data-ttu-id="e6cb6-174">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e6cb6-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e6cb6-175">DLL</span><span class="sxs-lookup"><span data-stu-id="e6cb6-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e6cb6-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6cb6-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6cb6-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6cb6-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6cb6-178">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="e6cb6-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
