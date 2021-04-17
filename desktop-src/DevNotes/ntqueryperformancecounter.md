---
description: Retorna o valor atual de um contador de desempenho e, opcionalmente, a frequência do contador de desempenho.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Função NtQueryPerformanceCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754461"
---
# <a name="ntqueryperformancecounter-function"></a><span data-ttu-id="455fe-103">Função NtQueryPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="455fe-103">NtQueryPerformanceCounter function</span></span>

<span data-ttu-id="455fe-104">\[Essa função não tem suporte e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="455fe-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="455fe-105">Em vez disso, use as funções **QueryPerformanceCounter** e **QueryPerformanceFrequency** .\]</span><span class="sxs-lookup"><span data-stu-id="455fe-105">Use the **QueryPerformanceCounter** and **QueryPerformanceFrequency** functions instead.\]</span></span>

<span data-ttu-id="455fe-106">Retorna o valor atual de um contador de desempenho e, opcionalmente, a frequência do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="455fe-106">Returns the current value of a performance counter and, optionally, the frequency of the performance counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="455fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="455fe-107">Syntax</span></span>


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a><span data-ttu-id="455fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="455fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="455fe-109">*PerformanceCounter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="455fe-109">*PerformanceCounter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="455fe-110">O endereço de uma variável para receber o valor do contador de desempenho atual.</span><span class="sxs-lookup"><span data-stu-id="455fe-110">The address of a variable to receive the current performance counter value.</span></span>

</dd> <dt>

<span data-ttu-id="455fe-111">*PerformanceFrequency* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="455fe-111">*PerformanceFrequency* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="455fe-112">O endereço de uma variável para receber a frequência do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="455fe-112">The address of a variable to receive the performance counter frequency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="455fe-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="455fe-113">Return value</span></span>

<span data-ttu-id="455fe-114">Se a função for bem-sucedida, ela retornará o status de código de **NTSTATUS** **\_ Success**; caso contrário, retornará um código de erro como **status \_ \_ violação de acesso**.</span><span class="sxs-lookup"><span data-stu-id="455fe-114">If the function succeeds, it returns the **NTSTATUS** code **STATUS\_SUCCESS**; otherwise, it returns an error code such as **STATUS\_ACCESS\_VIOLATION**.</span></span>

## <a name="remarks"></a><span data-ttu-id="455fe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="455fe-115">Remarks</span></span>

<span data-ttu-id="455fe-116">Nenhum arquivo de cabeçalho está disponível para **NtQueryPerformanceCounter**.</span><span class="sxs-lookup"><span data-stu-id="455fe-116">No header file is available for **NtQueryPerformanceCounter**.</span></span> <span data-ttu-id="455fe-117">Você deve usar as funções alternativas nomeadas acima, embora também possa usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="455fe-117">You should use the alternative functions named above, although you can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

<span data-ttu-id="455fe-118">Frequência de desempenho é a frequência do contador de desempenho em Hertz, especificamente em contagens por segundo.</span><span class="sxs-lookup"><span data-stu-id="455fe-118">Performance frequency is the frequency of the performance counter in hertz, specifically in counts per second.</span></span> <span data-ttu-id="455fe-119">Esse valor é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="455fe-119">This value is implementation dependent.</span></span> <span data-ttu-id="455fe-120">Se a implementação não tiver hardware para dar suporte ao tempo de desempenho, o valor retornado será 0.</span><span class="sxs-lookup"><span data-stu-id="455fe-120">If the implementation does not have hardware to support performance timing, the value returned is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="455fe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="455fe-121">Requirements</span></span>



| <span data-ttu-id="455fe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="455fe-122">Requirement</span></span> | <span data-ttu-id="455fe-123">Valor</span><span class="sxs-lookup"><span data-stu-id="455fe-123">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="455fe-124">DLL</span><span class="sxs-lookup"><span data-stu-id="455fe-124">DLL</span></span><br/> | <dl> <span data-ttu-id="455fe-125"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="455fe-125"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="455fe-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="455fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455fe-127">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="455fe-127">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[<span data-ttu-id="455fe-128">**QueryPerformanceFrequency**</span><span class="sxs-lookup"><span data-stu-id="455fe-128">**QueryPerformanceFrequency**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
