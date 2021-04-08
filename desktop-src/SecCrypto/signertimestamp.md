---
description: A hora carimba o assunto especificado. Essa função dá suporte a carimbo de data/hora de Authenticode. Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Função SignerTimeStamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922434"
---
# <a name="signertimestamp-function"></a><span data-ttu-id="81423-105">Função SignerTimeStamp</span><span class="sxs-lookup"><span data-stu-id="81423-105">SignerTimeStamp function</span></span>

<span data-ttu-id="81423-106">O tempo da função **SignerTimeStamp** carimba o assunto especificado.</span><span class="sxs-lookup"><span data-stu-id="81423-106">The **SignerTimeStamp** function time stamps the specified subject.</span></span> <span data-ttu-id="81423-107">Essa função dá suporte a carimbo de data/hora de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="81423-107">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="81423-108">Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="81423-108">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="81423-109">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="81423-109">This function has no associated header file or import library.</span></span> <span data-ttu-id="81423-110">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="81423-110">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="81423-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81423-111">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="81423-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81423-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81423-113">*pSubjectInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81423-113">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81423-114">O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.</span><span class="sxs-lookup"><span data-stu-id="81423-114">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="81423-115">*pwszHttpTimeStamp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81423-115">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81423-116">O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="81423-116">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="81423-117">*psRequest* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="81423-117">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81423-118">O endereço de uma estrutura de [**\_ atributos cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="81423-118">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="81423-119">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="81423-119">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="81423-120">*pSipData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="81423-120">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81423-121">Um valor de 32 bits que é passado como dados adicionais para funções SIP.</span><span class="sxs-lookup"><span data-stu-id="81423-121">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="81423-122">O formato e o conteúdo deste são definidos pelo provedor SIP.</span><span class="sxs-lookup"><span data-stu-id="81423-122">The format and content of this is defined by the SIP provider.</span></span>

<span data-ttu-id="81423-123">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="81423-123">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81423-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81423-124">Return value</span></span>

<span data-ttu-id="81423-125">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81423-125">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="81423-126">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="81423-126">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="81423-127">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="81423-127">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81423-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81423-128">Requirements</span></span>



| <span data-ttu-id="81423-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="81423-129">Requirement</span></span> | <span data-ttu-id="81423-130">Valor</span><span class="sxs-lookup"><span data-stu-id="81423-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81423-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81423-131">Minimum supported client</span></span><br/> | <span data-ttu-id="81423-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="81423-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="81423-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81423-133">Minimum supported server</span></span><br/> | <span data-ttu-id="81423-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81423-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81423-135">DLL</span><span class="sxs-lookup"><span data-stu-id="81423-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81423-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81423-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
