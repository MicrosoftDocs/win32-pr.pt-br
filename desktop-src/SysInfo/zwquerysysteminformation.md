---
description: Recupera as informações do sistema especificadas.
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: Função ZwQuerySystemInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQuerySystemInformation
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 2e516b12e5109470c1ddb86ea6a665ca29f138b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756347"
---
# <a name="zwquerysysteminformation-function"></a><span data-ttu-id="79f50-103">Função ZwQuerySystemInformation</span><span class="sxs-lookup"><span data-stu-id="79f50-103">ZwQuerySystemInformation function</span></span>

<span data-ttu-id="79f50-104">\[O **ZwQuerySystemInformation** não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="79f50-104">\[**ZwQuerySystemInformation** is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79f50-105">Em vez disso, use as funções alternativas listadas neste tópico.\]</span><span class="sxs-lookup"><span data-stu-id="79f50-105">Instead, use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="79f50-106">Recupera as informações do sistema especificadas.</span><span class="sxs-lookup"><span data-stu-id="79f50-106">Retrieves the specified system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f50-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79f50-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="79f50-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79f50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f50-109">*SystemInformationClass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79f50-109">*SystemInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f50-110">O tipo de informações do sistema a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="79f50-110">The type of system information to be retrieved.</span></span> <span data-ttu-id="79f50-111">Esse parâmetro pode ser um dos seguintes valores do tipo de enumeração de **\_ \_ classe de informações do sistema** .</span><span class="sxs-lookup"><span data-stu-id="79f50-111">This parameter can be one of the following values from the **SYSTEM\_INFORMATION\_CLASS** enumeration type.</span></span>

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span data-ttu-id="79f50-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-113">O número de processadores no sistema em uma estrutura **de \_ \_ informações básicas do sistema** .</span><span class="sxs-lookup"><span data-stu-id="79f50-113">The number of processors in the system in a **SYSTEM\_BASIC\_INFORMATION** structure.</span></span> <span data-ttu-id="79f50-114">Em vez disso, use a função [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="79f50-114">Use the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function instead.</span></span>

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span data-ttu-id="79f50-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-116">Uma estrutura **de \_ \_ informações de desempenho do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-116">An opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-117">Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="79f50-117">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span data-ttu-id="79f50-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-119">Uma estrutura **de \_ \_ informações TIMEOFDAY do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-119">An opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-120">Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="79f50-120">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span data-ttu-id="79f50-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-122">Uma matriz de estruturas de **\_ \_ informações de processo do sistema** , uma para cada processo em execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="79f50-122">An array of **SYSTEM\_PROCESS\_INFORMATION** structures, one for each process running in the system.</span></span>

<span data-ttu-id="79f50-123">Essas estruturas contêm informações sobre o uso de recursos de cada processo, incluindo o número de identificadores usados pelo processo, a página de pico de uso do arquivo e o número de páginas de memória que o processo alocou.</span><span class="sxs-lookup"><span data-stu-id="79f50-123">These structures contain information about the resource usage of each process, including the number of handles used by the process, the peak page-file usage, and the number of memory pages that the process has allocated.</span></span>

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span data-ttu-id="79f50-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-125">Uma matriz de estruturas de informações de desempenho do processador do sistema, uma para cada processador instalado no sistema. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-125">An array of **SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION** structures, one for each processor installed in the system.</span></span>

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span data-ttu-id="79f50-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-127">Uma estrutura **de \_ \_ informações de interrupção do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-127">An opaque **SYSTEM\_INTERRUPT\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-128">Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="79f50-128">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span data-ttu-id="79f50-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-130">Uma estrutura **de \_ \_ informações de exceção do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-130">An opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-131">Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="79f50-131">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span data-ttu-id="79f50-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-133">Uma estrutura de **\_ informações de \_ cota \_ de registro do sistema** .</span><span class="sxs-lookup"><span data-stu-id="79f50-133">A **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure.</span></span>

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span data-ttu-id="79f50-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span><span class="sxs-lookup"><span data-stu-id="79f50-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-135">Uma estrutura **de \_ \_ informações** à parte do sistema opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-135">An opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-136">Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="79f50-136">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="79f50-137">*SystemInformation* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="79f50-137">*SystemInformation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="79f50-138">Um ponteiro para um buffer que recebe as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="79f50-138">A pointer to a buffer that receives the requested information.</span></span> <span data-ttu-id="79f50-139">O tamanho e a estrutura dessas informações variam de acordo com o valor do parâmetro *SystemInformationClass* , conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="79f50-139">The size and structure of this information varies depending on the value of the *SystemInformationClass* parameter, as indicated in the following table.</span></span>

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span data-ttu-id="79f50-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_informações básicas do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**SYSTEM\_BASIC\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-141">Quando o parâmetro *SystemInformationClass* é **SystemBasicInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações básica do sistema** individual com o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-141">When the *SystemInformationClass* parameter is **SystemBasicInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

<span data-ttu-id="79f50-142">O membro **NumberOfProcessors** contém o número de processadores presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="79f50-142">The **NumberOfProcessors** member contains the number of processors present in the system.</span></span> <span data-ttu-id="79f50-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) em vez disso para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="79f50-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) instead to retrieve this information.</span></span>

<span data-ttu-id="79f50-144">Os outros membros da estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-144">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span data-ttu-id="79f50-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_informações de desempenho do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**SYSTEM\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-146">Quando o parâmetro *SystemInformationClass* é **SystemPerformanceInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações de desempenho de sistema** opaca para uso na geração de uma semente imprevisível para um gerador de número aleatório.</span><span class="sxs-lookup"><span data-stu-id="79f50-146">When the *SystemInformationClass* parameter is **SystemPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-147">Para essa finalidade, a estrutura tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-147">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="79f50-148">Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-148">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="79f50-149">Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.</span><span class="sxs-lookup"><span data-stu-id="79f50-149">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span data-ttu-id="79f50-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_informações de TIMEOFDAY do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**SYSTEM\_TIMEOFDAY\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-151">Quando o parâmetro *SystemInformationClass* é **SystemTimeOfDayInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma estrutura **de \_ \_ informações TIMEOFDAY do sistema** opaca para uso na geração de uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-151">When the *SystemInformationClass* parameter is **SystemTimeOfDayInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-152">Para essa finalidade, a estrutura tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-152">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

<span data-ttu-id="79f50-153">Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-153">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="79f50-154">Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.</span><span class="sxs-lookup"><span data-stu-id="79f50-154">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span data-ttu-id="79f50-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_informações do processo do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**SYSTEM\_PROCESS\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-156">Quando o parâmetro *SystemInformationClass* é **SystemProcessInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma matriz que contenha tantas estruturas de **\_ \_ informações de processo do sistema** quanto há processos em execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="79f50-156">When the *SystemInformationClass* parameter is **SystemProcessInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processes running in the system.</span></span> <span data-ttu-id="79f50-157">Cada estrutura tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-157">Each structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    PVOID Reserved2[3];
    HANDLE UniqueProcessId;
    PVOID Reserved3;
    ULONG HandleCount;
    BYTE Reserved4[4];
    PVOID Reserved5[11];
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved6[6];
} SYSTEM_PROCESS_INFORMATION;
```

<span data-ttu-id="79f50-158">O membro **NumberOfThreads** contém o número total de threads em execução no momento no processo.</span><span class="sxs-lookup"><span data-stu-id="79f50-158">The **NumberOfThreads** member contains the total number of currently running threads in the process.</span></span>

<span data-ttu-id="79f50-159">O membro **HandleCount** contém o número total de identificadores que estão sendo usados pelo processo em questão; em vez disso, use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="79f50-159">The **HandleCount** member contains the total number of handles being used by the process in question; use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) to retrieve this information instead.</span></span>

<span data-ttu-id="79f50-160">O membro **PeakPagefileUsage** contém o número máximo de bytes de armazenamento de arquivo de página usado pelo processo e o membro **PrivatePageCount** contém o número de páginas de memória alocadas para o uso desse processo.</span><span class="sxs-lookup"><span data-stu-id="79f50-160">The **PeakPagefileUsage** member contains the maximum number of bytes of page-file storage used by the process, and the **PrivatePageCount** member contains the number of memory pages allocated for the use of this process.</span></span>

<span data-ttu-id="79f50-161">Você também pode recuperar essas informações usando a função [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) ou a classe [**de \_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="79f50-161">You can also retrieve this information using either the [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) function or the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span>

<span data-ttu-id="79f50-162">Os outros membros da estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-162">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span data-ttu-id="79f50-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_informações de \_ desempenho do processador do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-164">Quando o parâmetro *SystemInformationClass* é **SystemProcessorPerformanceInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma matriz que contenha tantas estruturas de **\_ \_ informações de processo do sistema** quanto há processadores (CPUs) instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="79f50-164">When the *SystemInformationClass* parameter is **SystemProcessorPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processors (CPUs) installed in the system.</span></span> <span data-ttu-id="79f50-165">Cada estrutura tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-165">Each structure has the following layout:</span></span>

``` syntax
typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="79f50-166">O membro **idletime** contém a quantidade de tempo em que o sistema esteve ocioso, em 1/100ths de um nanossegundo.</span><span class="sxs-lookup"><span data-stu-id="79f50-166">The **IdleTime** member contains the amount of time that the system has been idle, in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="79f50-167">O membro de **kerneltime** contém a quantidade de tempo que o sistema gastou executando no modo kernel (incluindo todos os threads em todos os processos, em todos os processadores), em 1/100ths de um nanossegundo.</span><span class="sxs-lookup"><span data-stu-id="79f50-167">The **KernelTime** member contains the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="79f50-168">O membro **usertime** contém a quantidade de tempo que o sistema gastou executando no modo de usuário (incluindo todos os threads em todos os processos, em todos os processadores), em 1/100ths de um nanossegundo.</span><span class="sxs-lookup"><span data-stu-id="79f50-168">The **UserTime** member contains the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="79f50-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) em vez disso para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="79f50-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) instead to retrieve this information.</span></span>

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span data-ttu-id="79f50-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_informações de interrupção do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**SYSTEM\_INTERRUPT\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-171">Quando o parâmetro *SystemInformationClass* é **SystemInterruptInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma matriz que contém tantas estruturas **de \_ \_ informações de interrupção do sistema** opacas quanto há processadores (CPUs) instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="79f50-171">When the *SystemInformationClass* parameter is **SystemInterruptInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many opaque **SYSTEM\_INTERRUPT\_INFORMATION** structures as there are processors (CPUs) installed on the system.</span></span> <span data-ttu-id="79f50-172">Cada estrutura, ou a matriz como um todo, pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-172">Each structure, or the array as a whole, can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-173">Para essa finalidade, a estrutura tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-173">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

