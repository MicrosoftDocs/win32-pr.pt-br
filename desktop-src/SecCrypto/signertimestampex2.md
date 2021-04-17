---
description: Time carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de contexto de signatário \_ que contém um ponteiro para um blob. Essa função pode ser usada para executar a infraestrutura de chave pública X. 509, RFC 3161&\# 8211; em conformidade, carimbos de data/hora.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: Função SignerTimeStampEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769269"
---
# <a name="signertimestampex2-function"></a><span data-ttu-id="40511-104">Função SignerTimeStampEx2</span><span class="sxs-lookup"><span data-stu-id="40511-104">SignerTimeStampEx2 function</span></span>

<span data-ttu-id="40511-105">O tempo da função **SignerTimeStampEx2** carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de [**\_ contexto de signatário**](signer-context.md) que contém um ponteiro para um [*blob*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="40511-105">The **SignerTimeStampEx2** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="40511-106">Essa função pode ser usada para executar a infraestrutura de chave pública X. 509, em conformidade com a RFC 3161 – carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="40511-106">This function can be used to perform X.509 Public Key Infrastructure, RFC 3161–compliant, time stamps.</span></span>

> [!Note]  
> <span data-ttu-id="40511-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="40511-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="40511-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="40511-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="40511-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40511-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="40511-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40511-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40511-111">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40511-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40511-112">Valor que especifica o tipo de carimbo de data/hora a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="40511-112">Value that specifies the type of time stamp to generate.</span></span> <span data-ttu-id="40511-113">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="40511-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="40511-114">Os valores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="40511-114">The values are mutually exclusive.</span></span>



| <span data-ttu-id="40511-115">Valor</span><span class="sxs-lookup"><span data-stu-id="40511-115">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="40511-116">Significado</span><span class="sxs-lookup"><span data-stu-id="40511-116">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <span data-ttu-id="40511-117"><dt>**\_carimbo de data/hora do signatário \_ AUTHENTICODE**</dt></span><span class="sxs-lookup"><span data-stu-id="40511-117"><dt>**SIGNER\_TIMESTAMP\_AUTHENTICODE**</dt></span></span> </dl> | <span data-ttu-id="40511-118">Especifica um carimbo de data/hora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="40511-118">Specifies an Authenticode time stamp.</span></span><br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <span data-ttu-id="40511-119"><dt>**\_Carimbo de data/hora do signatário \_ RFC3161**</dt></span><span class="sxs-lookup"><span data-stu-id="40511-119"><dt>**SIGNER\_TIMESTAMP\_RFC3161**</dt></span></span> </dl>                | <span data-ttu-id="40511-120">Especifica um carimbo de data/hora compatível com RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="40511-120">Specifies an RFC 3161–compliant time stamp.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="40511-121">*pSubjectInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40511-121">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40511-122">O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.</span><span class="sxs-lookup"><span data-stu-id="40511-122">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="40511-123">*pwszHttpTimeStamp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40511-123">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40511-124">O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="40511-124">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="40511-125">*dwAlgId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40511-125">*dwAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40511-126">Especifica um algoritmo de hash a ser usado para executar carimbos de data/hora compatíveis com RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="40511-126">Specifies a hash algorithm to be used for performing RFC 3161–compliant time stamps.</span></span> <span data-ttu-id="40511-127">Esse parâmetro é ignorado para carimbos de data/hora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="40511-127">This parameter is ignored for Authenticode time stamps.</span></span>

</dd> <dt>

<span data-ttu-id="40511-128">*psRequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40511-128">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40511-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40511-129">Optional.</span></span> <span data-ttu-id="40511-130">O endereço de uma estrutura de [**\_ atributos cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="40511-130">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="40511-131">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="40511-131">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="40511-132">*pSipData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40511-132">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40511-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40511-133">Optional.</span></span> <span data-ttu-id="40511-134">Um valor de 32 bits que é passado como dados adicionais para funções de SIP ( [*pacote de interface de entidade*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="40511-134">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="40511-135">O formato e o conteúdo desse parâmetro são definidos pelo provedor SIP.</span><span class="sxs-lookup"><span data-stu-id="40511-135">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="40511-136">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="40511-136">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="40511-137">*ppSignerContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="40511-137">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40511-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40511-138">Optional.</span></span> <span data-ttu-id="40511-139">O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o blob assinado.</span><span class="sxs-lookup"><span data-stu-id="40511-139">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="40511-140">Quando você terminar de usar a estrutura de **\_ contexto do assinante** , libere-a chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="40511-140">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40511-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40511-141">Return value</span></span>

<span data-ttu-id="40511-142">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40511-142">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="40511-143">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="40511-143">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="40511-144">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="40511-144">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40511-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40511-145">Requirements</span></span>



| <span data-ttu-id="40511-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="40511-146">Requirement</span></span> | <span data-ttu-id="40511-147">Valor</span><span class="sxs-lookup"><span data-stu-id="40511-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40511-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40511-148">Minimum supported client</span></span><br/> | <span data-ttu-id="40511-149">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="40511-149">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="40511-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40511-150">Minimum supported server</span></span><br/> | <span data-ttu-id="40511-151">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="40511-151">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="40511-152">DLL</span><span class="sxs-lookup"><span data-stu-id="40511-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40511-153"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40511-153"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40511-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="40511-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40511-155">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="40511-155">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> <dt>

[<span data-ttu-id="40511-156">**SignerTimeStampEx**</span><span class="sxs-lookup"><span data-stu-id="40511-156">**SignerTimeStampEx**</span></span>](signertimestampex.md)
</dt> </dl>

 

 
