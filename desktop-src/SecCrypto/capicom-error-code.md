---
description: Define os códigos de erro retornados pelo CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Enumeração de CAPICOM_ERROR_CODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756561"
---
# <a name="capicom_error_code-enumeration"></a><span data-ttu-id="76b06-103">Enumeração de código de \_ erro CApicom \_</span><span class="sxs-lookup"><span data-stu-id="76b06-103">CAPICOM\_ERROR\_CODE enumeration</span></span>

<span data-ttu-id="76b06-104">O tipo de enumeração de **\_ \_ código de erro capicod** define códigos de erro que são retornados pelo CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="76b06-104">The **CAPICOM\_ERROR\_CODE** enumeration type defines error codes that are returned by CAPICOM.</span></span>

> [!Note]  
> <span data-ttu-id="76b06-105">Visual Basic Scripting Edition erros retornam um valor **Err. Number** maior que zero.</span><span class="sxs-lookup"><span data-stu-id="76b06-105">Visual Basic Scripting Edition errors return an **Err.number** value greater than zero.</span></span> <span data-ttu-id="76b06-106">Para esses erros, os valores **Err. Description** fornecem informações sobre a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="76b06-106">For those errors, **Err.Description** values provide information about the cause of the error.</span></span> <span data-ttu-id="76b06-107">Além dos erros de Visual Basic Scripting Edition, os erros CAPICOM retornam os códigos definidos pelo **\_ \_ código de erro CAPICOM**.</span><span class="sxs-lookup"><span data-stu-id="76b06-107">In addition to Visual Basic Scripting Edition errors, CAPICOM errors return the codes defined by **CAPICOM\_ERROR\_CODE**.</span></span>

 

