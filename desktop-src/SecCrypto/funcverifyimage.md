---
description: Usado por um CSP (provedor de serviços de criptografia) para verificar a assinatura de uma DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: Ponteiro de função CRYPT_VERIFY_IMAGE (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813108"
---
# <a name="crypt_verify_image-function-pointer"></a><span data-ttu-id="005ac-103">\_Ponteiro de função de imagem de verificação cript \_</span><span class="sxs-lookup"><span data-stu-id="005ac-103">CRYPT\_VERIFY\_IMAGE function pointer</span></span>

<span data-ttu-id="005ac-104">A função de retorno de chamada **FuncVerifyImage** é usada por um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para verificar a assinatura de uma dll.</span><span class="sxs-lookup"><span data-stu-id="005ac-104">The **FuncVerifyImage** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to verify the signature of a DLL.</span></span>

<span data-ttu-id="005ac-105">Todas as DLLs auxiliares nas quais um CSP faz chamadas de função devem ser assinadas da mesma maneira (e com a mesma chave) que a DLL do CSP primário.</span><span class="sxs-lookup"><span data-stu-id="005ac-105">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="005ac-106">Para garantir essa assinatura, as DLLs auxiliares devem ser carregadas dinamicamente usando a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="005ac-106">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="005ac-107">Mas, antes que a DLL seja carregada, a assinatura da DLL deve ser verificada.</span><span class="sxs-lookup"><span data-stu-id="005ac-107">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="005ac-108">O CSP executa essa verificação chamando a função **FuncVerifyImage** , conforme mostrado no exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="005ac-108">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

## <a name="syntax"></a><span data-ttu-id="005ac-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="005ac-109">Syntax</span></span>


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a><span data-ttu-id="005ac-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="005ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="005ac-111">*lpszImage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="005ac-111">*lpszImage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005ac-112">O endereço de uma cadeia de caracteres terminada em nulo que contém o caminho e o nome do arquivo da DLL para verificar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="005ac-112">The address of a null-terminated string that contains the path and file name of the DLL to verify the signature for.</span></span>

</dd> <dt>

<span data-ttu-id="005ac-113">*pbSigData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="005ac-113">*pbSigData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005ac-114">O endereço de um buffer que contém a assinatura.</span><span class="sxs-lookup"><span data-stu-id="005ac-114">The address of a buffer that contains the signature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="005ac-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="005ac-115">Return value</span></span>

<span data-ttu-id="005ac-116">Retornará **true** se a função for bem-sucedida, **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="005ac-116">Returns **TRUE** if the function succeeds, **FALSE** if it fails.</span></span>

## <a name="examples"></a><span data-ttu-id="005ac-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="005ac-117">Examples</span></span>

<span data-ttu-id="005ac-118">O exemplo a seguir mostra como usar a função de retorno de chamada **FuncVerifyImage** para verificar a assinatura de uma DLL antes de ser carregada por um CSP.</span><span class="sxs-lookup"><span data-stu-id="005ac-118">The following example shows how to use the **FuncVerifyImage** callback function to verify the signature of a DLL before it is loaded by a CSP.</span></span>


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a><span data-ttu-id="005ac-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="005ac-119">Requirements</span></span>



| <span data-ttu-id="005ac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="005ac-120">Requirement</span></span> | <span data-ttu-id="005ac-121">Valor</span><span class="sxs-lookup"><span data-stu-id="005ac-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="005ac-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="005ac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="005ac-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="005ac-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="005ac-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="005ac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="005ac-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="005ac-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="005ac-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="005ac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="005ac-127"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="005ac-127"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005ac-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="005ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005ac-129">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="005ac-129">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="005ac-130">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="005ac-130">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
