---
description: Assina o arquivo especificado e retorna um ponteiro para os dados assinados.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: Função SignerSignEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661897"
---
# <a name="signersignex-function"></a><span data-ttu-id="65c9e-103">Função SignerSignEx</span><span class="sxs-lookup"><span data-stu-id="65c9e-103">SignerSignEx function</span></span>

<span data-ttu-id="65c9e-104">A função **SignerSignEx** assina o arquivo especificado e retorna um ponteiro para os dados assinados.</span><span class="sxs-lookup"><span data-stu-id="65c9e-104">The **SignerSignEx** function signs the specified file and returns a pointer to the signed data.</span></span>

> [!Note]  
> <span data-ttu-id="65c9e-105">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="65c9e-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="65c9e-106">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="65c9e-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="65c9e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65c9e-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="65c9e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65c9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c9e-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-110">Modifica o comportamento dessa função.</span><span class="sxs-lookup"><span data-stu-id="65c9e-110">Modifies the behavior of this function.</span></span>

<span data-ttu-id="65c9e-111">Se o arquivo a ser assinado for um arquivo executável portátil (PE), isso poderá ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="65c9e-111">If the file to be signed is a portable executable (PE) file, this can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="65c9e-112">Esses identificadores são definidos em Mssip. h.</span><span class="sxs-lookup"><span data-stu-id="65c9e-112">These identifiers are defined in Mssip.h.</span></span>



| <span data-ttu-id="65c9e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="65c9e-113">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="65c9e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="65c9e-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="65c9e-115"><dt>**SPC \_ \_ \_ \_ \_ Sinalizador de hashes de página do PE do exc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65c9e-115"><dt>**SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x10</dt></span></span> </dl>                    | <span data-ttu-id="65c9e-116">Exclua os hashes de página ao criar dados indiretos SIP para o arquivo PE.</span><span class="sxs-lookup"><span data-stu-id="65c9e-116">Exclude page hashes when creating SIP indirect data for the PE file.</span></span> <span data-ttu-id="65c9e-117">Esse sinalizador tem precedência sobre o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** .</span><span class="sxs-lookup"><span data-stu-id="65c9e-117">This flag takes precedence over the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag.</span></span><br/> <span data-ttu-id="65c9e-118">Se nem o sinalizador de **\_ \_ \_ \_ hashes \_ de página do SPC exc PE** ou o sinalizador de **\_ \_ \_ \_ \_ sinalizador de hashes de página do PE Inc** . do SPC for especificado, o valor definido com a função [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) será usado para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="65c9e-118">If neither the **SPC\_EXC\_PE\_PAGE\_HASHES\_FLAG** or the **SPC\_INC\_PE\_PAGE\_HASHES\_FLAG** flag is specified, the value set with the [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) function is used for this setting.</span></span> <span data-ttu-id="65c9e-119">O padrão para essa configuração é excluir hashes de página ao criar dados indiretos SIP para arquivos PE.</span><span class="sxs-lookup"><span data-stu-id="65c9e-119">The default for this setting is to exclude page hashes when creating SIP indirect data for PE files.</span></span><br/> <span data-ttu-id="65c9e-120">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="65c9e-120">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <span data-ttu-id="65c9e-121"><dt>**SPC \_ \_Sinalizador de \_ \_ tabela de \_ \_ end de importação do PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65c9e-121"><dt>**SPC\_INC\_PE\_IMPORT\_ADDR\_TABLE\_FLAG**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="65c9e-122">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="65c9e-122">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <span data-ttu-id="65c9e-123"><dt>**SPC \_ 0x40 \_ do \_ \_ \_ sinalizador de informações de depuração Inc PE**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65c9e-123"><dt>**SPC\_INC\_PE\_DEBUG\_INFO\_FLAG**</dt> <dt>0x40</dt></span></span> </dl>                       | <span data-ttu-id="65c9e-124">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="65c9e-124">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <span data-ttu-id="65c9e-125"><dt>**SPC \_ 0x80 \_ de \_ \_ sinalizador de recursos do PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65c9e-125"><dt>**SPC\_INC\_PE\_RESOURCES\_FLAG**</dt> <dt>0x80</dt></span></span> </dl>                           | <span data-ttu-id="65c9e-126">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="65c9e-126">This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <span data-ttu-id="65c9e-127"><dt>**SPC \_ 0x100 \_ do \_ \_ \_ sinalizador de hash da página do PE Inc**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65c9e-127"><dt>**SPC\_INC\_PE\_PAGE\_HASHES\_FLAG**</dt> <dt>0x100</dt></span></span> </dl>                   | <span data-ttu-id="65c9e-128">Inclua hashes de página ao criar dados indiretos SIP para o arquivo PE.</span><span class="sxs-lookup"><span data-stu-id="65c9e-128">Include page hashes when creating SIP indirect data for the PE file.</span></span><br/> <span data-ttu-id="65c9e-129">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="65c9e-129">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="65c9e-130">*pSubjectInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-130">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-131">Um ponteiro para uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que especifica o assunto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="65c9e-131">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="65c9e-132">*pSignerCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-132">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-133">Um ponteiro para uma estrutura de [**\_ certificado de signatário**](signer-cert.md) que especifica o certificado a ser usado para criar a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="65c9e-133">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="65c9e-134">*pSignatureInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-134">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-135">Um ponteiro para uma estrutura de [**\_ \_ informações de assinatura de assinante**](signer-signature-info.md) que contém informações sobre a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="65c9e-135">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="65c9e-136">*pProviderInfo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-136">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-137">Um ponteiro para uma estrutura de [**\_ \_ informações do provedor de assinante**](signer-provider-info.md) que especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de chave privada usadas para criar a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="65c9e-137">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create the digital signature.</span></span>

