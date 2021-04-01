---
description: 'Libera o identificador para um CSP (provedor de serviços de criptografia) ou para uma chave de Cryptography API: próxima geração (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: Função FreeCryptProvFromCertEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829540"
---
# <a name="freecryptprovfromcertex-function"></a><span data-ttu-id="3e117-103">Função FreeCryptProvFromCertEx</span><span class="sxs-lookup"><span data-stu-id="3e117-103">FreeCryptProvFromCertEx function</span></span>

<span data-ttu-id="3e117-104">A função **FreeCryptProvFromCertEx** libera o identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) ou para uma chave de Cryptography API: próxima geração (CNG).</span><span class="sxs-lookup"><span data-stu-id="3e117-104">The **FreeCryptProvFromCertEx** function releases the handle either to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or to a Cryptography API: Next Generation (CNG) key.</span></span>

> [!Note]  
> <span data-ttu-id="3e117-105">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="3e117-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="3e117-106">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="3e117-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3e117-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e117-107">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="3e117-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e117-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e117-109">*fAcquired* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e117-109">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e117-110">Um valor que especifica se o identificador do provedor foi adquirido do [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3e117-110">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e117-111">*hProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e117-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e117-112">Um identificador para um CSP capicor ou um identificador para uma chave CNG.</span><span class="sxs-lookup"><span data-stu-id="3e117-112">A handle to a CAPICOM CSP or a handle to a CNG key.</span></span>

</dd> <dt>

<span data-ttu-id="3e117-113">*dwKeySpec*</span><span class="sxs-lookup"><span data-stu-id="3e117-113">*dwKeySpec*</span></span> 
</dt> <dd>

<span data-ttu-id="3e117-114">O endereço de uma variável **DWORD** que recebe informações adicionais sobre a chave.</span><span class="sxs-lookup"><span data-stu-id="3e117-114">The address of a **DWORD** variable that receives additional information about the key.</span></span> <span data-ttu-id="3e117-115">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e117-115">This can be one of the following values.</span></span>



| <span data-ttu-id="3e117-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3e117-116">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="3e117-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3e117-117">Meaning</span></span>                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="3e117-118"><dt>**em \_ troca de**</dt></span><span class="sxs-lookup"><span data-stu-id="3e117-118"><dt>**AT\_KEYEXCHANGE**</dt></span></span> </dl>                     | <span data-ttu-id="3e117-119">O par de chaves é um par de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="3e117-119">The key pair is a key exchange pair.</span></span><br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="3e117-120"><dt>**NA \_ assinatura**</dt></span><span class="sxs-lookup"><span data-stu-id="3e117-120"><dt>**AT\_SIGNATURE**</dt></span></span> </dl>                           | <span data-ttu-id="3e117-121">O par de chaves é um par de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="3e117-121">The key pair is a signature pair.</span></span><br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <span data-ttu-id="3e117-122"><dt>**especificação de chave de certificado \_ NCRYPT \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e117-122"><dt>**CERT\_NCRYPT\_KEY\_SPEC**</dt></span></span> </dl> | <span data-ttu-id="3e117-123">A chave é uma chave CNG.</span><span class="sxs-lookup"><span data-stu-id="3e117-123">The key is a CNG key.</span></span><br/> <span data-ttu-id="3e117-124">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="3e117-124">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3e117-125">*pwszCapiProvider* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3e117-125">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e117-126">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="3e117-126">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="3e117-127">*dwProviderType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e117-127">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e117-128">Especifica o tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="3e117-128">Specifies the CSP type.</span></span> <span data-ttu-id="3e117-129">Isso pode ser zero ou um dos [tipos de provedor criptográfico](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="3e117-129">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="3e117-130">Se esse membro for zero, o contêiner de chave será um dos provedores de armazenamento de chaves CNG.</span><span class="sxs-lookup"><span data-stu-id="3e117-130">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="3e117-131">*pwszTmpContainer* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3e117-131">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e117-132">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária.</span><span class="sxs-lookup"><span data-stu-id="3e117-132">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e117-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e117-133">Return value</span></span>

<span data-ttu-id="3e117-134">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3e117-134">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e117-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e117-135">Requirements</span></span>



| <span data-ttu-id="3e117-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e117-136">Requirement</span></span> | <span data-ttu-id="3e117-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3e117-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e117-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e117-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3e117-139">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e117-139">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3e117-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e117-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3e117-141">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="3e117-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3e117-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3e117-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e117-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e117-143"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
