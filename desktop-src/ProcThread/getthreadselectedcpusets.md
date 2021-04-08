---
description: Retorna a atribuição de conjunto de CPU explícita do thread especificado, se qualquer atribuição tiver sido definida usando a API SetThreadSelectedCpuSets. Se nenhuma atribuição explícita for definida, RequiredIdCount será definido como 0 e a função retornará TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Função GetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011020"
---
# <a name="getthreadselectedcpusets-function"></a><span data-ttu-id="33e6a-104">Função GetThreadSelectedCpuSets</span><span class="sxs-lookup"><span data-stu-id="33e6a-104">GetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="33e6a-105">Retorna a atribuição de conjunto de CPU explícita do thread especificado, se qualquer atribuição tiver sido definida usando a API [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) .</span><span class="sxs-lookup"><span data-stu-id="33e6a-105">Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API.</span></span> <span data-ttu-id="33e6a-106">Se nenhuma atribuição explícita for definida, **RequiredIdCount** será definido como 0 e a função retornará true.</span><span class="sxs-lookup"><span data-stu-id="33e6a-106">If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e6a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33e6a-107">Syntax</span></span>


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="33e6a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33e6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e6a-109">*Thread* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="33e6a-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e6a-110">Especifica o thread para o qual consultar os conjuntos de CPU selecionados.</span><span class="sxs-lookup"><span data-stu-id="33e6a-110">Specifies the thread for which to query the selected CPU Sets.</span></span> <span data-ttu-id="33e6a-111">Esse identificador deve ter o \_ direito de \_ acesso a informações limitadas à consulta de thread \_ .</span><span class="sxs-lookup"><span data-stu-id="33e6a-111">This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="33e6a-112">O valor retornado por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) também pode ser especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="33e6a-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="33e6a-113">*CpuSetIds* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33e6a-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33e6a-114">Especifica um buffer opcional para recuperar a lista de identificadores de conjunto de CPU.</span><span class="sxs-lookup"><span data-stu-id="33e6a-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="33e6a-115">*CpuSetIdCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33e6a-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e6a-116">Especifica a capacidade do buffer especificado em **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="33e6a-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="33e6a-117">Se o buffer for nulo, ele deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="33e6a-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="33e6a-118">*RequiredIdCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="33e6a-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33e6a-119">Especifica a capacidade necessária do buffer para manter a lista completa de conjuntos de CPU selecionados de thread.</span><span class="sxs-lookup"><span data-stu-id="33e6a-119">Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets.</span></span> <span data-ttu-id="33e6a-120">Após o retorno bem-sucedido, isso especifica o número de IDs preenchidas no buffer.</span><span class="sxs-lookup"><span data-stu-id="33e6a-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e6a-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33e6a-121">Return value</span></span>

<span data-ttu-id="33e6a-122">Essa API retorna TRUE em caso de êxito.</span><span class="sxs-lookup"><span data-stu-id="33e6a-122">This API returns TRUE on success.</span></span> <span data-ttu-id="33e6a-123">Se o buffer não for grande o suficiente, o valor **GetLastError** será um \_ buffer insuficiente de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="33e6a-123">If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="33e6a-124">Esta API não pode falhar quando passou parâmetros válidos e o buffer de retorno é grande o suficiente.</span><span class="sxs-lookup"><span data-stu-id="33e6a-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e6a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e6a-125">Requirements</span></span>



| <span data-ttu-id="33e6a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e6a-126">Requirement</span></span> | <span data-ttu-id="33e6a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="33e6a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e6a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e6a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="33e6a-129">\[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="33e6a-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="33e6a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e6a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="33e6a-131">Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="33e6a-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="33e6a-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33e6a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e6a-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e6a-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="33e6a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33e6a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="33e6a-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e6a-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="33e6a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="33e6a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33e6a-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33e6a-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

