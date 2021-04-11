---
description: Permite que um aplicativo consulte os conjuntos de CPU disponíveis no sistema e seu estado atual.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Função GetSystemCpuSetInformation (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169505"
---
# <a name="getsystemcpusetinformation-function"></a><span data-ttu-id="4f421-103">Função GetSystemCpuSetInformation</span><span class="sxs-lookup"><span data-stu-id="4f421-103">GetSystemCpuSetInformation function</span></span>

<span data-ttu-id="4f421-104">Permite que um aplicativo consulte os conjuntos de CPU disponíveis no sistema e seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="4f421-104">Allows an application to query the available CPU Sets on the system, and their current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f421-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f421-105">Syntax</span></span>


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a><span data-ttu-id="4f421-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f421-107">*Informações* \[ do out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f421-107">*Information* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f421-108">Um ponteiro para uma estrutura de informações do conjunto de CPU do sistema que recebe os dados do conjunto de CPU. [**\_ \_ \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)</span><span class="sxs-lookup"><span data-stu-id="4f421-108">A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data.</span></span> <span data-ttu-id="4f421-109">Passe NULL com um comprimento de buffer de 0 para determinar o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="4f421-109">Pass NULL with a buffer length of 0 to determine the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="4f421-110">*BufferLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f421-110">*BufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f421-111">O comprimento, em bytes, do buffer de saída passado como o argumento de informações.</span><span class="sxs-lookup"><span data-stu-id="4f421-111">The length, in bytes, of the output buffer passed as the Information argument.</span></span>

</dd> <dt>

<span data-ttu-id="4f421-112">*ReturnedLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4f421-112">*ReturnedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f421-113">O comprimento, em bytes, dos dados válidos no buffer de saída se o buffer for grande o suficiente ou o tamanho necessário do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="4f421-113">The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer.</span></span> <span data-ttu-id="4f421-114">Se não houver nenhum conjunto de CPU, esse valor será 0.</span><span class="sxs-lookup"><span data-stu-id="4f421-114">If no CPU Sets exist, this value will be 0.</span></span>

</dd> <dt>

<span data-ttu-id="4f421-115">*Processo* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f421-115">*Process* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f421-116">Um identificador opcional para um processo.</span><span class="sxs-lookup"><span data-stu-id="4f421-116">An optional handle to a process.</span></span> <span data-ttu-id="4f421-117">Esse processo é usado para determinar o valor do sinalizador **AllocatedToTargetProcess** na estrutura de informações do conjunto de CPU do sistema \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4f421-117">This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure.</span></span> <span data-ttu-id="4f421-118">Se um conjunto de CPU for alocado para o processo especificado, o sinalizador será definido.</span><span class="sxs-lookup"><span data-stu-id="4f421-118">If a CPU Set is allocated to the specified process, the flag is set.</span></span> <span data-ttu-id="4f421-119">Caso contrário, fica claro.</span><span class="sxs-lookup"><span data-stu-id="4f421-119">Otherwise, it is clear.</span></span> <span data-ttu-id="4f421-120">Esse identificador deve ter o \_ direito de \_ acesso de informações limitado à consulta de processo \_ .</span><span class="sxs-lookup"><span data-stu-id="4f421-120">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="4f421-121">O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="4f421-121">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="4f421-122">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="4f421-122">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="4f421-123">Reservado, deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="4f421-123">Reserved, must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f421-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f421-124">Return value</span></span>

<span data-ttu-id="4f421-125">Se a API for realizada com sucesso, ela retornará TRUE.</span><span class="sxs-lookup"><span data-stu-id="4f421-125">If the API succeeds it returns TRUE.</span></span> <span data-ttu-id="4f421-126">Se falhar, o motivo do erro estará disponível por meio de **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="4f421-126">If it fails, the error reason is available through **GetLastError**.</span></span> <span data-ttu-id="4f421-127">Se o buffer de informações era nulo ou não é grande o suficiente, o buffer de erro de código de erro \_ insuficiente \_ é retornado.</span><span class="sxs-lookup"><span data-stu-id="4f421-127">If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned.</span></span> <span data-ttu-id="4f421-128">Essa API não pode falhar quando passou parâmetros válidos e um buffer que é grande o suficiente para conter todos os dados de retorno.</span><span class="sxs-lookup"><span data-stu-id="4f421-128">This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f421-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f421-129">Requirements</span></span>



| <span data-ttu-id="4f421-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f421-130">Requirement</span></span> | <span data-ttu-id="4f421-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4f421-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f421-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f421-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4f421-133">\[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="4f421-133">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="4f421-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f421-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4f421-135">Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4f421-135">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="4f421-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f421-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f421-137"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f421-137"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="4f421-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f421-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f421-139"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f421-139"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="4f421-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4f421-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f421-141"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f421-141"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

