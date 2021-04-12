---
description: Cria um contêiner temporário no CSP (provedor de serviços de criptografia) e carrega uma chave privada da memória no contêiner.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: Função PvkPrivateKeyAcquireContextFromMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297346"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a><span data-ttu-id="f5f50-103">Função PvkPrivateKeyAcquireContextFromMemory</span><span class="sxs-lookup"><span data-stu-id="f5f50-103">PvkPrivateKeyAcquireContextFromMemory function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5f50-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="f5f50-104">This API is deprecated.</span></span> <span data-ttu-id="f5f50-105">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="f5f50-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="f5f50-106">A função **PvkPrivateKeyAcquireContextFromMemory** cria um contêiner temporário no CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e carrega uma [*chave privada*](../secgloss/p-gly.md) da memória no contêiner.</span><span class="sxs-lookup"><span data-stu-id="f5f50-106">The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and loads a [*private key*](../secgloss/p-gly.md) from memory into the container.</span></span>

> [!Note]  
> <span data-ttu-id="f5f50-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="f5f50-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="f5f50-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="f5f50-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f5f50-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5f50-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="f5f50-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5f50-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f50-111">*pwszProvName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-111">*pwszProvName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do CSP cujo tipo é solicitado em *dwProvType*.</span><span class="sxs-lookup"><span data-stu-id="f5f50-112">A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-113">*dwProvType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-113">*dwProvType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-114">Um valor **DWORD** para o tipo CSP.</span><span class="sxs-lookup"><span data-stu-id="f5f50-114">A **DWORD** value for the CSP type.</span></span> <span data-ttu-id="f5f50-115">Para obter mais informações sobre tipos de CSP, consulte [tipos de provedor criptográfico](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="f5f50-115">For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-116">*pbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-116">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-117">Um ponteiro para um buffer para receber os dados de contexto.</span><span class="sxs-lookup"><span data-stu-id="f5f50-117">A pointer to a buffer to receive the context data.</span></span> <span data-ttu-id="f5f50-118">O chamador deve fornecer esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f5f50-118">The caller must provide this resource.</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-119">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-119">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-120">Um valor **DWORD** que especifica o tamanho, em bytes, do buffer *pbData* .</span><span class="sxs-lookup"><span data-stu-id="f5f50-120">A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer.</span></span> <span data-ttu-id="f5f50-121">O chamador deve fornecer esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5f50-121">The caller must provide this value.</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-122">*hwndOwner* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-122">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-123">Se uma senha for necessária para descriptografar os dados de contexto apontados pelo parâmetro *pbData* , esse parâmetro será um identificador para o pai da caixa de diálogo; caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f5f50-123">If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-124">*pwszKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-124">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-125">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da chave a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="f5f50-125">A pointer to a null-terminated string that contains the name of the key to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-126">*pdwKeySpec* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-126">*pdwKeySpec* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-127">Um ponteiro para um valor **DWORD** que especifica o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="f5f50-127">A pointer to a **DWORD** value that specifies the type of key.</span></span> <span data-ttu-id="f5f50-128">Os valores possíveis incluem **em \_ keyexchange** ou **na \_ assinatura**.</span><span class="sxs-lookup"><span data-stu-id="f5f50-128">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-129">*phCryptProv* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-129">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-130">Um ponteiro para um identificador para o CSP.</span><span class="sxs-lookup"><span data-stu-id="f5f50-130">A pointer to a handle for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-131">*ppwszTmpContainer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-131">*ppwszTmpContainer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f50-132">O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome de contêiner temporário.</span><span class="sxs-lookup"><span data-stu-id="f5f50-132">The address of a pointer to a null-terminated string for the temporary container name.</span></span> <span data-ttu-id="f5f50-133">A função **PvkPrivateKeyAcquireContextFromMemory** fornece o buffer para essa cadeia de caracteres e a inicializa.</span><span class="sxs-lookup"><span data-stu-id="f5f50-133">The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it.</span></span> <span data-ttu-id="f5f50-134">Ao chamar **PvkPrivateKeyAcquireContextFromMemory**, o endereço deve apontar para um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="f5f50-134">When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f50-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5f50-135">Return value</span></span>

<span data-ttu-id="f5f50-136">Após o êxito, essa função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="f5f50-136">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="f5f50-137">A função **PvkPrivateKeyAcquireContextFromMemory** retornará **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="f5f50-137">The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f50-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5f50-138">Requirements</span></span>



| <span data-ttu-id="f5f50-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f50-139">Requirement</span></span> | <span data-ttu-id="f5f50-140">Valor</span><span class="sxs-lookup"><span data-stu-id="f5f50-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f50-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5f50-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f50-142">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5f50-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5f50-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f50-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5f50-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f5f50-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5f50-146"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5f50-146"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
