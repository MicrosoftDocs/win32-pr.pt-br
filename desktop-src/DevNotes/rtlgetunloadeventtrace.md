---
description: Permite que o código de despejo obtenha as informações do módulo descarregado de Ntdll.dll para armazenamento no minidespejo.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Função RtlGetUnloadEventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748686"
---
# <a name="rtlgetunloadeventtrace-function"></a><span data-ttu-id="c7959-103">Função RtlGetUnloadEventTrace</span><span class="sxs-lookup"><span data-stu-id="c7959-103">RtlGetUnloadEventTrace function</span></span>

<span data-ttu-id="c7959-104">\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]</span><span class="sxs-lookup"><span data-stu-id="c7959-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="c7959-105">Permite que o código de despejo obtenha as informações do módulo descarregado de Ntdll.dll para armazenamento no minidespejo.</span><span class="sxs-lookup"><span data-stu-id="c7959-105">Enables the dump code to get the unloaded module information from Ntdll.dll for storage in the minidump.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7959-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7959-106">Syntax</span></span>


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="c7959-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7959-107">Parameters</span></span>

<span data-ttu-id="c7959-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c7959-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7959-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c7959-109">Return value</span></span>

<span data-ttu-id="c7959-110">Essa função retorna um ponteiro para uma matriz.</span><span class="sxs-lookup"><span data-stu-id="c7959-110">This function returns a pointer to an array.</span></span> <span data-ttu-id="c7959-111">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="c7959-111">For more information, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7959-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7959-112">Remarks</span></span>

<span data-ttu-id="c7959-113">A matriz RtlpUnloadEventTrace é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c7959-113">The RtlpUnloadEventTrace array is defined as follows:</span></span>

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

<span data-ttu-id="c7959-114">Esta função não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="c7959-114">This function has no associated header file.</span></span> <span data-ttu-id="c7959-115">A biblioteca de importação associada, ntdll. lib, está disponível no Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="c7959-115">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="c7959-116">Você também pode chamar essa função usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c7959-116">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7959-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7959-117">Requirements</span></span>



| <span data-ttu-id="c7959-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7959-118">Requirement</span></span> | <span data-ttu-id="c7959-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c7959-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7959-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c7959-120">DLL</span></span><br/> | <dl> <span data-ttu-id="c7959-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7959-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
