---
description: Recupera informações sobre o processo especificado.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: Função ZwQueryInformationProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQueryInformationProcess
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 30207c8d3d54c54f77194b542e10e9fee94e055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782295"
---
# <a name="zwqueryinformationprocess-function"></a><span data-ttu-id="7f686-103">Função ZwQueryInformationProcess</span><span class="sxs-lookup"><span data-stu-id="7f686-103">ZwQueryInformationProcess function</span></span>

<span data-ttu-id="7f686-104">\[O **ZwQueryInformationProcess** pode ser alterado ou indisponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f686-104">\[**ZwQueryInformationProcess** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="7f686-105">Os aplicativos devem usar as funções alternativas listadas neste tópico.\]</span><span class="sxs-lookup"><span data-stu-id="7f686-105">Applications should use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="7f686-106">Recupera informações sobre o processo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f686-106">Retrieves information about the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f686-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f686-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="7f686-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f686-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f686-109">*ProcessHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f686-109">*ProcessHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f686-110">Um identificador para o processo para o qual as informações serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7f686-110">A handle to the process for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="7f686-111">*ProcessInformationClass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f686-111">*ProcessInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f686-112">O tipo de informações do processo a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7f686-112">The type of process information to be retrieved.</span></span> <span data-ttu-id="7f686-113">Esse parâmetro pode ser um dos valores a seguir da enumeração **PROCESSINFOCLASS** .</span><span class="sxs-lookup"><span data-stu-id="7f686-113">This parameter can be one of the following values from the **PROCESSINFOCLASS** enumeration.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f686-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7f686-114">Value</span></span></th>
<th><span data-ttu-id="7f686-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7f686-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <span data-ttu-id="7f686-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="7f686-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="7f686-117">Recupera um ponteiro para uma estrutura PEB que pode ser usada para determinar se o processo especificado está sendo depurado e um valor exclusivo usado pelo sistema para identificar o processo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f686-117">Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process.</span></span> <br/> <span data-ttu-id="7f686-118">É melhor usar as funções <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> e <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>getprocessid</strong></a> para obter essas informações.</span><span class="sxs-lookup"><span data-stu-id="7f686-118">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> functions to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <span data-ttu-id="7f686-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="7f686-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="7f686-120">Recupera um valor de <strong>DWORD_PTR</strong> que é o número da porta do depurador para o processo.</span><span class="sxs-lookup"><span data-stu-id="7f686-120">Retrieves a <strong>DWORD_PTR</strong> value that is the port number of the debugger for the process.</span></span> <span data-ttu-id="7f686-121">Um valor diferente de zero indica que o processo está sendo executado sob o controle de um depurador de anel 3.</span><span class="sxs-lookup"><span data-stu-id="7f686-121">A nonzero value indicates that the process is being run under the control of a ring 3 debugger.</span></span><br/> <span data-ttu-id="7f686-122">É melhor usar a função <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> ou <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7f686-122">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <span data-ttu-id="7f686-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span><span class="sxs-lookup"><span data-stu-id="7f686-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span></span></dl></td>
<td><span data-ttu-id="7f686-124">Determina se o processo está em execução no ambiente WOW64 (o WOW64 é o emulador x86 que permite a execução de aplicativos baseados em Win32 no Windows de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="7f686-124">Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).</span></span><br/> <span data-ttu-id="7f686-125">É melhor usar a função <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> para obter essas informações.</span><span class="sxs-lookup"><span data-stu-id="7f686-125">It is best to use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> function to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <span data-ttu-id="7f686-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span><span class="sxs-lookup"><span data-stu-id="7f686-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span></span></dl></td>
<td><span data-ttu-id="7f686-127">Recupera um valor de <strong>UNICODE_STRING</strong> que contém o nome do arquivo de imagem para o processo.</span><span class="sxs-lookup"><span data-stu-id="7f686-127">Retrieves a <strong>UNICODE_STRING</strong> value containing the name of the image file for the process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <span data-ttu-id="7f686-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span><span class="sxs-lookup"><span data-stu-id="7f686-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span></span></dl></td>
<td><span data-ttu-id="7f686-129">Recupera um valor <strong>ULONG</strong> que indica se o processo é considerado crítico.</span><span class="sxs-lookup"><span data-stu-id="7f686-129">Retrieves a <strong>ULONG</strong> value indicating whether the process is considered critical.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7f686-130">Esse valor pode ser usado a partir do Windows XP com SP3.</span><span class="sxs-lookup"><span data-stu-id="7f686-130">This value can be used starting in Windows XP with SP3.</span></span> <span data-ttu-id="7f686-131">A partir do Windows 8.1, o <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> deve ser usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7f686-131">Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> should be used instead.</span></span>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <span data-ttu-id="7f686-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span><span class="sxs-lookup"><span data-stu-id="7f686-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span></span></dl></td>
<td><span data-ttu-id="7f686-133">Recupera um valor de BYTE que indica o tipo de processo protegido e o signatário de processo protegido.</span><span class="sxs-lookup"><span data-stu-id="7f686-133">Retrieves a BYTE value indicating the type of protected process and the protected process signer.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="7f686-134">*ProcessInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7f686-134">*ProcessInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f686-135">Um ponteiro para um buffer fornecido pelo aplicativo de chamada no qual a função grava as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7f686-135">A pointer to a buffer supplied by the calling application into which the function writes the requested information.</span></span> <span data-ttu-id="7f686-136">O tamanho das informações gravadas varia dependendo do valor do parâmetro *ProcessInformationClass* :</span><span class="sxs-lookup"><span data-stu-id="7f686-136">The size of the information written varies depending on the value of the *ProcessInformationClass* parameter:</span></span>

<dl> <dt>

<span data-ttu-id="7f686-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>\_informações básicas do processo \_</span><span class="sxs-lookup"><span data-stu-id="7f686-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESS\_BASIC\_INFORMATION</span></span>
</dt> <dd>

<span data-ttu-id="7f686-138">Quando o parâmetro *ProcessInformationClass* é **ProcessBasicInformation**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações básica de processo** único com o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="7f686-138">When the *ProcessInformationClass* parameter is **ProcessBasicInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PROCESS\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

<span data-ttu-id="7f686-139">O membro **UniqueProcessId** aponta para o identificador exclusivo do sistema para esse processo.</span><span class="sxs-lookup"><span data-stu-id="7f686-139">The **UniqueProcessId** member points to the system's unique identifier for this process.</span></span> <span data-ttu-id="7f686-140">É melhor usar a função [**Getprocessid**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="7f686-140">It is best to use the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information.</span></span>

<span data-ttu-id="7f686-141">O membro **PebBaseAddress** aponta para uma estrutura [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) .</span><span class="sxs-lookup"><span data-stu-id="7f686-141">The **PebBaseAddress** member points to a [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) structure.</span></span>

<span data-ttu-id="7f686-142">Os outros membros dessa estrutura são reservados para uso interno pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7f686-142">The other members of this structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7f686-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>\_ponteiro ULONG</span><span class="sxs-lookup"><span data-stu-id="7f686-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG\_PTR</span></span>
</dt> <dd>

<span data-ttu-id="7f686-144">Quando o parâmetro *ProcessInformationClass* é **ProcessWow64Information**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para conter um **ULONG \_ PTR**.</span><span class="sxs-lookup"><span data-stu-id="7f686-144">When the *ProcessInformationClass* parameter is **ProcessWow64Information**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **ULONG\_PTR**.</span></span> <span data-ttu-id="7f686-145">Se esse valor for diferente de zero, o processo será executado em um ambiente WOW64; caso contrário, se o valor for igual a zero, o processo não será executado em um ambiente do WOW64.</span><span class="sxs-lookup"><span data-stu-id="7f686-145">If this value is nonzero, the process is running in a WOW64 environment; otherwise, if the value is equal to zero, the process is not running in a WOW64 environment.</span></span>

<span data-ttu-id="7f686-146">É melhor usar a função [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) para determinar se um processo está sendo executado no ambiente WOW64.</span><span class="sxs-lookup"><span data-stu-id="7f686-146">It is best to use the [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) function to determine whether a process is running in the WOW64 environment.</span></span>

</dd> <dt>

<span data-ttu-id="7f686-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>\_cadeia de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="7f686-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="7f686-148">Quando o parâmetro *ProcessInformationClass* é **ProcessImageFileName**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para conter uma estrutura de **cadeia de \_ caracteres Unicode** , bem como a própria cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7f686-148">When the *ProcessInformationClass* parameter is **ProcessImageFileName**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **UNICODE\_STRING** structure as well as the string itself.</span></span> <span data-ttu-id="7f686-149">A cadeia de caracteres armazenada no membro do **buffer** é o nome do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="7f686-149">The string stored in the **Buffer** member is the name of the image file.</span></span>

<span data-ttu-id="7f686-150">Se o buffer for muito pequeno, a função falhará com o \_ código de erro de comprimento incompatível das informações de status \_ \_ e o parâmetro *ReturnLength* será definido como o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="7f686-150">If the buffer is too small, the function fails with the STATUS\_INFO\_LENGTH\_MISMATCH error code and the *ReturnLength* parameter is set to the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="7f686-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span><span class="sxs-lookup"><span data-stu-id="7f686-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span></span>
</dt> <dd>

<span data-ttu-id="7f686-152">Quando o parâmetro *ProcessInformationClass* é **ProcessProtectionInformation**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para manter uma única estrutura de **PS_PROTECTION** com o seguinte layout:</span><span class="sxs-lookup"><span data-stu-id="7f686-152">When the *ProcessInformationClass* parameter is **ProcessProtectionInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PS_PROTECTION** structure having the following layout:</span></span>

``` syntax
typedef struct _PS_PROTECTION {
    union {
        UCHAR Level;
        struct {
            UCHAR Type   : 3;
            UCHAR Audit  : 1;                  // Reserved
            UCHAR Signer : 4;
        };
    };
} PS_PROTECTION, *PPS_PROTECTION;
```

<span data-ttu-id="7f686-153">Os três primeiros bits contêm o tipo de processo protegido:</span><span class="sxs-lookup"><span data-stu-id="7f686-153">The first 3 bits contain the type of protected process:</span></span>

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

<span data-ttu-id="7f686-154">Os quatro principais bits contêm o signatário de processo protegido:</span><span class="sxs-lookup"><span data-stu-id="7f686-154">The top 4 bits contain the protected process signer:</span></span>

``` syntax
typedef enum _PS_PROTECTED_SIGNER {
    PsProtectedSignerNone = 0,
    PsProtectedSignerAuthenticode,
    PsProtectedSignerCodeGen,
    PsProtectedSignerAntimalware,
    PsProtectedSignerLsa,
    PsProtectedSignerWindows,
    PsProtectedSignerWinTcb,
    PsProtectedSignerWinSystem,
    PsProtectedSignerApp,
    PsProtectedSignerMax
} PS_PROTECTED_SIGNER, *PPS_PROTECTED_SIGNER;
```

</dd> </dl> </dd> <dt>

<span data-ttu-id="7f686-155">*ProcessInformationLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f686-155">*ProcessInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f686-156">O tamanho do buffer apontado pelo parâmetro *ProcessInformation* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="7f686-156">The size of the buffer pointed to by the *ProcessInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7f686-157">*ReturnLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7f686-157">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f686-158">Um ponteiro para uma variável na qual a função retorna o tamanho das informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7f686-158">A pointer to a variable in which the function returns the size of the requested information.</span></span> <span data-ttu-id="7f686-159">Se a função foi bem-sucedida, esse é o tamanho das informações gravadas no buffer apontado pelo parâmetro *ProcessInformation* , mas se o buffer era muito pequeno, esse é o tamanho mínimo do buffer necessário para receber as informações com êxito.</span><span class="sxs-lookup"><span data-stu-id="7f686-159">If the function was successful, this is the size of the information written to the buffer pointed to by the *ProcessInformation* parameter, but if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f686-160">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f686-160">Return value</span></span>

<span data-ttu-id="7f686-161">Retorna um código de erro ou de êxito de NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="7f686-161">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="7f686-162">Os formulários e o significado dos códigos de erro NTSTATUS estão listados no arquivo de cabeçalho Ntstatus. h disponível no DDK e são descritos na documentação do DDK em Kernel-Mode guia de arquitetura/design do driver/erros de log/técnicas de programação.</span><span class="sxs-lookup"><span data-stu-id="7f686-162">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f686-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f686-163">Remarks</span></span>

<span data-ttu-id="7f686-164">A função **ZwQueryInformationProcess** e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra.</span><span class="sxs-lookup"><span data-stu-id="7f686-164">The **ZwQueryInformationProcess** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="7f686-165">Para manter a compatibilidade do seu aplicativo, é melhor usar funções públicas mencionadas na descrição do parâmetro *ProcessInformationClass* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7f686-165">To maintain the compatibility of your application, it is better to use public functions mentioned in the description of the *ProcessInformationClass* parameter instead.</span></span>

<span data-ttu-id="7f686-166">Se você usar **ZwQueryInformationProcess**, acesse a função por meio da [vinculação dinâmica em tempo de execução](../dlls/using-run-time-dynamic-linking.md).</span><span class="sxs-lookup"><span data-stu-id="7f686-166">If you do use **ZwQueryInformationProcess**, access the function through [run-time dynamic linking](../dlls/using-run-time-dynamic-linking.md).</span></span> <span data-ttu-id="7f686-167">Isso dá ao seu código uma oportunidade de responder normalmente se a função tiver sido alterada ou removida do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7f686-167">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="7f686-168">As alterações de assinatura, no entanto, podem não ser detectáveis.</span><span class="sxs-lookup"><span data-stu-id="7f686-168">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="7f686-169">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="7f686-169">This function has no associated import library.</span></span> <span data-ttu-id="7f686-170">Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="7f686-170">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f686-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f686-171">Requirements</span></span>



| <span data-ttu-id="7f686-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f686-172">Requirement</span></span> | <span data-ttu-id="7f686-173">Valor</span><span class="sxs-lookup"><span data-stu-id="7f686-173">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7f686-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f686-174">Minimum supported client</span></span><br/> | <span data-ttu-id="7f686-175">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f686-175">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7f686-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f686-176">Minimum supported server</span></span><br/> | <span data-ttu-id="7f686-177">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f686-177">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7f686-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7f686-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f686-179"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f686-179"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f686-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f686-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f686-181">**CheckRemoteDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="7f686-181">**CheckRemoteDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[<span data-ttu-id="7f686-182">**GetProcessId**</span><span class="sxs-lookup"><span data-stu-id="7f686-182">**GetProcessId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[<span data-ttu-id="7f686-183">**IsDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="7f686-183">**IsDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[<span data-ttu-id="7f686-184">**IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="7f686-184">**IsWow64Process**</span></span>](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
