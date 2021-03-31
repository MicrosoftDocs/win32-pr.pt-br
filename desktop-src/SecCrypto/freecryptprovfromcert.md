---
description: Libera o identificador para um CSP (provedor de serviços de criptografia) e, opcionalmente, exclui o contêiner temporário criado pela função GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Função FreeCryptProvFromCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829541"
---
# <a name="freecryptprovfromcert-function"></a><span data-ttu-id="a5ccf-103">Função FreeCryptProvFromCert</span><span class="sxs-lookup"><span data-stu-id="a5ccf-103">FreeCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5ccf-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-104">This API is deprecated.</span></span> <span data-ttu-id="a5ccf-105">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="a5ccf-106">A função **FreeCryptProvFromCert** libera o identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e, opcionalmente, exclui o contêiner temporário criado pela função [**GetCryptProvFromCert**](getcryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="a5ccf-106">The **FreeCryptProvFromCert** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**GetCryptProvFromCert**](getcryptprovfromcert.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="a5ccf-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="a5ccf-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a5ccf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5ccf-109">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="a5ccf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5ccf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5ccf-111">*fAcquired* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5ccf-111">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5ccf-112">Um valor que especifica se o identificador do provedor foi adquirido do [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a5ccf-112">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5ccf-113">*hProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5ccf-113">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5ccf-114">Um ponteiro para uma estrutura [**HCRYPTPROV**](hcryptprov.md) para o CSP.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-114">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="a5ccf-115">*pwszCapiProvider* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a5ccf-115">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5ccf-116">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-116">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="a5ccf-117">*dwProviderType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5ccf-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5ccf-118">Especifica o tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-118">Specifies the CSP type.</span></span> <span data-ttu-id="a5ccf-119">Isso pode ser zero ou um dos [tipos de provedor criptográfico](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="a5ccf-119">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="a5ccf-120">Se esse membro for zero, o contêiner de chave será um dos provedores de armazenamento de chaves CNG.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-120">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="a5ccf-121">*pwszTmpContainer* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a5ccf-121">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5ccf-122">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-122">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5ccf-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5ccf-123">Return value</span></span>

<span data-ttu-id="a5ccf-124">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a5ccf-124">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ccf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5ccf-125">Requirements</span></span>



| <span data-ttu-id="a5ccf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5ccf-126">Requirement</span></span> | <span data-ttu-id="a5ccf-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ccf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ccf-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5ccf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ccf-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a5ccf-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a5ccf-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5ccf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ccf-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a5ccf-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5ccf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a5ccf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5ccf-133"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ccf-133"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
