---
description: Obtém um identificador para um CSP (provedor de serviços de criptografia) baseado em um arquivo de chave privada ou em um nome de contêiner de chave.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: Função PvkGetCryptProv
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837380"
---
# <a name="pvkgetcryptprov-function"></a><span data-ttu-id="95c97-103">Função PvkGetCryptProv</span><span class="sxs-lookup"><span data-stu-id="95c97-103">PvkGetCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95c97-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="95c97-104">This API is deprecated.</span></span> <span data-ttu-id="95c97-105">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="95c97-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="95c97-106">A função **PvkGetCryptProv** Obtém um identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) baseado em um arquivo de [*chave privada*](../secgloss/p-gly.md) ou em um nome de contêiner de chave.</span><span class="sxs-lookup"><span data-stu-id="95c97-106">The **PvkGetCryptProv** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) based on either a [*private key*](../secgloss/p-gly.md) file or a key container name.</span></span>

> [!Note]  
> <span data-ttu-id="95c97-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="95c97-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="95c97-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="95c97-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="95c97-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95c97-109">Syntax</span></span>


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a><span data-ttu-id="95c97-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95c97-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c97-111">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c97-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-112">Se uma senha for necessária para descriptografar o arquivo de chave privada, esse parâmetro será um identificador para o pai da caixa de diálogo de senha; caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="95c97-112">If a password is required to decrypt the private key file, this parameter is a handle to the parent of the password dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="95c97-113">*pwszCaption* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c97-113">*pwszCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-114">Um ponteiro para uma cadeia de caracteres terminada em nulo para a legenda da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="95c97-114">A pointer to a null-terminated string for the dialog box caption.</span></span>

</dd> <dt>

<span data-ttu-id="95c97-115">*pwszCapiProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c97-115">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-116">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do CSP.</span><span class="sxs-lookup"><span data-stu-id="95c97-116">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="95c97-117">*dwProviderType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c97-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-118">Um valor **DWORD** que representa o tipo de provedor criptográfico.</span><span class="sxs-lookup"><span data-stu-id="95c97-118">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="95c97-119">Para obter mais informações, consulte [tipos de provedor criptográfico](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="95c97-119">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="95c97-120">*pwszPvkFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c97-120">*pwszPvkFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-121">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome de um arquivo de chave privada.</span><span class="sxs-lookup"><span data-stu-id="95c97-121">A pointer to a null-terminated string that contains the name of a private key file.</span></span>

</dd> <dt>

<span data-ttu-id="95c97-122">*pwszKeyContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95c97-122">*pwszKeyContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-123">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner da chave privada.</span><span class="sxs-lookup"><span data-stu-id="95c97-123">A pointer to a null-terminated string for the private key container name.</span></span>

</dd> <dt>

<span data-ttu-id="95c97-124">*pdwKeySpec* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95c97-124">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-125">Um ponteiro para um valor **DWORD** para o tipo de chave do contêiner retornado com *phCryptProv* e *ppwszTmpContainer*.</span><span class="sxs-lookup"><span data-stu-id="95c97-125">A pointer to a **DWORD** value for the type of key of the container returned with *phCryptProv* and *ppwszTmpContainer*.</span></span>

</dd> <dt>

<span data-ttu-id="95c97-126">*ppwszTmpContainer* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="95c97-126">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-127">O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária.</span><span class="sxs-lookup"><span data-stu-id="95c97-127">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="95c97-128">A função **PvkGetCryptProv** fornece e inicializa o contêiner temporário.</span><span class="sxs-lookup"><span data-stu-id="95c97-128">The **PvkGetCryptProv** function provides and initializes the temporary container.</span></span> <span data-ttu-id="95c97-129">Ao chamar **PvkGetCryptProv**, o endereço deve apontar para um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="95c97-129">When calling **PvkGetCryptProv**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="95c97-130">*phCryptProv* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95c97-130">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95c97-131">Um ponteiro para um identificador para o CSP.</span><span class="sxs-lookup"><span data-stu-id="95c97-131">A pointer to a handle for the CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c97-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95c97-132">Return value</span></span>

<span data-ttu-id="95c97-133">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="95c97-133">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="95c97-134">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="95c97-134">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="95c97-135">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="95c97-135">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95c97-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="95c97-136">Remarks</span></span>

<span data-ttu-id="95c97-137">A função **PvkGetCryptProv** primeiro tenta obter o identificador do provedor do nome do contêiner de chave especificado pelo parâmetro *pwszKeyContainerName* .</span><span class="sxs-lookup"><span data-stu-id="95c97-137">The **PvkGetCryptProv** function first tries to get the provider handle from the key container name specified by the *pwszKeyContainerName* parameter.</span></span> <span data-ttu-id="95c97-138">Se você passar **NULL** para o parâmetro *pwszKeyContainerName* , **PvkGetCryptProv** tentará obter o provedor do arquivo de chave privada especificado no parâmetro *pwszPvkFile* .</span><span class="sxs-lookup"><span data-stu-id="95c97-138">If you pass **NULL** for the *pwszKeyContainerName* parameter, **PvkGetCryptProv** tries to get the provider from the private key file specified in the *pwszPvkFile* parameter.</span></span>

<span data-ttu-id="95c97-139">Quando você terminar de usar o CSP, libere o identificador do provedor e o contêiner de chave temporária chamando a função [**PvkFreeCryptProv**](pvkfreecryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="95c97-139">When you have finished using the CSP, free the provider handle and temporary key container by calling the [**PvkFreeCryptProv**](pvkfreecryptprov.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c97-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c97-140">Requirements</span></span>



| <span data-ttu-id="95c97-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="95c97-141">Requirement</span></span> | <span data-ttu-id="95c97-142">Valor</span><span class="sxs-lookup"><span data-stu-id="95c97-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95c97-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95c97-143">Minimum supported client</span></span><br/> | <span data-ttu-id="95c97-144">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="95c97-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="95c97-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95c97-145">Minimum supported server</span></span><br/> | <span data-ttu-id="95c97-146">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95c97-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95c97-147">DLL</span><span class="sxs-lookup"><span data-stu-id="95c97-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95c97-148"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95c97-148"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
