---
description: Recupera o tamanho e o local da lista de módulos descarregados dinamicamente para o processo atual.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: Função RtlGetUnloadEventTraceEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756323"
---
# <a name="rtlgetunloadeventtraceex-function"></a><span data-ttu-id="5689b-103">Função RtlGetUnloadEventTraceEx</span><span class="sxs-lookup"><span data-stu-id="5689b-103">RtlGetUnloadEventTraceEx function</span></span>

<span data-ttu-id="5689b-104">Recupera o tamanho e o local da lista de módulos descarregados dinamicamente para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="5689b-104">Retrieves the size and location of the dynamically unloaded module list for the current process.</span></span>

## <a name="syntax"></a><span data-ttu-id="5689b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5689b-105">Syntax</span></span>


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a><span data-ttu-id="5689b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5689b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5689b-107">*Elementos de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5689b-107">*ElementSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5689b-108">Um ponteiro para uma variável que contém o tamanho de um elemento na lista.</span><span class="sxs-lookup"><span data-stu-id="5689b-108">A pointer to a variable that contains the size of an element in the list.</span></span>

</dd> <dt>

<span data-ttu-id="5689b-109">*ElementCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5689b-109">*ElementCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5689b-110">Um ponteiro para uma variável que contém o número de elementos na lista.</span><span class="sxs-lookup"><span data-stu-id="5689b-110">A pointer to a variable that contains the number of elements in the list.</span></span>

</dd> <dt>

<span data-ttu-id="5689b-111">*EventTrace* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5689b-111">*EventTrace* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5689b-112">Um ponteiro para uma matriz de estruturas de **\_ rastreamento de \_ eventos \_ de descarga DPE** .</span><span class="sxs-lookup"><span data-stu-id="5689b-112">A pointer to an array of **RTL\_UNLOAD\_EVENT\_TRACE** structures.</span></span> <span data-ttu-id="5689b-113">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="5689b-113">For more information, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5689b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5689b-114">Return value</span></span>

<span data-ttu-id="5689b-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5689b-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5689b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5689b-116">Remarks</span></span>

<span data-ttu-id="5689b-117">O carregador armazena informações de eventos descarregadas em locais que podem ser lidos entre processos aproveitando o fato de que Ntdll.dll é carregado no mesmo endereço base em todos os processos.</span><span class="sxs-lookup"><span data-stu-id="5689b-117">The loader stores unloaded event information in locations that can be read across processes by taking advantage of the fact that Ntdll.dll is loaded at the same base address in all processes.</span></span> <span data-ttu-id="5689b-118">Quando um depurador precisa consultar informações de módulo descarregadas, ele chama essa função para determinar o endereço no qual as variáveis residem e, em seguida, consulta a memória virtual no processo de destino nesses endereços para ler os valores reais.</span><span class="sxs-lookup"><span data-stu-id="5689b-118">When a debugger needs to query unloaded module information, it calls this function to determine the address at which the variables reside, then queries the virtual memory in the target process at those addresses to read the actual values.</span></span>

<span data-ttu-id="5689b-119">Cada elemento na lista é definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5689b-119">Each element in the list is defined as follows.</span></span>

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

<span data-ttu-id="5689b-120">Esta função não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="5689b-120">This function has no associated header file.</span></span> <span data-ttu-id="5689b-121">A biblioteca de importação associada, ntdll. lib, está disponível no Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="5689b-121">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="5689b-122">Você também pode chamar essa função usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5689b-122">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5689b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5689b-123">Requirements</span></span>



| <span data-ttu-id="5689b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5689b-124">Requirement</span></span> | <span data-ttu-id="5689b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5689b-125">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5689b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5689b-126">DLL</span></span><br/> | <dl> <span data-ttu-id="5689b-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5689b-127"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
