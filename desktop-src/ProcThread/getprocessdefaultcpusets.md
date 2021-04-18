---
description: Recupera a lista de conjuntos de CPU no conjunto padrão de processo que foi definido por SetProcessDefaultCpuSets. Se nenhum conjunto de CPU padrão for definido para um determinado processo, o RequiredIdCount será definido como 0 e a função terá sucesso.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Função GetProcessDefaultCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766360"
---
# <a name="getprocessdefaultcpusets-function"></a><span data-ttu-id="c13ca-104">Função GetProcessDefaultCpuSets</span><span class="sxs-lookup"><span data-stu-id="c13ca-104">GetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="c13ca-105">Recupera a lista de conjuntos de CPU no conjunto padrão de processo que foi definido por [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span><span class="sxs-lookup"><span data-stu-id="c13ca-105">Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span></span> <span data-ttu-id="c13ca-106">Se nenhum conjunto de CPU padrão for definido para um determinado processo, o **RequiredIdCount** será definido como 0 e a função terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="c13ca-106">If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c13ca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c13ca-107">Syntax</span></span>


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="c13ca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c13ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c13ca-109">*Processo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c13ca-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c13ca-110">Especifica um identificador de processo para o processo a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="c13ca-110">Specifies a process handle for the process to query.</span></span> <span data-ttu-id="c13ca-111">Esse identificador deve ter o \_ direito de \_ acesso de informações limitado à consulta de processo \_ .</span><span class="sxs-lookup"><span data-stu-id="c13ca-111">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="c13ca-112">O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="c13ca-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="c13ca-113">*CpuSetIds* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c13ca-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c13ca-114">Especifica um buffer opcional para recuperar a lista de identificadores de conjunto de CPU.</span><span class="sxs-lookup"><span data-stu-id="c13ca-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="c13ca-115">*CpuSetIdCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c13ca-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c13ca-116">Especifica a capacidade do buffer especificado em **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="c13ca-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="c13ca-117">Se o buffer for nulo, ele deverá ser 0.</span><span class="sxs-lookup"><span data-stu-id="c13ca-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="c13ca-118">*RequiredIdCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c13ca-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c13ca-119">Especifica a capacidade necessária do buffer para manter a lista completa de conjuntos de CPU de processo padrão.</span><span class="sxs-lookup"><span data-stu-id="c13ca-119">Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets.</span></span> <span data-ttu-id="c13ca-120">Após o retorno bem-sucedido, isso especifica o número de IDs preenchidas no buffer.</span><span class="sxs-lookup"><span data-stu-id="c13ca-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c13ca-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c13ca-121">Return value</span></span>

<span data-ttu-id="c13ca-122">Essa API retorna TRUE em caso de êxito.</span><span class="sxs-lookup"><span data-stu-id="c13ca-122">This API returns TRUE on success.</span></span> <span data-ttu-id="c13ca-123">Se o buffer não for grande o suficiente, a API retornará FALSE e o valor **GetLastError** será um \_ buffer insuficiente de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="c13ca-123">If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="c13ca-124">Esta API não pode falhar quando passou parâmetros válidos e o buffer de retorno é grande o suficiente.</span><span class="sxs-lookup"><span data-stu-id="c13ca-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="c13ca-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c13ca-125">Requirements</span></span>



| <span data-ttu-id="c13ca-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c13ca-126">Requirement</span></span> | <span data-ttu-id="c13ca-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c13ca-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c13ca-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c13ca-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c13ca-129">\[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="c13ca-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="c13ca-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c13ca-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c13ca-131">Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c13ca-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="c13ca-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c13ca-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c13ca-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c13ca-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="c13ca-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c13ca-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c13ca-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="c13ca-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="c13ca-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c13ca-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c13ca-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c13ca-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

