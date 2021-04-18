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
# <a name="zwquerysysteminformation-function"></a>Função ZwQuerySystemInformation

\[O **ZwQuerySystemInformation** não está mais disponível para uso a partir do Windows 8. Em vez disso, use as funções alternativas listadas neste tópico.\]

Recupera as informações do sistema especificadas.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SystemInformationClass* \[ no\]
</dt> <dd>

O tipo de informações do sistema a ser recuperado. Esse parâmetro pode ser um dos seguintes valores do tipo de enumeração de **\_ \_ classe de informações do sistema** .

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**


</dt> <dd>

O número de processadores no sistema em uma estrutura **de \_ \_ informações básicas do sistema** . Em vez disso, use a função [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**


</dt> <dd>

Uma estrutura **de \_ \_ informações de desempenho do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios. Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**


</dt> <dd>

Uma estrutura **de \_ \_ informações TIMEOFDAY do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios. Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**


</dt> <dd>

Uma matriz de estruturas de **\_ \_ informações de processo do sistema** , uma para cada processo em execução no sistema.

Essas estruturas contêm informações sobre o uso de recursos de cada processo, incluindo o número de identificadores usados pelo processo, a página de pico de uso do arquivo e o número de páginas de memória que o processo alocou.

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**


</dt> <dd>

Uma matriz de estruturas de informações de desempenho do processador do sistema, uma para cada processador instalado no sistema. **\_ \_ \_**

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**


</dt> <dd>

Uma estrutura **de \_ \_ informações de interrupção do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios. Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**


</dt> <dd>

Uma estrutura **de \_ \_ informações de exceção do sistema** opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios. Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**


</dt> <dd>

Uma estrutura de **\_ informações de \_ cota \_ de registro do sistema** .

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**


</dt> <dd>

Uma estrutura **de \_ \_ informações** à parte do sistema opaca que pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios. Em vez disso, use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> </dl> </dd> <dt>

*SystemInformation* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um buffer que recebe as informações solicitadas. O tamanho e a estrutura dessas informações variam de acordo com o valor do parâmetro *SystemInformationClass* , conforme indicado na tabela a seguir.

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_informações básicas do sistema \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemBasicInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações básica do sistema** individual com o seguinte layout:

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

O membro **NumberOfProcessors** contém o número de processadores presentes no sistema. Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) em vez disso para recuperar essas informações.

Os outros membros da estrutura são reservados para uso interno pelo sistema operacional.

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_informações de desempenho do sistema \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemPerformanceInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações de desempenho de sistema** opaca para uso na geração de uma semente imprevisível para um gerador de número aleatório. Para essa finalidade, a estrutura tem o seguinte layout:

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.

Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_informações de TIMEOFDAY do sistema \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemTimeOfDayInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma estrutura **de \_ \_ informações TIMEOFDAY do sistema** opaca para uso na geração de uma semente imprevisível para um gerador de números aleatórios. Para essa finalidade, a estrutura tem o seguinte layout:

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.

Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_informações do processo do sistema \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemProcessInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma matriz que contenha tantas estruturas de **\_ \_ informações de processo do sistema** quanto há processos em execução no sistema. Cada estrutura tem o seguinte layout:

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

O membro **NumberOfThreads** contém o número total de threads em execução no momento no processo.

O membro **HandleCount** contém o número total de identificadores que estão sendo usados pelo processo em questão; em vez disso, use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) para recuperar essas informações.

O membro **PeakPagefileUsage** contém o número máximo de bytes de armazenamento de arquivo de página usado pelo processo e o membro **PrivatePageCount** contém o número de páginas de memória alocadas para o uso desse processo.

Você também pode recuperar essas informações usando a função [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) ou a classe [**de \_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) .

Os outros membros da estrutura são reservados para uso interno pelo sistema operacional.

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_informações de \_ desempenho do processador do sistema \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemProcessorPerformanceInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma matriz que contenha tantas estruturas de **\_ \_ informações de processo do sistema** quanto há processadores (CPUs) instalados no sistema. Cada estrutura tem o seguinte layout:

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

O membro **idletime** contém a quantidade de tempo em que o sistema esteve ocioso, em 1/100ths de um nanossegundo.

O membro de **kerneltime** contém a quantidade de tempo que o sistema gastou executando no modo kernel (incluindo todos os threads em todos os processos, em todos os processadores), em 1/100ths de um nanossegundo.

O membro **usertime** contém a quantidade de tempo que o sistema gastou executando no modo de usuário (incluindo todos os threads em todos os processos, em todos os processadores), em 1/100ths de um nanossegundo.

Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) em vez disso para recuperar essas informações.

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_informações de interrupção do sistema \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemInterruptInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma matriz que contém tantas estruturas **de \_ \_ informações de interrupção do sistema** opacas quanto há processadores (CPUs) instalados no sistema. Cada estrutura, ou a matriz como um todo, pode ser usada para gerar uma semente imprevisível para um gerador de números aleatórios. Para essa finalidade, a estrutura tem o seguinte layout:

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.

Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_informações de exceção do sistema \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemExceptionInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para conter uma estrutura **de \_ \_ informações de exceção do sistema** opaca para uso na geração de uma semente imprevisível para um gerador de números aleatórios. Para essa finalidade, a estrutura tem o seguinte layout:

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.

Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_informações de cota de registro do sistema \_ \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemRegistryQuotaInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ \_ informações de cota de registro de sistema** único com o seguinte layout:

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

O membro **RegistryQuotaAllowed** contém o tamanho máximo, em bytes, que o registro pode obter nesse sistema.

O membro **RegistryQuotaUsed** contém o tamanho atual do registro, em bytes.

Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) em vez disso para recuperar essas informações.

O outro membro da estrutura é reservado para uso interno pelo sistema operacional.

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**informações à parte do sistema \_ \_**


</dt> <dd>

Quando o parâmetro *SystemInformationClass* é **SystemLookasideInformation**, o buffer apontado pelo parâmetro *SystemInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações** à parte do sistema opaca para uso na geração de uma semente imprevisível para um gerador de números aleatórios. Para essa finalidade, a estrutura tem o seguinte layout:

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

Os membros individuais da estrutura são reservados para uso interno pelo sistema operacional.

Use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) em vez disso para gerar dados aleatórios criptograficamente.

</dd> </dl> </dd> <dt>

*SystemInformationLength* \[ no\]
</dt> <dd>

O tamanho do buffer apontado pelo parâmetro *SystemInformation* , em bytes.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Um ponteiro opcional para um local em que a função grava o tamanho real das informações solicitadas. Se esse tamanho for menor ou igual ao parâmetro *SystemInformationLength* , a função copiará as informações para o buffer *SystemInformation* ; caso contrário, ele retorna um código de erro NTSTATUS e retorna em *ReturnLength* o tamanho do buffer necessário para receber as informações solicitadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um código de erro ou de êxito de NTSTATUS.

Os formulários e o significado dos códigos de erro NTSTATUS são listados no arquivo de cabeçalho Ntstatus. h disponível no DDK e são descritos na documentação do DDK.

## <a name="remarks"></a>Comentários

A função **ZwQuerySystemInformation** e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra. Para manter a compatibilidade do seu aplicativo, é melhor usar as funções alternativas mencionadas anteriormente em vez disso.

Se você usar **ZwQuerySystemInformation**, acesse a função por meio da [vinculação dinâmica em tempo de execução](/windows/desktop/Dlls/using-run-time-dynamic-linking). Isso dá ao seu código uma oportunidade de responder normalmente se a função tiver sido alterada ou removida do sistema operacional. As alterações de assinatura, no entanto, podem não ser detectáveis.

Esta função não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