<span data-ttu-id="65c9e-138">Se o valor desse parâmetro for **nulo**, o valor do parâmetro *pSignerCert* deverá especificar um certificado associado a um CSP.</span><span class="sxs-lookup"><span data-stu-id="65c9e-138">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="65c9e-139">*pwszHttpTimeStamp* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-139">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-140">A URL de um servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="65c9e-140">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="65c9e-141">*psRequest* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-141">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-142">Um ponteiro para uma matriz de estruturas de [**\_ atributo cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) -las que são adicionadas a uma solicitação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="65c9e-142">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="65c9e-143">Esse parâmetro será ignorado se o parâmetro *pwszHttpTimeStamp* não contiver um valor válido que não seja **nulo**.</span><span class="sxs-lookup"><span data-stu-id="65c9e-143">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65c9e-144">*pSipData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-144">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-145">Um valor de 32 bits que é passado como dados adicionais para funções SIP.</span><span class="sxs-lookup"><span data-stu-id="65c9e-145">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="65c9e-146">O formato e o conteúdo deste são definidos pelo provedor SIP.</span><span class="sxs-lookup"><span data-stu-id="65c9e-146">The format and content of this is defined by the SIP provider.</span></span>

</dd> <dt>

<span data-ttu-id="65c9e-147">*ppSignerContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-147">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65c9e-148">O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o [*blob*](../secgloss/b-gly.md)assinado.</span><span class="sxs-lookup"><span data-stu-id="65c9e-148">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="65c9e-149">Quando você terminar de usar a estrutura de **\_ contexto do signatário** , libere a estrutura do **\_ contexto do signatário** chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="65c9e-149">When you have finished using the **SIGNER\_CONTEXT** structure, free the **SIGNER\_CONTEXT** structure by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c9e-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65c9e-150">Return value</span></span>

<span data-ttu-id="65c9e-151">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65c9e-151">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="65c9e-152">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="65c9e-152">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="65c9e-153">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="65c9e-153">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65c9e-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65c9e-154">Requirements</span></span>



| <span data-ttu-id="65c9e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="65c9e-155">Requirement</span></span> | <span data-ttu-id="65c9e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="65c9e-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65c9e-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65c9e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="65c9e-158">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65c9e-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65c9e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="65c9e-160">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65c9e-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65c9e-161">DLL</span><span class="sxs-lookup"><span data-stu-id="65c9e-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65c9e-162"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65c9e-162"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c9e-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="65c9e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c9e-164">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="65c9e-164">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="65c9e-165">**SignerFreeSignerContext**</span><span class="sxs-lookup"><span data-stu-id="65c9e-165">**SignerFreeSignerContext**</span></span>](signerfreesignercontext.md)
</dt> </dl>

 

 
