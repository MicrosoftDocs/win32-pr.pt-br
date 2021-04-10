---
description: Time carimba o assunto especificado e dá suporte à configuração de carimbos de data/hora em várias assinaturas.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: Função SignerTimeStampEx3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089841"
---
# <a name="signertimestampex3-function"></a><span data-ttu-id="f37f1-103">Função SignerTimeStampEx3</span><span class="sxs-lookup"><span data-stu-id="f37f1-103">SignerTimeStampEx3 function</span></span>

<span data-ttu-id="f37f1-104">O tempo da função **SignerTimeStampEx3** carimba o assunto especificado e dá suporte à definição de carimbos de data/hora em várias assinaturas.</span><span class="sxs-lookup"><span data-stu-id="f37f1-104">The **SignerTimeStampEx3** function time stamps the specified subject and supports setting time stamps on multiple signatures.</span></span>

> [!Note]  
> <span data-ttu-id="f37f1-105">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="f37f1-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="f37f1-106">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="f37f1-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f37f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f37f1-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="f37f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f37f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f37f1-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-110">Sinalizador que especifica o tipo de carimbo de data/hora a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="f37f1-110">Flag that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="f37f1-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f37f1-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="f37f1-112">Os valores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f37f1-112">The values are mutually exclusive.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f37f1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f37f1-113">Value</span></span></th>
<th><span data-ttu-id="f37f1-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f37f1-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="f37f1-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f37f1-115"><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f37f1-116">Especifica um carimbo de data/hora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="f37f1-116">Specifies an Authenticode time stamp.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f37f1-117">O Authenticode não é mais o tipo preferencial de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="f37f1-117">Authenticode is no longer the preferred type of time stamp.</span></span> <span data-ttu-id="f37f1-118">O suporte para carimbos de data/hora Authenticode pode ser removido no futuro.</span><span class="sxs-lookup"><span data-stu-id="f37f1-118">Support for Authenticode time stamps may be removed in the future.</span></span> <span data-ttu-id="f37f1-119">É recomendável usar a RFC 3161 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="f37f1-119">We recommend that you use RFC 3161 instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="f37f1-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f37f1-120"><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f37f1-121">Especifica um carimbo de data/hora compatível com RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="f37f1-121">Specifies an RFC 3161–compliant time stamp.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f37f1-122">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-122">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-123">Especifica o número de sequência da assinatura à qual o carimbo de data/hora será adicionado.</span><span class="sxs-lookup"><span data-stu-id="f37f1-123">Specifies the sequence number of the signature to which the timestamp will be added.</span></span> <span data-ttu-id="f37f1-124">Se esse valor for zero (0), a assinatura externa estará com carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="f37f1-124">If this value is zero (0), the outer signature will be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-125">*pSubjectInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-125">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-126">O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.</span><span class="sxs-lookup"><span data-stu-id="f37f1-126">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-127">*pwszHttpTimeStamp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-127">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-128">O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="f37f1-128">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-129">*pszAlgorithmOid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-129">*pszAlgorithmOid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-130">Um algoritmo de hash a ser usado para executar carimbos de data/hora compatíveis com o RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="f37f1-130">A hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="f37f1-131">Esse parâmetro é ignorado para carimbos de data/hora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="f37f1-131">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-132">*psRequest* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-132">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f37f1-133">Optional.</span></span> <span data-ttu-id="f37f1-134">O endereço de uma estrutura de [**\_ atributos cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="f37f1-134">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="f37f1-135">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="f37f1-135">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-136">*pSipData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-136">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f37f1-137">Optional.</span></span> <span data-ttu-id="f37f1-138">Um valor de 32 bits que é passado como dados adicionais para funções de SIP ( [*pacote de interface de entidade*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="f37f1-138">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="f37f1-139">O formato e o conteúdo desse parâmetro são definidos pelo provedor SIP.</span><span class="sxs-lookup"><span data-stu-id="f37f1-139">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="f37f1-140">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="f37f1-140">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-141">*ppSignerContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-141">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f37f1-142">Optional.</span></span> <span data-ttu-id="f37f1-143">O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o blob assinado.</span><span class="sxs-lookup"><span data-stu-id="f37f1-143">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="f37f1-144">Quando você terminar de usar a estrutura de **\_ contexto do assinante** , libere-a chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="f37f1-144">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-145">*pCryptoPolicy* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-145">*pCryptoPolicy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f37f1-146">Se presente, um ponteiro para uma estrutura de [**\_ \_ sinal \_ de segurança de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) que contém os parâmetros usados para verificar se há assinaturas fortes.</span><span class="sxs-lookup"><span data-stu-id="f37f1-146">If present, a pointer to a [**CERT\_STRONG\_SIGN\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) structure that contains the parameters used to check for strong signatures.</span></span> <span data-ttu-id="f37f1-147">O carimbo de data/hora deve passar nesta política criptográfica.</span><span class="sxs-lookup"><span data-stu-id="f37f1-147">The time stamp must pass this cryptographic policy.</span></span>

</dd> <dt>

<span data-ttu-id="f37f1-148">*Preservação*</span><span class="sxs-lookup"><span data-stu-id="f37f1-148">*pReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="f37f1-149">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f37f1-149">Reserved.</span></span> <span data-ttu-id="f37f1-150">Esse valor deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f37f1-150">This value must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f37f1-151">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f37f1-151">Return value</span></span>

<span data-ttu-id="f37f1-152">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f37f1-152">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="f37f1-153">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="f37f1-153">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="f37f1-154">Os códigos de erro possíveis retornados por essa função incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f37f1-154">Possible error codes returned by this function include, but are not limited to, the following.</span></span> <span data-ttu-id="f37f1-155">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="f37f1-155">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f37f1-156">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f37f1-156">Return code</span></span></th>
<th><span data-ttu-id="f37f1-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="f37f1-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="f37f1-158"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f37f1-158"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f37f1-159">Esse erro pode ser retornado para as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="f37f1-159">This error can be returned for the following conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="f37f1-160">Você deve definir <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> ou <strong>SIGNER_TIMESTAMP_RFC3161</strong> para o parâmetro <em>dwFlags</em> .</span><span class="sxs-lookup"><span data-stu-id="f37f1-160">You must set either <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> or <strong>SIGNER_TIMESTAMP_RFC3161</strong> for the <em>dwFlags</em> parameter.</span></span></li>
<li><span data-ttu-id="f37f1-161">O parâmetro <em>preservado</em> deve ser <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="f37f1-161">The <em>pReserved</em> parameter must be <strong>NULL</strong>.</span></span></li>
<li><span data-ttu-id="f37f1-162">Se você definir o sinalizador <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> no parâmetro <em>dwFlags</em> , deverá definir o parâmetro <em>dwIndex</em> como zero.</span><span class="sxs-lookup"><span data-stu-id="f37f1-162">If you set the <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> flag in the <em>dwFlags</em> parameter, you must set the <em>dwIndex</em> parameter to zero.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f37f1-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f37f1-163">Requirements</span></span>



| <span data-ttu-id="f37f1-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="f37f1-164">Requirement</span></span> | <span data-ttu-id="f37f1-165">Valor</span><span class="sxs-lookup"><span data-stu-id="f37f1-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f37f1-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f37f1-166">Minimum supported client</span></span><br/> | <span data-ttu-id="f37f1-167">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-167">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f37f1-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f37f1-168">Minimum supported server</span></span><br/> | <span data-ttu-id="f37f1-169">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f37f1-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f37f1-170">DLL</span><span class="sxs-lookup"><span data-stu-id="f37f1-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f37f1-171"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f37f1-171"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f37f1-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="f37f1-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f37f1-173">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="f37f1-173">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="f37f1-174">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="f37f1-174">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> <dt>

[<span data-ttu-id="f37f1-175">**SignerTimeStampEx2**</span><span class="sxs-lookup"><span data-stu-id="f37f1-175">**SignerTimeStampEx2**</span></span>](signertimestampex2.md)
</dt> </dl>

 

 
