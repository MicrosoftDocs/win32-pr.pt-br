---
description: Salva o certificado em um arquivo.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'Método ICertificate2:: Save'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796380"
---
# <a name="icertificate2save-method"></a><span data-ttu-id="b7cbb-103">Método ICertificate2:: Save</span><span class="sxs-lookup"><span data-stu-id="b7cbb-103">ICertificate2::Save method</span></span>

<span data-ttu-id="b7cbb-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b7cbb-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b7cbb-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b7cbb-106">O método **Save** salva o certificado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-106">The **Save** method saves the certificate to a file.</span></span> <span data-ttu-id="b7cbb-107">Esse método foi introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cbb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7cbb-108">Syntax</span></span>


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b7cbb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7cbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7cbb-110">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7cbb-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cbb-111">Uma cadeia de caracteres que contém o nome do arquivo de saída no qual o certificado será salvo.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-111">A string that contains the name of the output file where the certificate will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="b7cbb-112">*Senha* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7cbb-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cbb-113">Uma cadeia de caracteres que contém a senha de [*texto não criptografado*](../secgloss/p-gly.md) para um arquivo de [*chave privada*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b7cbb-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="b7cbb-114">A senha pode conter até 32 caracteres Unicode, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="b7cbb-115">Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="b7cbb-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7cbb-116">*Salvar como* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7cbb-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cbb-117">Um valor da enumeração do [**certificado CAPICOM \_ \_ Salvar \_ como \_ tipo**](capicom-certificate-save-as-type.md) que especifica o formato do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-117">A value of the [**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**](capicom-certificate-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="b7cbb-118">O padrão é o **CAPICOM de \_ \_ salvar certificado \_ como \_ cer**.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-118">The default is **CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**.</span></span> <span data-ttu-id="b7cbb-119">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="b7cbb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b7cbb-120">Value</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="b7cbb-121">Significado</span><span class="sxs-lookup"><span data-stu-id="b7cbb-121">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <span data-ttu-id="b7cbb-122"><dt>**\_salvar certificado de CApicom \_ \_ como \_ cer**</dt></span><span class="sxs-lookup"><span data-stu-id="b7cbb-122"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</dt></span></span> </dl> | <span data-ttu-id="b7cbb-123">O arquivo de saída será formatado como um arquivo. cer sem chaves privadas salvas.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-123">The output file will be formatted as a .cer file with no private keys saved.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <span data-ttu-id="b7cbb-124"><dt>**\_salvar certificado de CApicom \_ \_ como \_ pfx**</dt></span><span class="sxs-lookup"><span data-stu-id="b7cbb-124"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</dt></span></span> </dl> | <span data-ttu-id="b7cbb-125">O arquivo de saída será formatado como um arquivo. pfx (PKCS \# 12) e quaisquer chaves privadas associadas que sejam exportáveis também serão salvas.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-125">The output file will be formatted as a .pfx (PKCS \#12) file and any associated private keys that are exportable will also be saved.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b7cbb-126">*IncludeOption* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7cbb-126">*IncludeOption* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cbb-127">Um valor do [**certificado CAPICOM \_ \_ inclui \_**](capicom-certificate-include-option.md) a enumeração de opção que especifica quantos certificados na cadeia são salvos no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-127">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies how many certificates in the chain are saved to the output file.</span></span> <span data-ttu-id="b7cbb-128">O padrão é capicor \_ certificado \_ somente inclusão de \_ \_ entidade final \_ .</span><span class="sxs-lookup"><span data-stu-id="b7cbb-128">The default is CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY.</span></span> <span data-ttu-id="b7cbb-129">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-129">The following table shows the possible values.</span></span>



| <span data-ttu-id="b7cbb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b7cbb-130">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="b7cbb-131">Significado</span><span class="sxs-lookup"><span data-stu-id="b7cbb-131">Meaning</span></span>                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="b7cbb-132"><dt>**CAPICOM de certificado de caissor \_ \_ \_ \_ , exceto \_ raiz**</dt></span><span class="sxs-lookup"><span data-stu-id="b7cbb-132"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="b7cbb-133">Salva todos os certificados na cadeia com a exceção da entidade raiz</span><span class="sxs-lookup"><span data-stu-id="b7cbb-133">Saves all certificates in the chain with the exception of the root entity</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="b7cbb-134"><dt>**certificado CAPICOM \_ \_ incluir \_ \_ cadeia inteira**</dt></span><span class="sxs-lookup"><span data-stu-id="b7cbb-134"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="b7cbb-135">Salva a cadeia de certificados completa</span><span class="sxs-lookup"><span data-stu-id="b7cbb-135">Saves the complete certificate chain</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="b7cbb-136"><dt>**o certificado CAPICOM \_ \_ inclui \_ \_ somente entidade final \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7cbb-136"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="b7cbb-137">Salva apenas o certificado de entidade final</span><span class="sxs-lookup"><span data-stu-id="b7cbb-137">Saves only the end entity certificate</span></span><br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7cbb-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7cbb-138">Return value</span></span>

<span data-ttu-id="b7cbb-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7cbb-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7cbb-140">Remarks</span></span>

<span data-ttu-id="b7cbb-141">Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="b7cbb-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cbb-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7cbb-142">Requirements</span></span>



| <span data-ttu-id="b7cbb-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7cbb-143">Requirement</span></span> | <span data-ttu-id="b7cbb-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b7cbb-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cbb-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b7cbb-145">End of client support</span></span><br/> | <span data-ttu-id="b7cbb-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7cbb-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b7cbb-147">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b7cbb-147">End of server support</span></span><br/> | <span data-ttu-id="b7cbb-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7cbb-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b7cbb-149">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b7cbb-149">Redistributable</span></span><br/>       | <span data-ttu-id="b7cbb-150">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7cbb-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7cbb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b7cbb-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b7cbb-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7cbb-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
