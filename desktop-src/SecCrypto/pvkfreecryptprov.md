---
description: Libera o identificador para um CSP (provedor de serviços de criptografia) e, opcionalmente, exclui o contêiner temporário criado pela função PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: Função PvkFreeCryptProv
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796371"
---
# <a name="pvkfreecryptprov-function"></a><span data-ttu-id="19acd-103">Função PvkFreeCryptProv</span><span class="sxs-lookup"><span data-stu-id="19acd-103">PvkFreeCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19acd-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="19acd-104">This API is deprecated.</span></span> <span data-ttu-id="19acd-105">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="19acd-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="19acd-106">A função **PvkFreeCryptProv** libera o identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e, opcionalmente, exclui o contêiner temporário criado pela função [**PvkGetCryptProv**](pvkgetcryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="19acd-106">The **PvkFreeCryptProv** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**PvkGetCryptProv**](pvkgetcryptprov.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="19acd-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="19acd-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="19acd-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="19acd-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="19acd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19acd-109">Syntax</span></span>


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="19acd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19acd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19acd-111">*hProv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19acd-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19acd-112">Um identificador para o CSP.</span><span class="sxs-lookup"><span data-stu-id="19acd-112">A handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="19acd-113">*pwszCapiProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19acd-113">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19acd-114">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do CSP.</span><span class="sxs-lookup"><span data-stu-id="19acd-114">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="19acd-115">*dwProviderType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19acd-115">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19acd-116">Um valor **DWORD** que representa o tipo de provedor criptográfico.</span><span class="sxs-lookup"><span data-stu-id="19acd-116">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="19acd-117">Para obter mais informações, consulte [tipos de provedor criptográfico](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="19acd-117">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="19acd-118">*pwszTmpContainer* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19acd-118">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19acd-119">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária.</span><span class="sxs-lookup"><span data-stu-id="19acd-119">A pointer to a null-terminated string for the temporary key container name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19acd-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19acd-120">Return value</span></span>

<span data-ttu-id="19acd-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="19acd-121">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="19acd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19acd-122">Requirements</span></span>



| <span data-ttu-id="19acd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19acd-123">Requirement</span></span> | <span data-ttu-id="19acd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="19acd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19acd-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19acd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19acd-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="19acd-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="19acd-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19acd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19acd-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19acd-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19acd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="19acd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19acd-130"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19acd-130"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