<span data-ttu-id="79f50-174">Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-174">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="79f50-175">Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.</span><span class="sxs-lookup"><span data-stu-id="79f50-175">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span data-ttu-id="79f50-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_informações de exceção do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**SYSTEM\_EXCEPTION\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-177">Quando o parâmetro *SystemInformationClass* é **SystemExceptionInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma estrutura **de \_ \_ informações de exceção do sistema** opaca para uso na geração de uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-177">When the *SystemInformationClass* parameter is **SystemExceptionInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-178">Para essa finalidade, a estrutura tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-178">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

<span data-ttu-id="79f50-179">Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-179">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="79f50-180">Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.</span><span class="sxs-lookup"><span data-stu-id="79f50-180">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span data-ttu-id="79f50-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_informações de cota de registro do sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**SYSTEM\_REGISTRY\_QUOTA\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-182">Quando o parâmetro *SystemInformationClass* é **SystemRegistryQuotaInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ \_ informações de cota de registro de sistema** único com o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-182">When the *SystemInformationClass* parameter is **SystemRegistryQuotaInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

<span data-ttu-id="79f50-183">O membro **RegistryQuotaAllowed** contém o tamanho máximo, em bytes, que o registro pode obter nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="79f50-183">The **RegistryQuotaAllowed** member contains the maximum size, in bytes, that the Registry can attain on this system.</span></span>

