---
description: Verifica a assinatura de um arquivo assinado e Obtém o valor de hash e o identificador do algoritmo para o arquivo.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: Função WTHelperGetFileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921844"
---
# <a name="wthelpergetfilehash-function"></a><span data-ttu-id="2a8d1-103">Função WTHelperGetFileHash</span><span class="sxs-lookup"><span data-stu-id="2a8d1-103">WTHelperGetFileHash function</span></span>

<span data-ttu-id="2a8d1-104">\[A função **WTHelperGetFileHash** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-104">\[The **WTHelperGetFileHash** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2a8d1-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="2a8d1-106">A função **WTHelperGetFileHash** verifica a assinatura de um arquivo assinado e Obtém o valor de hash e o identificador de algoritmo para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-106">The **WTHelperGetFileHash** function verifies the signature of a signed file and obtains the hash value and algorithm identifier for the file.</span></span>

> [!Note]  
> <span data-ttu-id="2a8d1-107">Essa função não é declarada em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-107">This function is not declared in a published header file.</span></span> <span data-ttu-id="2a8d1-108">Para usar essa função, declare-a no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-108">To use this function, declare it in the exact format shown.</span></span> <span data-ttu-id="2a8d1-109">Essa função também não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-109">This function also has no associated import library.</span></span> <span data-ttu-id="2a8d1-110">Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-110">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2a8d1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a8d1-111">Syntax</span></span>


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a><span data-ttu-id="2a8d1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a8d1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a8d1-113">*pwszFilename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-113">*pwszFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8d1-114">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o caminho e o nome de arquivo do arquivo para o qual obter o hash.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-114">A pointer to a null-terminated Unicode string that contains the path and file name of the file to get the hash for.</span></span>

</dd> <dt>

<span data-ttu-id="2a8d1-115">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8d1-116">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-116">This parameter is not used and should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2a8d1-117">*pvReserved* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-117">*pvReserved* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8d1-118">Esse parâmetro não é usado e deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-118">This parameter is not used and should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2a8d1-119">*pbFileHash* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-119">*pbFileHash* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8d1-120">Um ponteiro para um buffer para receber o valor de hash do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-120">A pointer to a buffer to receive the hash value for the file.</span></span> <span data-ttu-id="2a8d1-121">O parâmetro *pcbFileHash* contém o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-121">The *pcbFileHash* parameter contains the size of this buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2a8d1-122">*pcbFileHash* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-122">*pcbFileHash* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8d1-123">Um ponteiro para uma variável **DWORD** que, na entrada, contém o tamanho, em bytes, do buffer *pbFileHash* e, na saída, recebe o tamanho, em bytes, do valor de hash.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-123">A pointer to a **DWORD** variable that, on input, contains the size, in bytes, of the *pbFileHash* buffer and, on output, receives the size, in bytes, of the hash value.</span></span>

<span data-ttu-id="2a8d1-124">Para obter o tamanho necessário do valor de hash, passe **NULL** para o parâmetro *pbFileHash* .</span><span class="sxs-lookup"><span data-stu-id="2a8d1-124">To obtain the required size of the hash value, pass **NULL** for the *pbFileHash* parameter.</span></span> <span data-ttu-id="2a8d1-125">Essa função coloca o tamanho necessário, em bytes, do valor de hash neste local.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-125">This function will place the required size, in bytes, of the hash value in this location.</span></span>

<span data-ttu-id="2a8d1-126">Se o parâmetro *pbFileHash* não for **nulo** e o tamanho não for grande o suficiente para receber o valor de hash, essa função irá inserir o tamanho necessário, em bytes, nesse local e retornará **\_ mais \_ dados de erro**.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-126">If the *pbFileHash* parameter is not **NULL**, and the size is not large enough to receive the hash value, this function will place the required size, in bytes, in this location and return **ERROR\_MORE\_DATA**.</span></span>

</dd> <dt>

<span data-ttu-id="2a8d1-127">*pHashAlgid* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-127">*pHashAlgid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8d1-128">Um ponteiro para uma variável de [**\_ ID alg**](alg-id.md) para receber o identificador do algoritmo usado para criar o valor de hash.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-128">A pointer to an [**ALG\_ID**](alg-id.md) variable to receive the identifier of the algorithm used to create the hash value.</span></span> <span data-ttu-id="2a8d1-129">Esse parâmetro poderá ser **nulo** se essas informações não forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-129">This parameter can be **NULL** if this information is not needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a8d1-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a8d1-130">Return value</span></span>

<span data-ttu-id="2a8d1-131">Retorna um código de status que indica o êxito ou a falha da função.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-131">Returns a status code that indicates the success or failure of the function.</span></span>

<span data-ttu-id="2a8d1-132">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-132">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="2a8d1-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2a8d1-133">Return code</span></span>                                                                                               | <span data-ttu-id="2a8d1-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a8d1-134">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a8d1-135"><dt>**êxito do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a8d1-135"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>             | <span data-ttu-id="2a8d1-136">O arquivo está assinado e a assinatura foi verificada.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-136">The file is signed, and the signature was verified.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="2a8d1-137"><dt>**ERRO de \_ mais \_ dados**</dt></span><span class="sxs-lookup"><span data-stu-id="2a8d1-137"><dt>**ERROR\_MORE\_DATA**</dt></span></span> </dl>          | <span data-ttu-id="2a8d1-138">O parâmetro *pbFileHash* não é **nulo** e o tamanho especificado pelo parâmetro *pcbFileHash* não é grande o suficiente para receber o hash.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-138">The *pbFileHash* parameter is not **NULL**, and the size specified by the *pcbFileHash* parameter is not large enough to receive the hash.</span></span><br/> |
| <dl> <span data-ttu-id="2a8d1-139"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a8d1-139"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="2a8d1-140">Ocorreu uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-140">A memory allocation failure occurred.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="2a8d1-141"><dt>**CONFIAR \_ E \_ má \_ Digest**</dt></span><span class="sxs-lookup"><span data-stu-id="2a8d1-141"><dt>**TRUST\_E\_BAD\_DIGEST**</dt></span></span> </dl>      | <span data-ttu-id="2a8d1-142">A assinatura do arquivo não foi verificada.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-142">The signature of the file was not verified.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="2a8d1-143"><dt>**CONFIAR \_ E \_ noassinatura**</dt></span><span class="sxs-lookup"><span data-stu-id="2a8d1-143"><dt>**TRUST\_E\_NOSIGNATURE**</dt></span></span> </dl>      | <span data-ttu-id="2a8d1-144">O arquivo não foi assinado ou tinha uma assinatura que não é válida.</span><span class="sxs-lookup"><span data-stu-id="2a8d1-144">The file was not signed or had a signature that is not valid.</span></span><br/>                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="2a8d1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a8d1-145">Requirements</span></span>



| <span data-ttu-id="2a8d1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a8d1-146">Requirement</span></span> | <span data-ttu-id="2a8d1-147">Valor</span><span class="sxs-lookup"><span data-stu-id="2a8d1-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8d1-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a8d1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8d1-149">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2a8d1-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a8d1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8d1-151">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a8d1-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a8d1-152">DLL</span><span class="sxs-lookup"><span data-stu-id="2a8d1-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a8d1-153"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a8d1-153"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
