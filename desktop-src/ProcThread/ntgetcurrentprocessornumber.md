---
description: Recupera o número do processador no qual o thread atual estava sendo executado durante a chamada para essa função.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Função NtGetCurrentProcessorNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757744"
---
# <a name="ntgetcurrentprocessornumber-function"></a><span data-ttu-id="caa4d-103">Função NtGetCurrentProcessorNumber</span><span class="sxs-lookup"><span data-stu-id="caa4d-103">NtGetCurrentProcessorNumber function</span></span>

<span data-ttu-id="caa4d-104">\[O **NtGetCurrentProcessorNumber** pode ser alterado ou indisponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="caa4d-104">\[**NtGetCurrentProcessorNumber** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="caa4d-105">Em vez disso, os aplicativos devem usar a função [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) .\]</span><span class="sxs-lookup"><span data-stu-id="caa4d-105">Applications should use the [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) function instead.\]</span></span>

<span data-ttu-id="caa4d-106">Recupera o número do processador no qual o thread atual estava sendo executado durante a chamada para essa função.</span><span class="sxs-lookup"><span data-stu-id="caa4d-106">Retrieves the number of the processor the current thread was running on during the call to this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="caa4d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="caa4d-107">Syntax</span></span>


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a><span data-ttu-id="caa4d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caa4d-108">Parameters</span></span>

<span data-ttu-id="caa4d-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="caa4d-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="caa4d-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="caa4d-110">Return value</span></span>

<span data-ttu-id="caa4d-111">A função retorna o número de processador atual.</span><span class="sxs-lookup"><span data-stu-id="caa4d-111">The function returns the current processor number.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa4d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="caa4d-112">Remarks</span></span>

<span data-ttu-id="caa4d-113">Essa função é usada para fornecer informações para estimar o desempenho do processo.</span><span class="sxs-lookup"><span data-stu-id="caa4d-113">This function is used to provide information for estimating process performance.</span></span>

<span data-ttu-id="caa4d-114">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="caa4d-114">This function has no associated import library.</span></span> <span data-ttu-id="caa4d-115">Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="caa4d-115">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="caa4d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caa4d-116">Requirements</span></span>



| <span data-ttu-id="caa4d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="caa4d-117">Requirement</span></span> | <span data-ttu-id="caa4d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="caa4d-118">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="caa4d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="caa4d-119">DLL</span></span><br/> | <dl> <span data-ttu-id="caa4d-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caa4d-120"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caa4d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="caa4d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa4d-122">Vários processadores</span><span class="sxs-lookup"><span data-stu-id="caa4d-122">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="caa4d-123">Funções de thread e processo</span><span class="sxs-lookup"><span data-stu-id="caa4d-123">Process and Thread Functions</span></span>](process-and-thread-functions.md)
</dt> <dt>

[<span data-ttu-id="caa4d-124">Processos</span><span class="sxs-lookup"><span data-stu-id="caa4d-124">Processes</span></span>](child-processes.md)
</dt> </dl>

 

 
