---
description: Salva os objetos de certificado na coleção.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Método Certificates. Save
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750437"
---
# <a name="certificatessave-method"></a><span data-ttu-id="9477b-103">Método Certificates. Save</span><span class="sxs-lookup"><span data-stu-id="9477b-103">Certificates.Save method</span></span>

<span data-ttu-id="9477b-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9477b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9477b-105">Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9477b-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9477b-106">O método **Save** salva os objetos de [**certificado**](certificate.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="9477b-106">The **Save** method saves the [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9477b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9477b-107">Syntax</span></span>


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9477b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9477b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9477b-109">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9477b-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9477b-110">Uma cadeia de caracteres que contém o nome do arquivo de saída onde os certificados serão salvos.</span><span class="sxs-lookup"><span data-stu-id="9477b-110">A string that contains the name of the output file where the certificates will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="9477b-111">*Senha* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9477b-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9477b-112">Uma cadeia de caracteres que contém a senha de [*texto não criptografado*](../secgloss/p-gly.md) para um arquivo de [*chave privada*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9477b-112">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="9477b-113">O valor padrão é a cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="9477b-113">The default value is the empty string ("").</span></span> <span data-ttu-id="9477b-114">Até 32 caracteres Unicode, incluindo um caractere nulo de terminação, podem ser usados para a senha.</span><span class="sxs-lookup"><span data-stu-id="9477b-114">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="9477b-115">Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="9477b-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="9477b-116">*Salvar como* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9477b-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9477b-117">Um valor da enumeração de [**certificados CAPICOM \_ \_ Salvar \_ como \_ tipo**](capicom-certificates-save-as-type.md) que especifica o formato do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="9477b-117">A value of the [**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**](capicom-certificates-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="9477b-118">O padrão é capicor \_ certificados \_ Save \_ as \_ PFX.</span><span class="sxs-lookup"><span data-stu-id="9477b-118">The default is CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX.</span></span> <span data-ttu-id="9477b-119">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="9477b-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="9477b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9477b-120">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="9477b-121">Significado</span><span class="sxs-lookup"><span data-stu-id="9477b-121">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <span data-ttu-id="9477b-122"><dt>**os certificados CAPICOM \_ \_ Salvar \_ como \_ pfx**</dt></span><span class="sxs-lookup"><span data-stu-id="9477b-122"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</dt></span></span> </dl>                      | <span data-ttu-id="9477b-123">Os certificados são salvos como um PFX.</span><span class="sxs-lookup"><span data-stu-id="9477b-123">The certificates are saved as a PFX.</span></span><br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <span data-ttu-id="9477b-124"><dt>**Os certificados CAPICOM \_ \_ Save \_ as \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="9477b-124"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="9477b-125">Os certificados são salvos como um PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="9477b-125">The certificates are saved as a PKCS \#7.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <span data-ttu-id="9477b-126"><dt>**os certificados CAPICOM \_ \_ Salvar \_ como \_ serializado**</dt></span><span class="sxs-lookup"><span data-stu-id="9477b-126"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="9477b-127">Os certificados são salvos como serializados.</span><span class="sxs-lookup"><span data-stu-id="9477b-127">The certificates are saved as serialized.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9477b-128">*ExportFlag* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9477b-128">*ExportFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9477b-129">Um valor da enumeração [**do \_ \_ sinalizador de exportação de CAPICOM**](capicom-export-flag.md) que especifica se os erros de exportação de chave privada são ignorados.</span><span class="sxs-lookup"><span data-stu-id="9477b-129">A value of the [**CAPICOM\_EXPORT\_FLAG**](capicom-export-flag.md) enumeration that specifies whether any private key export errors are ignored.</span></span> <span data-ttu-id="9477b-130">O padrão é o CAPICOM de \_ exportação \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="9477b-130">The default is CAPICOM\_EXPORT\_DEFAULT.</span></span> <span data-ttu-id="9477b-131">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="9477b-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="9477b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="9477b-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="9477b-133">Significado</span><span class="sxs-lookup"><span data-stu-id="9477b-133">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <span data-ttu-id="9477b-134"><dt>**\_padrão de exportação de CApicom \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9477b-134"><dt>**CAPICOM\_EXPORT\_DEFAULT**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="9477b-135">Os erros de exportação de chave privada não são ignorados.</span><span class="sxs-lookup"><span data-stu-id="9477b-135">Private key export errors are not ignored.</span></span><br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <span data-ttu-id="9477b-136"><dt>**\_erro de exportação para \_ ignorar \_ \_ chave privada \_ não \_ exportável \_ do CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="9477b-136"><dt>**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="9477b-137">Erros de exportação de chave privada são ignorados.</span><span class="sxs-lookup"><span data-stu-id="9477b-137">Private key export errors are ignored.</span></span><br/>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9477b-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9477b-138">Return value</span></span>

<span data-ttu-id="9477b-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9477b-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9477b-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="9477b-140">Remarks</span></span>

<span data-ttu-id="9477b-141">Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="9477b-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="9477b-142">Os objetos de [**certificado**](certificate.md) podem ser recuperados usando o método [**Store. Load**](store-load.md) .</span><span class="sxs-lookup"><span data-stu-id="9477b-142">The [**Certificate**](certificate.md) objects can be retrieved by using the [**Store.Load**](store-load.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9477b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9477b-143">Requirements</span></span>



| <span data-ttu-id="9477b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9477b-144">Requirement</span></span> | <span data-ttu-id="9477b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="9477b-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9477b-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9477b-146">End of client support</span></span><br/> | <span data-ttu-id="9477b-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9477b-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9477b-148">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="9477b-148">End of server support</span></span><br/> | <span data-ttu-id="9477b-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9477b-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9477b-150">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9477b-150">Redistributable</span></span><br/>       | <span data-ttu-id="9477b-151">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="9477b-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9477b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9477b-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9477b-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9477b-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9477b-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="9477b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9477b-155">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="9477b-155">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
