---
description: Salva uma chave privada e sua chave pública correspondente em um arquivo especificado.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Função PvkPrivateKeySave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760381"
---
# <a name="pvkprivatekeysave-function"></a><span data-ttu-id="d8cb0-103">Função PvkPrivateKeySave</span><span class="sxs-lookup"><span data-stu-id="d8cb0-103">PvkPrivateKeySave function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8cb0-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-104">This API is deprecated.</span></span> <span data-ttu-id="d8cb0-105">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="d8cb0-106">A função **PvkPrivateKeySave** salva uma [*chave privada*](../secgloss/p-gly.md) e sua [*chave pública*](../secgloss/p-gly.md) correspondente em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-106">The **PvkPrivateKeySave** function saves a [*private key*](../secgloss/p-gly.md) and its corresponding [*public key*](../secgloss/p-gly.md) to a specified file.</span></span>

> [!Note]  
> <span data-ttu-id="d8cb0-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="d8cb0-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d8cb0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8cb0-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d8cb0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8cb0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8cb0-111">*HCRYPTPROV* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-111">*hCryptProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-112">Um identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="d8cb0-112">A handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="d8cb0-113">*hFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-113">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-114">Um identificador para um arquivo criado com a permissão de leitura/gravação inicial e a permissão de somente leitura subsequente.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-114">A handle to a file created with initial read/write permission and subsequent read-only permission.</span></span>

</dd> <dt>

<span data-ttu-id="d8cb0-115">*dwKeySpec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-115">*dwKeySpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-116">Um inteiro longo para o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-116">A long integer for the type of key.</span></span> <span data-ttu-id="d8cb0-117">Os valores possíveis incluem **em \_ keyexchange** ou **na \_ assinatura**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-117">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="d8cb0-118">*hwndOwner* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-118">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-119">Se uma senha for necessária para criptografar a chave privada, esse parâmetro será um identificador para o pai da caixa de diálogo; caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-119">If a password is required to encrypt the private key, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d8cb0-120">*pwszKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-120">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-121">Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome da chave a ser salva.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-121">A pointer to a null-terminated string for the name of the key to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="d8cb0-122">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-123">Um valor **DWORD** que especifica opções adicionais para a função.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-123">A **DWORD** value that specifies additional options for the function.</span></span> <span data-ttu-id="d8cb0-124">Para obter mais informações, consulte o parâmetro *dwFlags* em [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="d8cb0-124">For more information, see the *dwFlags* parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8cb0-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8cb0-125">Return value</span></span>

<span data-ttu-id="d8cb0-126">Após o êxito, essa função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-126">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="d8cb0-127">A função **PvkPrivateKeySave** retornará **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-127">The **PvkPrivateKeySave** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8cb0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8cb0-128">Requirements</span></span>



| <span data-ttu-id="d8cb0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8cb0-129">Requirement</span></span> | <span data-ttu-id="d8cb0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d8cb0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8cb0-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8cb0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d8cb0-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d8cb0-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8cb0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d8cb0-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8cb0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d8cb0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8cb0-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8cb0-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
