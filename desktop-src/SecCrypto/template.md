---
description: Representa o modelo de extensão de certificado do certificado.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Objeto de modelo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750492"
---
# <a name="template-object"></a><span data-ttu-id="0e068-103">Objeto de modelo</span><span class="sxs-lookup"><span data-stu-id="0e068-103">Template object</span></span>

<span data-ttu-id="0e068-104">\[O objeto de **modelo** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="0e068-104">\[The **Template** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0e068-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="0e068-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="0e068-106">O objeto de **modelo** representa o modelo de extensão de certificado do certificado.</span><span class="sxs-lookup"><span data-stu-id="0e068-106">The **Template** object represents the certificate extension template of the certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="0e068-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="0e068-107">When to use</span></span>

<span data-ttu-id="0e068-108">O objeto de **modelo** é usado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0e068-108">The **Template** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="0e068-109">Determine se o modelo está marcado como crítico ou presente.</span><span class="sxs-lookup"><span data-stu-id="0e068-109">Determine whether the template is marked critical or present.</span></span>
-   <span data-ttu-id="0e068-110">Recupere o [*identificador de objeto*](../secgloss/o-gly.md) (OID) ou o nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e068-110">Retrieve the [*object identifier*](../secgloss/o-gly.md) (OID) or name of the template.</span></span>
-   <span data-ttu-id="0e068-111">Recupere a versão secundária ou principal do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e068-111">Retrieve the minor or major version of the template.</span></span>

## <a name="members"></a><span data-ttu-id="0e068-112">Membros</span><span class="sxs-lookup"><span data-stu-id="0e068-112">Members</span></span>

<span data-ttu-id="0e068-113">O objeto de **modelo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0e068-113">The **Template** object has these types of members:</span></span>

-   [<span data-ttu-id="0e068-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0e068-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e068-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0e068-115">Properties</span></span>

<span data-ttu-id="0e068-116">O objeto de **modelo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0e068-116">The **Template** object has these properties.</span></span>



| <span data-ttu-id="0e068-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0e068-117">Property</span></span>                                                 | <span data-ttu-id="0e068-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="0e068-118">Access type</span></span>          | <span data-ttu-id="0e068-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e068-119">Description</span></span>                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e068-120">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="0e068-120">**IsCritical**</span></span>](template-iscritical.md)<br/>     | <span data-ttu-id="0e068-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e068-121">Read-only</span></span><br/> | <span data-ttu-id="0e068-122">Recupera um valor booliano que indica se a extensão do modelo está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="0e068-122">Retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="0e068-123">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="0e068-123">**IsPresent**</span></span>](template-ispresent.md)<br/>       | <span data-ttu-id="0e068-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e068-124">Read-only</span></span><br/> | <span data-ttu-id="0e068-125">Recupera um valor booliano que indica se a extensão do modelo está presente.</span><span class="sxs-lookup"><span data-stu-id="0e068-125">Retrieves a Boolean value that indicates whether the template extension is present.</span></span><br/>         |
| [<span data-ttu-id="0e068-126">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="0e068-126">**MajorVersion**</span></span>](template-majorversion.md)<br/> | <span data-ttu-id="0e068-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e068-127">Read-only</span></span><br/> | <span data-ttu-id="0e068-128">Recupera o número de versão principal do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e068-128">Retrieves the major version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="0e068-129">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="0e068-129">**MinorVersion**</span></span>](template-minorversion.md)<br/> | <span data-ttu-id="0e068-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e068-130">Read-only</span></span><br/> | <span data-ttu-id="0e068-131">Recupera o número de versão secundária do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e068-131">Retrieves the minor version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="0e068-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0e068-132">**Name**</span></span>](template-name.md)<br/>                 | <span data-ttu-id="0e068-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e068-133">Read-only</span></span><br/> | <span data-ttu-id="0e068-134">Recupera uma cadeia de caracteres que contém o nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e068-134">Retrieves a string that contains the name of the template.</span></span><br/>                                  |
| [<span data-ttu-id="0e068-135">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="0e068-135">**OID**</span></span>](template-oid.md)<br/>                   | <span data-ttu-id="0e068-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e068-136">Read-only</span></span><br/> | <span data-ttu-id="0e068-137">Recupera um objeto [**OID**](oid.md) que identifica o objeto de **modelo** .</span><span class="sxs-lookup"><span data-stu-id="0e068-137">Retrieves an [**OID**](oid.md) object that identifies the **Template** object.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="0e068-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e068-138">Remarks</span></span>

<span data-ttu-id="0e068-139">Não é possível criar o objeto de **modelo** .</span><span class="sxs-lookup"><span data-stu-id="0e068-139">The **Template** object cannot be created.</span></span>

<span data-ttu-id="0e068-140">Um objeto de **modelo** é retornado pelo método [**Certificate. Template**](certificate-template.md) .</span><span class="sxs-lookup"><span data-stu-id="0e068-140">A **Template** object is returned by the [**Certificate.Template**](certificate-template.md) method.</span></span>

<span data-ttu-id="0e068-141">O CAPICOM usa duas versões diferentes dos modelos de certificado.</span><span class="sxs-lookup"><span data-stu-id="0e068-141">CAPICOM uses two different versions of certificate templates.</span></span> <span data-ttu-id="0e068-142">A tabela a seguir mostra o nome e o OID para cada versão do modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="0e068-142">The following table shows the name and OID for each certificate template version.</span></span>



| <span data-ttu-id="0e068-143">Versão</span><span class="sxs-lookup"><span data-stu-id="0e068-143">Version</span></span> | <span data-ttu-id="0e068-144">Nome</span><span class="sxs-lookup"><span data-stu-id="0e068-144">Name</span></span>                               | <span data-ttu-id="0e068-145">OID</span><span class="sxs-lookup"><span data-stu-id="0e068-145">OID</span></span>                    |
|---------|------------------------------------|------------------------|
| <span data-ttu-id="0e068-146">V1</span><span class="sxs-lookup"><span data-stu-id="0e068-146">V1</span></span>      | <span data-ttu-id="0e068-147">\_ \_ extensão certtype de registro szOID \_</span><span class="sxs-lookup"><span data-stu-id="0e068-147">szOID\_ENROLL\_CERTTYPE\_EXTENSION</span></span> | <span data-ttu-id="0e068-148">"1.3.6.1.4.1.311.20.2"</span><span class="sxs-lookup"><span data-stu-id="0e068-148">"1.3.6.1.4.1.311.20.2"</span></span> |
| <span data-ttu-id="0e068-149">V2</span><span class="sxs-lookup"><span data-stu-id="0e068-149">V2</span></span>      | <span data-ttu-id="0e068-150">\_modelo de certificado szOID \_</span><span class="sxs-lookup"><span data-stu-id="0e068-150">szOID\_CERTIFICATE\_TEMPLATE</span></span>       | <span data-ttu-id="0e068-151">"1.3.6.1.4.1.311.21.7"</span><span class="sxs-lookup"><span data-stu-id="0e068-151">"1.3.6.1.4.1.311.21.7"</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0e068-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e068-152">Requirements</span></span>



| <span data-ttu-id="0e068-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e068-153">Requirement</span></span> | <span data-ttu-id="0e068-154">Valor</span><span class="sxs-lookup"><span data-stu-id="0e068-154">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e068-155">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0e068-155">Redistributable</span></span><br/> | <span data-ttu-id="0e068-156">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e068-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0e068-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0e068-157">DLL</span></span><br/>             | <dl> <span data-ttu-id="0e068-158"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e068-158"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
