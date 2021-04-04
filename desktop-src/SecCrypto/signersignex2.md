---
description: Os sinais e a hora carimbam o arquivo especificado, permitindo várias assinaturas aninhadas.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: Função SignerSignEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171106"
---
# <a name="signersignex2-function"></a><span data-ttu-id="87799-103">Função SignerSignEx2</span><span class="sxs-lookup"><span data-stu-id="87799-103">SignerSignEx2 function</span></span>

<span data-ttu-id="87799-104">A função **SignerSignEx2** sinaliza e o tempo marca o arquivo especificado, permitindo várias assinaturas aninhadas.</span><span class="sxs-lookup"><span data-stu-id="87799-104">The **SignerSignEx2** function signs and time stamps the specified file, allowing multiple nested signatures.</span></span>

> [!Note]  
> <span data-ttu-id="87799-105">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="87799-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="87799-106">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="87799-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="87799-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87799-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="87799-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87799-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87799-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87799-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-110">Modifica o comportamento dessa função.</span><span class="sxs-lookup"><span data-stu-id="87799-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="87799-111">Se o arquivo a ser assinado for um arquivo executável portátil (PE), isso poderá ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="87799-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="87799-112">Valor</span><span class="sxs-lookup"><span data-stu-id="87799-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="87799-113">Significado</span><span class="sxs-lookup"><span data-stu-id="87799-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="87799-114"><dt>**SPC \_ \_ \_ \_ \_ Sinalizador de hashes de página do PE do exc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87799-114"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="87799-115">Exclua os hashes de página ao criar dados indiretos SIP para o arquivo PE.</span><span class="sxs-lookup"><span data-stu-id="87799-115">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="87799-116">Esse sinalizador tem precedência sobre o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** .</span><span class="sxs-lookup"><span data-stu-id="87799-116">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="87799-117">Se nem o sinalizador de **\_ \_ \_ \_ hashes \_ de página do SPC exc PE** ou o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** . do SPC for especificado, o valor definido com a função [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) será usado para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="87799-117">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="87799-118">O padrão para essa configuração é excluir hashes de página ao criar dados indiretos SIP para arquivos PE.</span><span class="sxs-lookup"><span data-stu-id="87799-118">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="87799-119">Esse valor é definido no arquivo de cabeçalho Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="87799-119">This value is defined in the Mssip.h header file.</span></span><br/> <span data-ttu-id="87799-120">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="87799-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="87799-121"><dt>**SPC \_ \_Sinalizador de \_ \_ tabela de \_ \_ end de importação do PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87799-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="87799-122">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="87799-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="87799-123"><dt>**SPC \_ 0x40 \_ do \_ \_ \_ sinalizador de informações de depuração Inc PE**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87799-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="87799-124">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="87799-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="87799-125"><dt>**SPC \_ 0x80 \_ de \_ \_ sinalizador de recursos do PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87799-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="87799-126">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="87799-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="87799-127"><dt>**SPC \_ 0x100 \_ do \_ \_ \_ sinalizador de hash da página do PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87799-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="87799-128">Inclua hashes de página ao criar dados indiretos SIP para o arquivo PE.</span><span class="sxs-lookup"><span data-stu-id="87799-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="87799-129">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="87799-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> <span data-ttu-id="87799-130">Esse valor é definido no arquivo de cabeçalho Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="87799-130">This value is defined in the Mssip.h header file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <span data-ttu-id="87799-131"><dt>**SIG \_ ACRESCENTAR**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="87799-131"><dt>**SIG\_APPEND**</dt> <dt>0x1000</dt></span></span> </dl>                                                                         | <span data-ttu-id="87799-132">A assinatura será aninhada.</span><span class="sxs-lookup"><span data-stu-id="87799-132">The signature will be nested.</span></span> <span data-ttu-id="87799-133">Se você definir esse sinalizador antes que qualquer assinatura tenha sido adicionada, a assinatura gerada será adicionada como a assinatura externa.</span><span class="sxs-lookup"><span data-stu-id="87799-133">If you set this flag before any signature has been added, the generated signature will be added as the outer signature.</span></span> <span data-ttu-id="87799-134">Se você não definir esse sinalizador, a assinatura gerada substituirá a assinatura externa, excluindo todas as assinaturas internas.</span><span class="sxs-lookup"><span data-stu-id="87799-134">If you do not set this flag, the generated signature replaces the outer signature, deleting all inner signatures.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="87799-135">*pSubjectInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87799-135">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-136">Ponteiro para uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que especifica o assunto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="87799-136">Pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="87799-137">*pSignerCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87799-137">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-138">Ponteiro para uma estrutura de [**\_ certificado de signatário**](signer-cert.md) que especifica o certificado a ser usado para criar a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="87799-138">Pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="87799-139">*pSignatureInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87799-139">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-140">Um ponteiro para uma estrutura de [**\_ \_ informações de assinatura de assinante**](signer-signature-info.md) que contém informações sobre a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="87799-140">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="87799-141">*pProviderInfo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87799-141">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-142">Ponteiro para uma estrutura de [**\_ \_ informações do provedor de assinante**](signer-provider-info.md) que especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de chave privada usadas para criar a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="87799-142">Pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="87799-143">Se o valor desse parâmetro for **nulo**, o parâmetro *pSignerCert* deverá especificar um certificado associado a um CSP.</span><span class="sxs-lookup"><span data-stu-id="87799-143">If the value of this parameter is **NULL**, the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="87799-144">*dwTimestampFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87799-144">*dwTimestampFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-145">Sinalizadores que serão passados para [**SignerTimeStampEx3**](signertimestampex3.md) se o parâmetro *PwszHttpTimeStamp* não for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="87799-145">Flags that will be passed to [**SignerTimeStampEx3**](signertimestampex3.md) if the *pwszHttpTimeStamp* parameter is not **NULL**.</span></span> <span data-ttu-id="87799-146">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="87799-146">This can be one of the following values.</span></span>