## <a name="members"></a><span data-ttu-id="76b06-108">Membros</span><span class="sxs-lookup"><span data-stu-id="76b06-108">Members</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76b06-109">Membro</span><span class="sxs-lookup"><span data-stu-id="76b06-109">Member</span></span></th>
<th><span data-ttu-id="76b06-110">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="76b06-110">Description</span></span></th>
<th><span data-ttu-id="76b06-111">Valor</span><span class="sxs-lookup"><span data-stu-id="76b06-111">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76b06-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="76b06-113">Um tipo de codificação inválido foi usado.</span><span class="sxs-lookup"><span data-stu-id="76b06-113">An encoding type that is not valid was used.</span></span><br/> <span data-ttu-id="76b06-114">A lista a seguir mostra os tipos de codificação válidos:</span><span class="sxs-lookup"><span data-stu-id="76b06-114">The following list shows the valid encoding types:</span></span>
<ul>
<li><span data-ttu-id="76b06-115">CAPICOM_ENCODE_ANY</span><span class="sxs-lookup"><span data-stu-id="76b06-115">CAPICOM_ENCODE_ANY</span></span></li>
<li><span data-ttu-id="76b06-116">CAPICOM_ENCODE_BASE64</span><span class="sxs-lookup"><span data-stu-id="76b06-116">CAPICOM_ENCODE_BASE64</span></span></li>
<li><span data-ttu-id="76b06-117">CAPICOM_ENCODE_BINARY</span><span class="sxs-lookup"><span data-stu-id="76b06-117">CAPICOM_ENCODE_BINARY</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="76b06-118">0x80880100</span><span class="sxs-lookup"><span data-stu-id="76b06-118">0x80880100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span></span></td>
<td><span data-ttu-id="76b06-120">A propriedade <a href="eku-oid.md"><strong>OID</strong></a> do objeto <a href="eku.md"><strong>EKU</strong></a> não pode ser definida porque a propriedade <a href="eku-name.md"><strong>Name</strong></a> não está definida como CAPICOM_EKU_OTHER.</span><span class="sxs-lookup"><span data-stu-id="76b06-120">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object cannot be set because the <a href="eku-name.md"><strong>Name</strong></a> property is not set to CAPICOM_EKU_OTHER.</span></span><br/> <span data-ttu-id="76b06-121">Defina a propriedade <a href="eku-name.md"><strong>Name</strong></a> como CAPICOM_EKU_OTHER antes de definir a propriedade <a href="eku-oid.md"><strong>OID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-121">Set the <a href="eku-name.md"><strong>Name</strong></a> property to CAPICOM_EKU_OTHER before setting the <a href="eku-oid.md"><strong>OID</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="76b06-122">0x80880200</span><span class="sxs-lookup"><span data-stu-id="76b06-122">0x80880200</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-124">A propriedade <a href="eku-oid.md"><strong>OID</strong></a> do objeto <a href="eku.md"><strong>EKU</strong></a> não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="76b06-124">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-125">Defina a propriedade <a href="eku-name.md"><strong>Name</strong></a> para qualquer coisa diferente de CAPICOM_EKU_OTHER, ou defina a propriedade <strong>Name</strong> como CAPICOM_EKU_OTHER e a propriedade <a href="eku-oid.md"><strong>OID</strong></a> como um valor.</span><span class="sxs-lookup"><span data-stu-id="76b06-125">Either set the <a href="eku-name.md"><strong>Name</strong></a> property to anything other than CAPICOM_EKU_OTHER, or set the <strong>Name</strong> property to CAPICOM_EKU_OTHER and the <a href="eku-oid.md"><strong>OID</strong></a> property to a value.</span></span><br/></td>
<td><span data-ttu-id="76b06-126">0x80880201</span><span class="sxs-lookup"><span data-stu-id="76b06-126">0x80880201</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-128">O objeto de <a href="certificate.md"><strong>certificado</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-128">The <a href="certificate.md"><strong>Certificate</strong></a> object has not been initialized.</span></span><br/> <span data-ttu-id="76b06-129">Normalmente, esse código de erro é retornado quando um objeto de <a href="certificate.md"><strong>certificado</strong></a> é instanciado, mas não associado a um certificado digital.</span><span class="sxs-lookup"><span data-stu-id="76b06-129">Usually, this error code is returned when a <a href="certificate.md"><strong>Certificate</strong></a> object is instantiated but not associated with a digital certificate.</span></span> <span data-ttu-id="76b06-130">Para associar o objeto a um certificado digital, atribua-o a um objeto de <strong>certificado</strong> existente ou chame o método de <a href="certificate-import.md"><strong>importação</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-130">To associate the object with a digital certificate, either assign it to an existing <strong>Certificate</strong> object or call the <a href="certificate-import.md"><strong>Import</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-131">0x80880210</span><span class="sxs-lookup"><span data-stu-id="76b06-131">0x80880210</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span></span></td>
<td><span data-ttu-id="76b06-133">O objeto de <a href="certificate.md"><strong>certificado</strong></a> não tem uma chave privada associada.</span><span class="sxs-lookup"><span data-stu-id="76b06-133">The <a href="certificate.md"><strong>Certificate</strong></a> object does not have an associated private key.</span></span><br/> <span data-ttu-id="76b06-134">Esse código de erro é retornado quando é feita uma tentativa de assinar dados usando a chave privada do signatário, mas o objeto de <a href="certificate.md"><strong>certificado</strong></a> associado ao objeto de <a href="signer.md"><strong>signatário</strong></a> não pode ser usado para a operação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="76b06-134">This error code is returned when an attempt is made to sign data using the signer's private key, but the <a href="certificate.md"><strong>Certificate</strong></a> object that is associated with the <a href="signer.md"><strong>Signer</strong></a> object cannot be used for the signing operation.</span></span><br/></td>
<td><span data-ttu-id="76b06-135">0x80880211</span><span class="sxs-lookup"><span data-stu-id="76b06-135">0x80880211</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span></span></td>
<td><span data-ttu-id="76b06-137">O objeto de <a href="chain.md"><strong>cadeia</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-137">The <a href="chain.md"><strong>Chain</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-138">Para inicializar o objeto <a href="chain.md"><strong>Chain</strong></a> , chame o método <a href="chain-build.md"><strong>Build</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-138">To initialize the <a href="chain.md"><strong>Chain</strong></a> object, call the <a href="chain-build.md"><strong>Build</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-139">0x80880220</span><span class="sxs-lookup"><span data-stu-id="76b06-139">0x80880220</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span></span></td>
<td><span data-ttu-id="76b06-141">O objeto de <a href="store.md"><strong>repositório</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-141">The <a href="store.md"><strong>Store</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-142">Para inicializar o objeto de <a href="store.md"><strong>armazenamento</strong></a> , chame o método <a href="store-open.md"><strong>Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-142">To initialize the <a href="store.md"><strong>Store</strong></a> object, call the <a href="store-open.md"><strong>Open</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-143">0x80880230</span><span class="sxs-lookup"><span data-stu-id="76b06-143">0x80880230</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span></span></td>
<td><span data-ttu-id="76b06-145">O objeto de <a href="store.md"><strong>repositório</strong></a> não contém nenhum objeto de <a href="certificate.md"><strong>certificado</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-145">The <a href="store.md"><strong>Store</strong></a> object does not contain any <a href="certificate.md"><strong>Certificate</strong></a> objects.</span></span><br/></td>
<td><span data-ttu-id="76b06-146">0x80880231</span><span class="sxs-lookup"><span data-stu-id="76b06-146">0x80880231</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span></span></td>
<td><span data-ttu-id="76b06-148">O parâmetro <em>OpenMode</em> do método <a href="store-open.md"><strong>Store. Open</strong></a> não contém um valor válido de CAPICOM_STORE_OPEN_MODE.</span><span class="sxs-lookup"><span data-stu-id="76b06-148">The <em>OpenMode</em> parameter of the <a href="store-open.md"><strong>Store.Open</strong></a> method does not contain a valid value of CAPICOM_STORE_OPEN_MODE.</span></span><br/> <span data-ttu-id="76b06-149">A lista a seguir mostra os valores válidos de CAPICOM_STORE_OPEN_MODE:</span><span class="sxs-lookup"><span data-stu-id="76b06-149">The following list shows the valid values of CAPICOM_STORE_OPEN_MODE:</span></span>
<ul>
<li><span data-ttu-id="76b06-150">CAPICOM_STORE_OPEN_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="76b06-150">CAPICOM_STORE_OPEN_READ_ONLY</span></span></li>
<li><span data-ttu-id="76b06-151">CAPICOM_STORE_OPEN_READ_WRITE</span><span class="sxs-lookup"><span data-stu-id="76b06-151">CAPICOM_STORE_OPEN_READ_WRITE</span></span></li>
<li><span data-ttu-id="76b06-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="76b06-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span></span></li>
<li><span data-ttu-id="76b06-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span><span class="sxs-lookup"><span data-stu-id="76b06-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span></span></li>
<li><span data-ttu-id="76b06-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span><span class="sxs-lookup"><span data-stu-id="76b06-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="76b06-155">0x80880232</span><span class="sxs-lookup"><span data-stu-id="76b06-155">0x80880232</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span></span></td>
<td><span data-ttu-id="76b06-157">O valor de <em>SaveAs</em> passado para o método <a href="store-export.md"><strong>Export</strong></a> do objeto <a href="store.md"><strong>Store</strong></a> não era válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-157">The <em>SaveAs</em> value passed to the <a href="store-export.md"><strong>Export</strong></a> method of the <a href="store.md"><strong>Store</strong></a> object was not valid.</span></span> <br/> <span data-ttu-id="76b06-158">A lista a seguir mostra os valores válidos de <em>SaveAs</em> :</span><span class="sxs-lookup"><span data-stu-id="76b06-158">The following list shows the valid <em>SaveAs</em> values:</span></span>
<ul>
<li><span data-ttu-id="76b06-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span><span class="sxs-lookup"><span data-stu-id="76b06-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span></span></li>
<li><span data-ttu-id="76b06-160">CAPICOM_STORE_SAVE_AS_PKCS7</span><span class="sxs-lookup"><span data-stu-id="76b06-160">CAPICOM_STORE_SAVE_AS_PKCS7</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="76b06-161">0x80880233</span><span class="sxs-lookup"><span data-stu-id="76b06-161">0x80880233</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-163">A propriedade <a href="attribute-name.md"><strong>Name</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="76b06-163">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-164">Defina a propriedade <a href="attribute-name.md"><strong>Name</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-164">Set the <a href="attribute-name.md"><strong>Name</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="76b06-165">0x80880240</span><span class="sxs-lookup"><span data-stu-id="76b06-165">0x80880240</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-167">A propriedade <a href="attribute-value.md"><strong>Value</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="76b06-167">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-168">Defina a propriedade <a href="attribute-value.md"><strong>valor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-168">Set the <a href="attribute-value.md"><strong>Value</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="76b06-169">0x80880241</span><span class="sxs-lookup"><span data-stu-id="76b06-169">0x80880241</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span></span></td>
<td><span data-ttu-id="76b06-171">A propriedade <a href="attribute-name.md"><strong>Name</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não é válida.</span><span class="sxs-lookup"><span data-stu-id="76b06-171">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="76b06-172">A lista a seguir mostra os nomes de atributo válidos:</span><span class="sxs-lookup"><span data-stu-id="76b06-172">The following list shows the valid attribute names:</span></span>
<ul>
<li><span data-ttu-id="76b06-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span><span class="sxs-lookup"><span data-stu-id="76b06-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span></span></li>
<li><span data-ttu-id="76b06-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span><span class="sxs-lookup"><span data-stu-id="76b06-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span></span></li>
<li><span data-ttu-id="76b06-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="76b06-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="76b06-176">0x80880242</span><span class="sxs-lookup"><span data-stu-id="76b06-176">0x80880242</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span></span></td>
<td><span data-ttu-id="76b06-178">A propriedade <a href="attribute-value.md"><strong>Value</strong></a> do objeto de <a href="attribute.md"><strong>atributo</strong></a> não é válida porque o tipo de dados não corresponde ao tipo de dados indicado pela propriedade <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="76b06-178">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid because the data type does not match the data type indicated by the <strong>Name</strong> property.</span></span> <br/> <span data-ttu-id="76b06-179">Por exemplo, se a propriedade <a href="attribute-value.md"><strong>Name</strong></a> for definida como CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, o tipo de dados deverá ser <strong>Date</strong>.</span><span class="sxs-lookup"><span data-stu-id="76b06-179">For example, if the <a href="attribute-value.md"><strong>Name</strong></a> property is set to CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, the data type must be <strong>DATE</strong>.</span></span><br/></td>
<td><span data-ttu-id="76b06-180">0x80880243</span><span class="sxs-lookup"><span data-stu-id="76b06-180">0x80880243</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-182">O objeto de <a href="signer.md"><strong>signatário</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-182">The <a href="signer.md"><strong>Signer</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-183">Para inicializar o objeto de <a href="signer.md"><strong>signatário</strong></a> , defina a propriedade de <a href="signer-certificate.md"><strong>certificado</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-183">To initialize the <a href="signer.md"><strong>Signer</strong></a> object, set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="76b06-184">0x80880250</span><span class="sxs-lookup"><span data-stu-id="76b06-184">0x80880250</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="76b06-186">Não é possível encontrar o signatário no objeto <a href="signeddata.md"><strong>SignedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-186">The signer cannot be found in the <a href="signeddata.md"><strong>SignedData</strong></a> object.</span></span> <br/> <span data-ttu-id="76b06-187">Normalmente, isso não acontece com um objeto <a href="signeddata.md"><strong>SignedData</strong></a> que foi criado pelo CAPICOM; no entanto, se o objeto <strong>SignedData</strong> foi criado por um produto de terceiros, o certificado do assinante pode não ser incluído na estrutura de #7 PKCS.</span><span class="sxs-lookup"><span data-stu-id="76b06-187">Usually, this does not happen with a <a href="signeddata.md"><strong>SignedData</strong></a> object that was created by CAPICOM; however, if the <strong>SignedData</strong> object was created by a third-party product, the signer's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="76b06-188">0x80880251</span><span class="sxs-lookup"><span data-stu-id="76b06-188">0x80880251</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span></span></td>
<td><span data-ttu-id="76b06-190">Não é possível encontrar um objeto de <a href="chain.md"><strong>cadeia</strong></a> no objeto de <a href="signer.md"><strong>signatário</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-190">A <a href="chain.md"><strong>Chain</strong></a> object cannot be found in the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="76b06-191">0x80880252//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-191">0x80880252 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span></span></td>
<td><span data-ttu-id="76b06-193">É feita uma tentativa de usar o Assinante de uma forma que não seja válida.</span><span class="sxs-lookup"><span data-stu-id="76b06-193">An attempt is made to use the signer in a way that is not valid.</span></span><br/></td>
<td><span data-ttu-id="76b06-194">0x80880253 //v2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-194">0x80880253 //v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-196">O objeto <a href="signeddata.md"><strong>SignedData</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-196">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-197">Para inicializar o objeto <a href="signeddata.md"><strong>SignedData</strong></a> , defina a propriedade <a href="signeddata-content.md"><strong>Content</strong></a> ou chame o método <a href="signeddata-verify.md"><strong>Verify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-197">To initialize the <a href="signeddata.md"><strong>SignedData</strong></a> object, set the <a href="signeddata-content.md"><strong>Content</strong></a> property or call the <a href="signeddata-verify.md"><strong>Verify</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-198">0x80880260</span><span class="sxs-lookup"><span data-stu-id="76b06-198">0x80880260</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="76b06-200">O objeto <a href="signeddata.md"><strong>SignedData</strong></a> contém um tipo que não é válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-200">The <a href="signeddata.md"><strong>SignedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="76b06-201">Normalmente, isso acontece quando é feita uma tentativa de verificar uma mensagem envelopada com um objeto <a href="signeddata.md"><strong>SignedData</strong></a> ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="76b06-201">Usually, this happens when an attempt is made to verify an enveloped message with a <a href="signeddata.md"><strong>SignedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="76b06-202">0x80880261</span><span class="sxs-lookup"><span data-stu-id="76b06-202">0x80880261</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="76b06-204">O objeto <a href="signeddata.md"><strong>SignedData</strong></a> não foi assinado.</span><span class="sxs-lookup"><span data-stu-id="76b06-204">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been signed.</span></span> <br/> <span data-ttu-id="76b06-205">Para assinar o objeto <a href="signeddata.md"><strong>SignedData</strong></a> , chame o método <a href="signeddata-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-205">To sign the <a href="signeddata.md"><strong>SignedData</strong></a> object, call the <a href="signeddata-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-206">0x80880262</span><span class="sxs-lookup"><span data-stu-id="76b06-206">0x80880262</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span></span></td>
<td><span data-ttu-id="76b06-208">O valor do algoritmo para a propriedade <a href="algorithm-name.md"><strong>Name</strong></a> do objeto de <a href="algorithm.md"><strong>algoritmo</strong></a> não é válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-208">The algorithm value for the <a href="algorithm-name.md"><strong>Name</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="76b06-209">A lista a seguir mostra os valores de algoritmo válidos para a propriedade <a href="algorithm-name.md"><strong>Name</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="76b06-209">The following list shows the valid algorithm values for the <a href="algorithm-name.md"><strong>Name</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="76b06-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span><span class="sxs-lookup"><span data-stu-id="76b06-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span></span></li>
<li><span data-ttu-id="76b06-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span><span class="sxs-lookup"><span data-stu-id="76b06-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span></span></li>
<li><span data-ttu-id="76b06-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span><span class="sxs-lookup"><span data-stu-id="76b06-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span></span></li>
<li><span data-ttu-id="76b06-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span><span class="sxs-lookup"><span data-stu-id="76b06-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="76b06-214">0x80880270</span><span class="sxs-lookup"><span data-stu-id="76b06-214">0x80880270</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span></span></td>
<td><span data-ttu-id="76b06-216">O valor de comprimento da chave para a propriedade <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> do objeto de <a href="algorithm.md"><strong>algoritmo</strong></a> não é válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-216">The key length value for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="76b06-217">A lista a seguir mostra os valores de comprimento de chave válidos para a propriedade <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="76b06-217">The following list shows the valid key length values for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="76b06-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span><span class="sxs-lookup"><span data-stu-id="76b06-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span></span></li>
<li><span data-ttu-id="76b06-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span><span class="sxs-lookup"><span data-stu-id="76b06-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span></span></li>
<li><span data-ttu-id="76b06-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span><span class="sxs-lookup"><span data-stu-id="76b06-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span></span></li>
<li><span data-ttu-id="76b06-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span><span class="sxs-lookup"><span data-stu-id="76b06-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="76b06-222">0x80880271</span><span class="sxs-lookup"><span data-stu-id="76b06-222">0x80880271</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-224">O objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-224">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-225">Para inicializar o objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , defina a propriedade <a href="envelopeddata-content.md"><strong>Content</strong></a> ou chame o método <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-225">To initialize the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object, either set the <a href="envelopeddata-content.md"><strong>Content</strong></a> property or call the <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-226">0x80880280</span><span class="sxs-lookup"><span data-stu-id="76b06-226">0x80880280</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="76b06-228">O objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contém um tipo que não é válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-228">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="76b06-229">Normalmente, isso acontece quando é feita uma tentativa de verificar uma mensagem assinada com um objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="76b06-229">Usually, this happens when an attempt is made to verify a signed message with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="76b06-230">0x80880281</span><span class="sxs-lookup"><span data-stu-id="76b06-230">0x80880281</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span></span></td>
<td><span data-ttu-id="76b06-232">Não há nenhum destinatário especificado no objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> quando o método <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> de um objeto <strong>EnvelopedData</strong> é chamado.</span><span class="sxs-lookup"><span data-stu-id="76b06-232">There is no recipient specified in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object when the <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> method of an <strong>EnvelopedData</strong> object is called.</span></span> <br/> <span data-ttu-id="76b06-233">Para adicionar um destinatário, chame o método <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-233">To add a recipient, call the <a href="recipients-add.md"><strong>Recipients.Add</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-234">0x80880282</span><span class="sxs-lookup"><span data-stu-id="76b06-234">0x80880282</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="76b06-236">O destinatário não pode ser encontrado no objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-236">The recipient cannot be found in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object.</span></span> <br/> <span data-ttu-id="76b06-237">Normalmente, isso não acontece com um objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> que foi criado pelo CAPICOM; no entanto, se o objeto <strong>EnvelopedData</strong> foi criado por um produto de terceiros, o certificado do destinatário pode não estar incluído na estrutura de #7 PKCS.</span><span class="sxs-lookup"><span data-stu-id="76b06-237">Usually, this does not happen with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object that was created by CAPICOM; however, if the <strong>EnvelopedData</strong> object was created by a third-party product, the recipient's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="76b06-238">0x80880283</span><span class="sxs-lookup"><span data-stu-id="76b06-238">0x80880283</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-240">O objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-240">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-241">Para inicializar o objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , defina a propriedade <a href="encrypteddata-content.md"><strong>Content</strong></a> ou chame o método <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-241">To initialize the <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, either set the <a href="encrypteddata-content.md"><strong>Content</strong></a> property or call the <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-242">0x80880290</span><span class="sxs-lookup"><span data-stu-id="76b06-242">0x80880290</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="76b06-244">O objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> não é um tipo válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-244">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object is not a valid type.</span></span> <br/> <span data-ttu-id="76b06-245">Normalmente, isso significa que os dados estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="76b06-245">Usually, this means the data is corrupted.</span></span><br/></td>
<td><span data-ttu-id="76b06-246">0x80880291</span><span class="sxs-lookup"><span data-stu-id="76b06-246">0x80880291</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span></span></td>
<td><span data-ttu-id="76b06-248">O segredo de um objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-248">The secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="76b06-249">Para inicializar o segredo de um objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , chame o método <a href="encrypteddata-setsecret.md"><strong>setsecret</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-249">To initialize the secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, call the <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-250">0x80880292</span><span class="sxs-lookup"><span data-stu-id="76b06-250">0x80880292</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-252">O objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-252">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="76b06-253">0x80880300//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-253">0x80880300 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span></span></td>
<td><span data-ttu-id="76b06-255">O objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> não pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="76b06-255">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object cannot be exported.</span></span><br/></td>
<td><span data-ttu-id="76b06-256">0x80880301//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-256">0x80880301 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-258">O objeto <a href="encodeddata.md"><strong>EncodedData</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-258">The <a href="encodeddata.md"><strong>EncodedData</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="76b06-259">0x80880320//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-259">0x80880320 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-261">O objeto de <a href="extension.md"><strong>extensão</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-261">The <a href="extension.md"><strong>Extension</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="76b06-262">0x80880330//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-262">0x80880330 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-264">A propriedade <a href="extendedproperty-propid.md"><strong>Propid</strong></a> do objeto <a href="extendedproperty.md"><strong>Extended</strong></a> não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="76b06-264">The <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of the <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="76b06-265">0x80880340//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-265">0x80880340 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="76b06-267">O parâmetro <em>FindType</em> do método <a href="certificates-find.md"><strong>Certificates. Find</strong></a> não é um valor da enumeração <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-267">The <em>FindType</em> parameter of the <a href="certificates-find.md"><strong>Certificates.Find</strong></a> method is not a value of the <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> enumeration.</span></span><br/></td>
<td><span data-ttu-id="76b06-268">0x80880350//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-268">0x80880350 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span></span></td>
<td><span data-ttu-id="76b06-270">A política predefinida especificada para a operação Localizar não é válida.</span><span class="sxs-lookup"><span data-stu-id="76b06-270">The specified predefined policy for the find operation is not valid.</span></span><br/></td>
<td><span data-ttu-id="76b06-271">0x80880351//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-271">0x80880351 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-273">O objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="76b06-273">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="76b06-274">0x80880360//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-274">0x80880360 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="76b06-276">O objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi assinado.</span><span class="sxs-lookup"><span data-stu-id="76b06-276">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been signed.</span></span><br/> <span data-ttu-id="76b06-277">Para assinar o objeto <a href="signedcode.md"><strong>SignedCode</strong></a> , chame o método <a href="signedcode-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-277">To sign the <a href="signedcode.md"><strong>SignedCode</strong></a> object, call the <a href="signedcode-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="76b06-278">0x80880361//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-278">0x80880361 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-280">A propriedade <a href="signedcode-description.md"><strong>Description</strong></a> do objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="76b06-280">The <a href="signedcode-description.md"><strong>Description</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="76b06-281">0x80880362//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-281">0x80880362 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="76b06-283">A propriedade <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> do objeto <a href="signedcode.md"><strong>SignedCode</strong></a> não foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="76b06-283">The <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="76b06-284">0x80880363//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-284">0x80880363 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span></span></td>
<td><span data-ttu-id="76b06-286">O parâmetro de <em>URL</em> do método <a href="signedcode-timestamp.md"><strong>SignedCode. Timestamp</strong></a> não é válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-286">The <em>URL</em> parameter of the <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> method is not valid.</span></span><br/></td>
<td><span data-ttu-id="76b06-287">0x80880364//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-287">0x80880364 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span></span></td>
<td><span data-ttu-id="76b06-289">O objeto <a href="hasheddata.md"><strong>HashedData</strong></a> não contém nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="76b06-289">The <a href="hasheddata.md"><strong>HashedData</strong></a> object does not contain any data.</span></span><br/></td>
<td><span data-ttu-id="76b06-290">0x80880370//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-290">0x80880370 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span></span></td>
<td><span data-ttu-id="76b06-292">O tipo de conversão não é válido.</span><span class="sxs-lookup"><span data-stu-id="76b06-292">The convert type is not valid.</span></span><br/></td>
<td><span data-ttu-id="76b06-293">0x80880380//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-293">0x80880380 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span></span></td>
<td><span data-ttu-id="76b06-295">A operação solicitada não tem suporte na plataforma atual.</span><span class="sxs-lookup"><span data-stu-id="76b06-295">The requested operation is not supported in the current platform.</span></span> <br/></td>
<td><span data-ttu-id="76b06-296">0x80880900</span><span class="sxs-lookup"><span data-stu-id="76b06-296">0x80880900</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-297"><strong>CAPICOM_E_UI_DISABLED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-297"><strong>CAPICOM_E_UI_DISABLED</strong></span></span></td>
<td><span data-ttu-id="76b06-298">Ao assinar, a propriedade de <a href="signer-certificate.md"><strong>certificado</strong></a> do objeto de <a href="signer.md"><strong>signatário</strong></a> não foi definida, mas o prompt para o certificado de usuário foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="76b06-298">When signing, the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object has not been set, but the prompt for the user certificate has been disabled.</span></span> <br/> <span data-ttu-id="76b06-299">Habilite o prompt definindo a propriedade <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> do objeto de <a href="settings.md"><strong>configurações</strong></a> ou defina a propriedade de <a href="signer-certificate.md"><strong>certificado</strong></a> do objeto de <a href="signer.md"><strong>signatário</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="76b06-299">Either enable the prompt by setting the <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> property of the <a href="settings.md"><strong>Settings</strong></a> object, or set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="76b06-300">0x80880901</span><span class="sxs-lookup"><span data-stu-id="76b06-300">0x80880901</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-301"><strong>CAPICOM_E_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-301"><strong>CAPICOM_E_CANCELLED</strong></span></span></td>
<td><span data-ttu-id="76b06-302">A operação foi cancelada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="76b06-302">The operation has been canceled by the user.</span></span> <br/> <span data-ttu-id="76b06-303">Isso acontece quando o usuário é solicitado a fornecer permissão para realizar uma determinada operação, como acessar a chave privada, e o usuário cancela a operação.</span><span class="sxs-lookup"><span data-stu-id="76b06-303">This happens when the user is prompted for permission to carry out a certain operation, such as accessing the private key, and the user cancels the operation.</span></span><br/></td>
<td><span data-ttu-id="76b06-304">0x80880902</span><span class="sxs-lookup"><span data-stu-id="76b06-304">0x80880902</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span></span></td>
<td><span data-ttu-id="76b06-306">A operação tentada não é permitida.</span><span class="sxs-lookup"><span data-stu-id="76b06-306">The attempted operation is not allowed.</span></span><br/> <span data-ttu-id="76b06-307">Por exemplo, a alteração da propriedade <a href="extendedproperty-propid.md"><strong>Propid</strong></a> de um objeto <a href="extendedproperty.md"><strong>Extended</strong></a> não será permitida se o objeto estiver anexado a um certificado.</span><span class="sxs-lookup"><span data-stu-id="76b06-307">For example, changing the <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of an <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object is not allowed if the object is attached to a certificate.</span></span><br/></td>
<td><span data-ttu-id="76b06-308">0x80880903//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-308">0x80880903 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span></span></td>
<td><span data-ttu-id="76b06-310">O capicont ficou sem um recurso.</span><span class="sxs-lookup"><span data-stu-id="76b06-310">CAPICOM has run out of a resource.</span></span><br/></td>
<td><span data-ttu-id="76b06-311">0x80880904//v 2.0</span><span class="sxs-lookup"><span data-stu-id="76b06-311">0x80880904 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76b06-312"><strong>CAPICOM_E_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-312"><strong>CAPICOM_E_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="76b06-313">Ocorreu um erro interno.</span><span class="sxs-lookup"><span data-stu-id="76b06-313">An internal error has occurred.</span></span> <br/> <span data-ttu-id="76b06-314">Contate o suporte técnico da Microsoft para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="76b06-314">Contact Microsoft Technical Support for assistance.</span></span><br/></td>
<td><span data-ttu-id="76b06-315">0x80880911</span><span class="sxs-lookup"><span data-stu-id="76b06-315">0x80880911</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76b06-316"><strong>CAPICOM_E_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="76b06-316"><strong>CAPICOM_E_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="76b06-317">Ocorreu um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="76b06-317">An unknown error has occurred.</span></span> <br/> <span data-ttu-id="76b06-318">Colete o máximo de informações possível e entre em contato com seu fornecedor.</span><span class="sxs-lookup"><span data-stu-id="76b06-318">Collect as much information as possible, and contact your vendor.</span></span><br/></td>
<td><span data-ttu-id="76b06-319">0x80880999</span><span class="sxs-lookup"><span data-stu-id="76b06-319">0x80880999</span></span></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="76b06-320">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76b06-320">Requirements</span></span>



| <span data-ttu-id="76b06-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="76b06-321">Requirement</span></span> | <span data-ttu-id="76b06-322">Valor</span><span class="sxs-lookup"><span data-stu-id="76b06-322">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76b06-323">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="76b06-323">Redistributable</span></span><br/> | <span data-ttu-id="76b06-324">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="76b06-324">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="76b06-325">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76b06-325">Header</span></span><br/>          | <dl> <span data-ttu-id="76b06-326"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="76b06-326"><dt>Capicom.h</dt></span></span> </dl> |



 

 




