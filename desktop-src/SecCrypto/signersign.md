---
description: Assina o arquivo especificado.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Função SignerSign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788100"
---
# <a name="signersign-function"></a><span data-ttu-id="a0a04-103">Função SignerSign</span><span class="sxs-lookup"><span data-stu-id="a0a04-103">SignerSign function</span></span>

<span data-ttu-id="a0a04-104">A função **SignerSign** assina o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a0a04-104">The **SignerSign** function signs the specified file.</span></span>

> [!Note]  
> <span data-ttu-id="a0a04-105">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="a0a04-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="a0a04-106">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="a0a04-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a0a04-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0a04-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="a0a04-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0a04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a04-109">*pSubjectInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-109">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a04-110">Um ponteiro para uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que especifica o assunto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="a0a04-110">A pointer to a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that specifies the subject to sign.</span></span>

</dd> <dt>

<span data-ttu-id="a0a04-111">*pSignerCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-111">*pSignerCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a04-112">Um ponteiro para uma estrutura de [**\_ certificado de signatário**](signer-cert.md) que especifica o certificado a ser usado para criar a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="a0a04-112">A pointer to a [**SIGNER\_CERT**](signer-cert.md) structure that specifies the certificate to use to create the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="a0a04-113">*pSignatureInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-113">*pSignatureInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a04-114">Um ponteiro para uma estrutura de [**\_ \_ informações de assinatura de assinante**](signer-signature-info.md) que contém informações sobre a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="a0a04-114">A pointer to a [**SIGNER\_SIGNATURE\_INFO**](signer-signature-info.md) structure that contains information about the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="a0a04-115">*pProviderInfo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-115">*pProviderInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a04-116">Um ponteiro para uma estrutura de [**\_ \_ informações do provedor de assinante**](signer-provider-info.md) que especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de [*chave privada*](../secgloss/p-gly.md) usadas para criar a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="a0a04-116">A pointer to a [**SIGNER\_PROVIDER\_INFO**](signer-provider-info.md) structure that specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and [*private key*](../secgloss/p-gly.md) information used to create the digital signature.</span></span>

<span data-ttu-id="a0a04-117">Se o valor desse parâmetro for **nulo**, o valor do parâmetro *pSignerCert* deverá especificar um certificado associado a um CSP.</span><span class="sxs-lookup"><span data-stu-id="a0a04-117">If the value of this parameter is **NULL**, the value of the *pSignerCert* parameter must specify a certificate that is associated with a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="a0a04-118">*pwszHttpTimeStamp* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-118">*pwszHttpTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a04-119">A URL de um servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="a0a04-119">The URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="a0a04-120">*psRequest* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-120">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a04-121">Um ponteiro para uma matriz de estruturas de [**\_ atributo cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) -las que são adicionadas a uma solicitação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0a04-121">A pointer to an array of [**CRYPT\_ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) structures that are added to a sign request.</span></span> <span data-ttu-id="a0a04-122">Esse parâmetro será ignorado se o parâmetro *pwszHttpTimeStamp* não contiver um valor válido que não seja **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a0a04-122">This parameter is ignored if the *pwszHttpTimeStamp* parameter does not contain a valid value that is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a04-123">*pSipData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-123">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a04-124">Um valor de 32 bits que é passado como dados adicionais para funções SIP.</span><span class="sxs-lookup"><span data-stu-id="a0a04-124">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="a0a04-125">O formato e o conteúdo deste são definidos pelo provedor SIP.</span><span class="sxs-lookup"><span data-stu-id="a0a04-125">The format and content of this is defined by the SIP provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a04-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0a04-126">Return value</span></span>

<span data-ttu-id="a0a04-127">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0a04-127">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="a0a04-128">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="a0a04-128">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="a0a04-129">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="a0a04-129">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a04-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0a04-130">Requirements</span></span>



| <span data-ttu-id="a0a04-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a04-131">Requirement</span></span> | <span data-ttu-id="a0a04-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a0a04-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a04-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a04-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a04-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0a04-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a04-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a04-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0a04-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0a04-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a0a04-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0a04-138"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0a04-138"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a04-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0a04-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a04-140">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="a0a04-140">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
