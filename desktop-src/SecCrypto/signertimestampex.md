---
description: Time carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de contexto de signatário \_ que contém um ponteiro para um blob.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: Função SignerTimeStampEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662912"
---
# <a name="signertimestampex-function"></a><span data-ttu-id="59567-103">Função SignerTimeStampEx</span><span class="sxs-lookup"><span data-stu-id="59567-103">SignerTimeStampEx function</span></span>

<span data-ttu-id="59567-104">O tempo da função **SignerTimeStampEx** carimba o assunto especificado e, opcionalmente, retorna um ponteiro para uma estrutura de [**\_ contexto de signatário**](signer-context.md) que contém um ponteiro para um [*blob*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="59567-104">The **SignerTimeStampEx** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="59567-105">Essa função dá suporte a carimbo de data/hora de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="59567-105">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="59567-106">Para executar o carimbo de data/hora da RFC 3161 (infraestrutura de chave pública) X. 509, use a função [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="59567-106">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="59567-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="59567-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="59567-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="59567-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="59567-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59567-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="59567-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59567-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59567-111">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59567-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59567-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="59567-112">Reserved.</span></span> <span data-ttu-id="59567-113">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="59567-113">This parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="59567-114">*pSubjectInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59567-114">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59567-115">O endereço de uma estrutura de [**\_ \_ informações de assunto de assinante**](signer-subject-info.md) que representa o assunto a ser carimbado.</span><span class="sxs-lookup"><span data-stu-id="59567-115">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="59567-116">*pwszHttpTimeStamp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59567-116">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59567-117">O endereço de uma cadeia de caracteres Unicode terminada em nulo que contém a URL de um servidor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="59567-117">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="59567-118">*psRequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59567-118">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59567-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59567-119">Optional.</span></span> <span data-ttu-id="59567-120">O endereço de uma estrutura de [**\_ atributos cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contém atributos adicionais que são adicionados à solicitação de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="59567-120">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="59567-121">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="59567-121">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="59567-122">*pSipData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59567-122">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59567-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59567-123">Optional.</span></span> <span data-ttu-id="59567-124">Um valor de 32 bits que é passado como dados adicionais para funções de SIP ( [*pacote de interface de entidade*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="59567-124">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="59567-125">O formato e o conteúdo desse parâmetro são definidos pelo provedor SIP.</span><span class="sxs-lookup"><span data-stu-id="59567-125">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="59567-126">Esse parâmetro é opcional e pode ser **nulo** se não estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="59567-126">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="59567-127">*ppSignerContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59567-127">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59567-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59567-128">Optional.</span></span> <span data-ttu-id="59567-129">O endereço de um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) que contém o blob assinado.</span><span class="sxs-lookup"><span data-stu-id="59567-129">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="59567-130">Quando você terminar de usar a estrutura de **\_ contexto do assinante** , libere-a chamando a função [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="59567-130">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59567-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59567-131">Return value</span></span>

<span data-ttu-id="59567-132">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59567-132">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="59567-133">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="59567-133">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="59567-134">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="59567-134">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59567-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59567-135">Requirements</span></span>



| <span data-ttu-id="59567-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="59567-136">Requirement</span></span> | <span data-ttu-id="59567-137">Valor</span><span class="sxs-lookup"><span data-stu-id="59567-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59567-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59567-138">Minimum supported client</span></span><br/> | <span data-ttu-id="59567-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="59567-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="59567-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59567-140">Minimum supported server</span></span><br/> | <span data-ttu-id="59567-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59567-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59567-142">DLL</span><span class="sxs-lookup"><span data-stu-id="59567-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59567-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59567-143"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59567-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="59567-144">See also</span></span>

<dl> <span data-ttu-id="59567-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="59567-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="59567-146">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="59567-146">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> </dl>

 

 
