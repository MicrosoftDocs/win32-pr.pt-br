---
title: Função TF_InvalidAssemblyListCacheIfExist
description: A \_ função TF InvalidAssemblyListCacheIfExist invalida o cache de descrição do processador de entrada de texto.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- Estrutura de serviços de texto de função TF_InvalidAssemblyListCacheIfExist
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499305"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a><span data-ttu-id="0b01d-104">\_Função TF InvalidAssemblyListCacheIfExist</span><span class="sxs-lookup"><span data-stu-id="0b01d-104">TF\_InvalidAssemblyListCacheIfExist function</span></span>

<span data-ttu-id="0b01d-105">A função **TF \_ InvalidAssemblyListCacheIfExist** invalida o cache de descrição do processador de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="0b01d-105">The **TF\_InvalidAssemblyListCacheIfExist** function invalidates the text input processor's description cache.</span></span> <span data-ttu-id="0b01d-106">Não é necessário chamar essa função se o programa de configuração do processador de entrada exigir que você reinicie ou faça logon.</span><span class="sxs-lookup"><span data-stu-id="0b01d-106">It is not necessary to call this function if the input processor setup program requires you to restart or log on.</span></span> <span data-ttu-id="0b01d-107">O cache é válido até que o usuário faça logoff.</span><span class="sxs-lookup"><span data-stu-id="0b01d-107">The cache is valid until the user logs off.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b01d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b01d-108">Syntax</span></span>


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a><span data-ttu-id="0b01d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b01d-109">Parameters</span></span>

<span data-ttu-id="0b01d-110">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0b01d-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b01d-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0b01d-111">Return value</span></span>

<span data-ttu-id="0b01d-112">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0b01d-112">This function can return one of these values.</span></span>



| <span data-ttu-id="0b01d-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0b01d-113">Return code</span></span>                                                                            | <span data-ttu-id="0b01d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b01d-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0b01d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b01d-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0b01d-116">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0b01d-116">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="0b01d-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0b01d-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0b01d-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="0b01d-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="0b01d-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b01d-119">Examples</span></span>

<span data-ttu-id="0b01d-120">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="0b01d-120">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="0b01d-121">O exemplo a seguir demonstra como obter um ponteiro para essa função.</span><span class="sxs-lookup"><span data-stu-id="0b01d-121">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="0b01d-122">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="0b01d-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="0b01d-123">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0b01d-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a><span data-ttu-id="0b01d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b01d-124">Requirements</span></span>



| <span data-ttu-id="0b01d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b01d-125">Requirement</span></span> | <span data-ttu-id="0b01d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0b01d-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0b01d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b01d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b01d-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b01d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0b01d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b01d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b01d-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b01d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0b01d-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0b01d-131">Redistributable</span></span><br/>          | <span data-ttu-id="0b01d-132">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0b01d-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="0b01d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0b01d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b01d-134"><dt>Msctf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b01d-134"><dt>Msctf.dll</dt></span></span> </dl> |



 

