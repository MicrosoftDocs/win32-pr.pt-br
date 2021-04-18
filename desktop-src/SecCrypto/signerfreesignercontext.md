---
description: Libera uma estrutura de \_ contexto de signatário alocada por uma chamada anterior à função SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: Função SignerFreeSignerContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755035"
---
# <a name="signerfreesignercontext-function"></a><span data-ttu-id="f7fd1-103">Função SignerFreeSignerContext</span><span class="sxs-lookup"><span data-stu-id="f7fd1-103">SignerFreeSignerContext function</span></span>

<span data-ttu-id="f7fd1-104">A função **SignerFreeSignerContext** libera uma estrutura [**de \_ contexto de signatário**](signer-context.md) alocada por uma chamada anterior à função [**SignerSignEx**](signersignex.md) .</span><span class="sxs-lookup"><span data-stu-id="f7fd1-104">The **SignerFreeSignerContext** function frees a [**SIGNER\_CONTEXT**](signer-context.md) structure allocated by a previous call to the [**SignerSignEx**](signersignex.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="f7fd1-105">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="f7fd1-106">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f7fd1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7fd1-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="f7fd1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7fd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7fd1-109">*pSignerContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7fd1-109">*pSignerContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7fd1-110">Um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) como gratuito.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-110">A pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7fd1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7fd1-111">Return value</span></span>

<span data-ttu-id="f7fd1-112">Se a função for realizada com sucesso, a função retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-112">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="f7fd1-113">Se a função falhar, ela retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="f7fd1-113">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="f7fd1-114">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="f7fd1-114">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7fd1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7fd1-115">Requirements</span></span>



| <span data-ttu-id="f7fd1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7fd1-116">Requirement</span></span> | <span data-ttu-id="f7fd1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f7fd1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7fd1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7fd1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f7fd1-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f7fd1-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f7fd1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7fd1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f7fd1-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7fd1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7fd1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f7fd1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7fd1-123"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7fd1-123"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7fd1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7fd1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7fd1-125">**contexto do ASSINAnte \_**</span><span class="sxs-lookup"><span data-stu-id="f7fd1-125">**SIGNER\_CONTEXT**</span></span>](signer-context.md)
</dt> <dt>

[<span data-ttu-id="f7fd1-126">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="f7fd1-126">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