<span data-ttu-id="79f50-184">O membro **RegistryQuotaUsed** contém o tamanho atual do registro, em bytes.</span><span class="sxs-lookup"><span data-stu-id="79f50-184">The **RegistryQuotaUsed** member contains the current size of the Registry, in bytes.</span></span>

<span data-ttu-id="79f50-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) em vez disso para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="79f50-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) instead to retrieve this information.</span></span>

<span data-ttu-id="79f50-186">O outro membro da estrutura é reservado para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-186">The other member of the structure is reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span data-ttu-id="79f50-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**informações à parte do sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79f50-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**SYSTEM\_LOOKASIDE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="79f50-188">Quando o parâmetro *SystemInformationClass* é **SystemLookasideInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações** à parte do sistema opaca para uso na geração de uma semente imprevisível para um gerador de números aleatórios.</span><span class="sxs-lookup"><span data-stu-id="79f50-188">When the *SystemInformationClass* parameter is **SystemLookasideInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="79f50-189">Para essa finalidade, a estrutura tem o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="79f50-189">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

<span data-ttu-id="79f50-190">Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-190">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="79f50-191">Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.</span><span class="sxs-lookup"><span data-stu-id="79f50-191">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="79f50-192">*SystemInformationLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79f50-192">*SystemInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f50-193">O tamanho do buffer apontado pelo parâmetro *SystemInformation* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="79f50-193">The size of the buffer pointed to by the *SystemInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="79f50-194">*ReturnLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="79f50-194">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79f50-195">Um ponteiro opcional para um local em que a função grava o tamanho real das informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="79f50-195">An optional pointer to a location where the function writes the actual size of the information requested.</span></span> <span data-ttu-id="79f50-196">Se esse tamanho for menor ou igual ao parâmetro *SystemInformationLength* , a função copiará as informações para o buffer *SystemInformation* ; caso contrário, ele retorna um código de erro NTSTATUS e retorna em *ReturnLength* o tamanho do buffer necessário para receber as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="79f50-196">If that size is less than or equal to the *SystemInformationLength* parameter, the function copies the information into the *SystemInformation* buffer; otherwise, it returns an NTSTATUS error code and returns in *ReturnLength* the size of buffer required to receive the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f50-197">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79f50-197">Return value</span></span>