| <span data-ttu-id="87799-147">Valor</span><span class="sxs-lookup"><span data-stu-id="87799-147">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="87799-148">Significado</span><span class="sxs-lookup"><span data-stu-id="87799-148">Meaning</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="87799-149"><dt>**\_carimbo de data/hora do signatário \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="87799-149"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="87799-150">Valor padrão.</span><span class="sxs-lookup"><span data-stu-id="87799-150">Default value.</span></span> <span data-ttu-id="87799-151">Especifica um carimbo de data/hora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="87799-151">Specifies an Authenticode timestamp.</span></span><br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="87799-152"><dt>**\_Carimbo de data/hora do signatário \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="87799-152"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="87799-153">Especifica um carimbo de data/hora RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="87799-153">Specifies an RFC 3161 timestamp.</span></span><br/>                    |



 

<span data-ttu-id="87799-154">Esse parâmetro será ignorado se o parâmetro *pwszHttpTimeStamp* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="87799-154">This parameter is ignored if the *pwszHttpTimeStamp* parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87799-155">*pszTimestampAlgorithmOid* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87799-155">*pszTimestampAlgorithmOid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-156">Identificador de objeto do algoritmo a ser usado para criar um carimbo de data/hora RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="87799-156">Object identifier of the algorithm to be used for creating an RFC 3161 timestamp.</span></span> <span data-ttu-id="87799-157">Esse parâmetro é ignorado para carimbos de data/hora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="87799-157">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="87799-158">*pwszHttpTimeStamp* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87799-158">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-159">URL do servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="87799-159">URL of the time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="87799-160">*psRequest* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87799-160">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-161">Ponteiro para uma matriz de estruturas de [**\_ atributo cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) -las que são adicionadas a uma solicitação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="87799-161">Pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="87799-162">Esse parâmetro será ignorado se o parâmetro *pwszHttpTimeStamp* não contiver um valor válido ou for **NULL**.</span><span class="sxs-lookup"><span data-stu-id="87799-162">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value or is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87799-163">*pSipData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87799-163">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-164">Um valor de 32 bits que é passado como dados adicionais para funções SIP.</span><span class="sxs-lookup"><span data-stu-id="87799-164">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="87799-165">O formato e o conteúdo deste são definidos pelo provedor SIP.</span><span class="sxs-lookup"><span data-stu-id="87799-165">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="87799-166">*ppSignerContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="87799-166">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-167">O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o [*blob*](../secgloss/b-gly.md)assinado.</span><span class="sxs-lookup"><span data-stu-id="87799-167">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="87799-168">Quando você terminar de usar a estrutura de **\_ contexto do signatário** , libere a estrutura do **\_ contexto do signatário** chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="87799-168">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="87799-169">*pCryptoPolicy* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="87799-169">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87799-170">Se presente, um ponteiro para uma estrutura de [**\_ \_ sinal \_ de segurança de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) que contém os parâmetros usados para verificar se há assinaturas fortes.</span><span class="sxs-lookup"><span data-stu-id="87799-170">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="87799-171">Se um certificado ou sua cadeia não passar, o arquivo não será alterado de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="87799-171">If either a certificate or its chain does not pass, the file is not altered in any way.</span></span> <span data-ttu-id="87799-172">Se uma URL for passada para especificar uma autoridade de carimbo de data/hora (TSA), essa política também será aplicada ao carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="87799-172">If a URL is passed in to specify a Time Stamping Authority (TSA), this policy is also applied to the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="87799-173">*Preservação*</span><span class="sxs-lookup"><span data-stu-id="87799-173">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="87799-174">Reservado.</span><span class="sxs-lookup"><span data-stu-id="87799-174">Reserved.</span></span> <span data-ttu-id="87799-175">Esse valor deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="87799-175">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87799-176">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87799-176">Return value</span></span>

<span data-ttu-id="87799-177">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87799-177">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="87799-178">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="87799-178">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="87799-179">Os códigos de erro possíveis retornados por essa função incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="87799-179">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="87799-180">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="87799-180">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



| <span data-ttu-id="87799-181">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="87799-181">Return code</span></span>                                                                                  | <span data-ttu-id="87799-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="87799-182">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87799-183"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="87799-183"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="87799-184">Se você definir o parâmetro *dwTimestampFlags* para o **assinante \_ timestamp \_ AUTHENTICODE**, não será possível definir o parâmetro *dwFlags* como **SIG \_ Append**.</span><span class="sxs-lookup"><span data-stu-id="87799-184">If you set the *dwTimestampFlags* parameter to **SIGNER\_TIMESTAMP\_AUTHENTICODE**, you cannot set the *dwFlags* parameter to **SIG\_APPEND**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="87799-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87799-185">Requirements</span></span>



| <span data-ttu-id="87799-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="87799-186">Requirement</span></span> | <span data-ttu-id="87799-187">Valor</span><span class="sxs-lookup"><span data-stu-id="87799-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87799-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87799-188">Minimum supported client</span></span><br/> | <span data-ttu-id="87799-189">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="87799-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="87799-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87799-190">Minimum supported server</span></span><br/> | <span data-ttu-id="87799-191">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="87799-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87799-192">DLL</span><span class="sxs-lookup"><span data-stu-id="87799-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87799-193"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87799-193"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87799-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="87799-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87799-195">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="87799-195">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="87799-196">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="87799-196">**SignerSignEx**</span></span>](signersignex.md)
</dt> <dt>

[<span data-ttu-id="87799-197">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="87799-197">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
