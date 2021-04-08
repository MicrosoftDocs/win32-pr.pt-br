---
description: Chama a função GetLastError e converte o código de retorno em um HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: Função SignError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010553"
---
# <a name="signerror-function"></a><span data-ttu-id="7fbba-103">Função SignError</span><span class="sxs-lookup"><span data-stu-id="7fbba-103">SignError function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fbba-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="7fbba-104">This API is deprecated.</span></span> <span data-ttu-id="7fbba-105">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="7fbba-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="7fbba-106">A função **SignError** chama a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte o código de retorno em um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7fbba-106">The **SignError** function calls the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and converts the return code to an **HRESULT**.</span></span>

> [!Note]  
> <span data-ttu-id="7fbba-107">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="7fbba-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="7fbba-108">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="7fbba-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7fbba-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fbba-109">Syntax</span></span>


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a><span data-ttu-id="7fbba-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fbba-110">Parameters</span></span>

<span data-ttu-id="7fbba-111">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7fbba-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fbba-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7fbba-112">Return value</span></span>

<span data-ttu-id="7fbba-113">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7fbba-113">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="7fbba-114">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="7fbba-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="7fbba-115">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="7fbba-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbba-116">Requirements</span></span>



| <span data-ttu-id="7fbba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbba-117">Requirement</span></span> | <span data-ttu-id="7fbba-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbba-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbba-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fbba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbba-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7fbba-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7fbba-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fbba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbba-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fbba-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7fbba-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7fbba-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fbba-124"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fbba-124"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