<span data-ttu-id="79f50-198">Retorna um código de erro ou de êxito de NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="79f50-198">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="79f50-199">Os formulários e o significado dos códigos de erro NTSTATUS são listados no arquivo de cabeçalho Ntstatus. h disponível no DDK e são descritos na documentação do DDK.</span><span class="sxs-lookup"><span data-stu-id="79f50-199">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="79f50-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="79f50-200">Remarks</span></span>

<span data-ttu-id="79f50-201">A função **ZwQuerySystemInformation** e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra.</span><span class="sxs-lookup"><span data-stu-id="79f50-201">The **ZwQuerySystemInformation** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="79f50-202">Para manter a compatibilidade do seu aplicativo, é melhor usar as funções alternativas mencionadas anteriormente em vez disso.</span><span class="sxs-lookup"><span data-stu-id="79f50-202">To maintain the compatibility of your application, it is better to use the alternate functions previously mentioned instead.</span></span>

<span data-ttu-id="79f50-203">Se você usar **ZwQuerySystemInformation**, acesse a função por meio da [vinculação dinâmica em tempo de execução](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span><span class="sxs-lookup"><span data-stu-id="79f50-203">If you do use **ZwQuerySystemInformation**, access the function through [run-time dynamic linking](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span></span> <span data-ttu-id="79f50-204">Isso dá ao seu código uma oportunidade de responder normalmente se a função tiver sido alterada ou removida do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79f50-204">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="79f50-205">As alterações de assinatura, no entanto, podem não ser detectáveis.</span><span class="sxs-lookup"><span data-stu-id="79f50-205">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="79f50-206">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="79f50-206">This function has no associated import library.</span></span> <span data-ttu-id="79f50-207">Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="79f50-207">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="79f50-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79f50-208">Requirements</span></span>



| <span data-ttu-id="79f50-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="79f50-209">Requirement</span></span> | <span data-ttu-id="79f50-210">Valor</span><span class="sxs-lookup"><span data-stu-id="79f50-210">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79f50-211">DLL</span><span class="sxs-lookup"><span data-stu-id="79f50-211">DLL</span></span><br/> | <dl> <span data-ttu-id="79f50-212"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79f50-212"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f50-213">Confira também</span><span class="sxs-lookup"><span data-stu-id="79f50-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f50-214">**GetSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="79f50-214">**GetSystemInfo**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[<span data-ttu-id="79f50-215">**GetProcessHandleCount**</span><span class="sxs-lookup"><span data-stu-id="79f50-215">**GetProcessHandleCount**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[<span data-ttu-id="79f50-216">**GetProcessMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="79f50-216">**GetProcessMemoryInfo**</span></span>](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[<span data-ttu-id="79f50-217">**GetSystemTimes**</span><span class="sxs-lookup"><span data-stu-id="79f50-217">**GetSystemTimes**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[<span data-ttu-id="79f50-218">**GetSystemRegistryQuota**</span><span class="sxs-lookup"><span data-stu-id="79f50-218">**GetSystemRegistryQuota**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

