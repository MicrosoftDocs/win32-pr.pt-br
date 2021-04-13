---
description: Obtém um identificador para um CSP (provedor de serviços de criptografia) e uma especificação de chave para um contexto de certificado.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: Função GetCryptProvFromCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297674"
---
# <a name="getcryptprovfromcert-function"></a><span data-ttu-id="65065-103">Função GetCryptProvFromCert</span><span class="sxs-lookup"><span data-stu-id="65065-103">GetCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65065-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="65065-104">This API is deprecated.</span></span> <span data-ttu-id="65065-105">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="65065-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="65065-106">A função **GetCryptProvFromCert** Obtém um identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e uma especificação de chave para um contexto de [*certificado*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="65065-106">The **GetCryptProvFromCert** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a key specification for a [*certificate*](../secgloss/c-gly.md) context.</span></span> <span data-ttu-id="65065-107">Use essa função para obter acesso à [*chave privada*](../secgloss/p-gly.md) do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="65065-107">Use this function to get access to the [*private key*](../secgloss/p-gly.md) of the certificate issuer.</span></span>

> [!Note]  
> <span data-ttu-id="65065-108">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="65065-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="65065-109">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="65065-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="65065-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65065-110">Syntax</span></span>


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a><span data-ttu-id="65065-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65065-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65065-112">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65065-112">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-113">O identificador da janela a ser usada como o proprietário de qualquer caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="65065-113">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="65065-114">Esse membro não é usado no momento e é ignorado.</span><span class="sxs-lookup"><span data-stu-id="65065-114">This member is not currently used and is ignored.</span></span> <span data-ttu-id="65065-115">É seguro passar **NULL** para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="65065-115">It is safe to pass **NULL** for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="65065-116">*pCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65065-116">*pCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-117">Um ponteiro para uma estrutura de [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado para o certificado.</span><span class="sxs-lookup"><span data-stu-id="65065-117">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="65065-118">*phCryptProv* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="65065-118">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-119">Um ponteiro para uma estrutura [**HCRYPTPROV**](hcryptprov.md) que é um identificador para o CSP.</span><span class="sxs-lookup"><span data-stu-id="65065-119">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure that is a handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="65065-120">*pdwKeySpec* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="65065-120">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-121">A especificação da chave privada a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="65065-121">The specification of the private key to retrieve.</span></span> <span data-ttu-id="65065-122">Os valores possíveis incluem **em \_ keyexchange** ou **na \_ assinatura**.</span><span class="sxs-lookup"><span data-stu-id="65065-122">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="65065-123">*pfDidCryptAcquire* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65065-123">*pfDidCryptAcquire* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-124">Um valor que especifica se a função adquiriu o identificador do provedor com base no certificado.</span><span class="sxs-lookup"><span data-stu-id="65065-124">A value that specifies whether the function acquired the provider handle based on the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="65065-125">*ppwszTmpContainer* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65065-125">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-126">O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária.</span><span class="sxs-lookup"><span data-stu-id="65065-126">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="65065-127">A função **GetCryptProvFromCert** fornece e inicializa o contêiner temporário.</span><span class="sxs-lookup"><span data-stu-id="65065-127">The **GetCryptProvFromCert** function provides and initializes the temporary container.</span></span> <span data-ttu-id="65065-128">Ao chamar **GetCryptProvFromCert**, o endereço deve apontar para um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="65065-128">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="65065-129">*ppwszProviderName* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65065-129">*ppwszProviderName* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-130">O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="65065-130">The address of a pointer to a null-terminated string for the provider name.</span></span> <span data-ttu-id="65065-131">A função **GetCryptProvFromCert** retorna o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="65065-131">The **GetCryptProvFromCert** function returns the provider name.</span></span> <span data-ttu-id="65065-132">Ao chamar **GetCryptProvFromCert**, o endereço deve apontar para um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="65065-132">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="65065-133">*pdwProviderType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="65065-133">*pdwProviderType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65065-134">Especifica o tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="65065-134">Specifies the CSP type.</span></span> <span data-ttu-id="65065-135">Isso pode ser zero ou um dos [tipos de provedor criptográfico](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="65065-135">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="65065-136">Se esse membro for zero, o contêiner de chave será um dos provedores de armazenamento de chaves CNG.</span><span class="sxs-lookup"><span data-stu-id="65065-136">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65065-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65065-137">Return value</span></span>

<span data-ttu-id="65065-138">Após o êxito, essa função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="65065-138">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="65065-139">A função **GetCryptProvFromCert** retornará **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="65065-139">The **GetCryptProvFromCert** function returns **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="65065-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="65065-140">Remarks</span></span>

<span data-ttu-id="65065-141">A ferramenta [MakeCert](makecert.md) chama **GetCryptProvFromCert** quando você a invoca usando a opção de linha de comando **-is** .</span><span class="sxs-lookup"><span data-stu-id="65065-141">The [MakeCert](makecert.md) tool calls **GetCryptProvFromCert** when you invoke it by using the **-is** command line option.</span></span>

<span data-ttu-id="65065-142">Se o parâmetro *pfDidCryptAcquire* for definido como **true**, a função definirá os parâmetros *phCryptProv*, *pdwKeySpec* e *pdwProviderType* para os valores do provedor.</span><span class="sxs-lookup"><span data-stu-id="65065-142">If the *pfDidCryptAcquire* parameter is set to **TRUE**, the function sets *phCryptProv*, *pdwKeySpec*, and *pdwProviderType* parameters to the provider values.</span></span>

<span data-ttu-id="65065-143">Quando você terminar de usar o CSP, libere-o chamando a função [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="65065-143">When you have finished using the CSP, free it by calling the [**FreeCryptProvFromCert**](freecryptprovfromcert.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="65065-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65065-144">Requirements</span></span>



| <span data-ttu-id="65065-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="65065-145">Requirement</span></span> | <span data-ttu-id="65065-146">Valor</span><span class="sxs-lookup"><span data-stu-id="65065-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65065-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65065-147">Minimum supported client</span></span><br/> | <span data-ttu-id="65065-148">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="65065-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65065-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65065-149">Minimum supported server</span></span><br/> | <span data-ttu-id="65065-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65065-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65065-151">DLL</span><span class="sxs-lookup"><span data-stu-id="65065-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65065-152"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65065-152"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
