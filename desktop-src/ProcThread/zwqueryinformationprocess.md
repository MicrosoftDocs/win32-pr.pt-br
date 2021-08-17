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
ms.openlocfilehash: 7972d3d2e6b98f56829680dd77c4c0a97b51679ffb2d9cfef928d4a279f6b7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792910"
---
# <a name="zwqueryinformationprocess-function"></a>Função ZwQueryInformationProcess

\[O **ZwQueryInformationProcess** pode ser alterado ou indisponível em versões futuras do Windows. Os aplicativos devem usar as funções alternativas listadas neste tópico.\]

Recupera informações sobre o processo especificado.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProcessHandle* \[ no\]
</dt> <dd>

Um identificador para o processo para o qual as informações serão recuperadas.

</dd> <dt>

*ProcessInformationClass* \[ no\]
</dt> <dd>

O tipo de informações do processo a ser recuperado. Esse parâmetro pode ser um dos valores a seguir da enumeração **PROCESSINFOCLASS** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </dl></td>
<td>Recupera um ponteiro para uma estrutura PEB que pode ser usada para determinar se o processo especificado está sendo depurado e um valor exclusivo usado pelo sistema para identificar o processo especificado. <br/> É melhor usar as funções <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> e <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>getprocessid</strong></a> para obter essas informações.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </dl></td>
<td>Recupera um valor de <strong>DWORD_PTR</strong> que é o número da porta do depurador para o processo. Um valor diferente de zero indica que o processo está sendo executado sob o controle de um depurador de anel 3.<br/> É melhor usar a função <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> ou <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </dl></td>
<td>Determina se o processo está em execução no ambiente WOW64 (o WOW64 é o emulador x86 que permite a execução de aplicativos baseados em Win32 no Windows de 64 bits).<br/> É melhor usar a função <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> para obter essas informações.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </dl></td>
<td>Recupera um valor de <strong>UNICODE_STRING</strong> que contém o nome do arquivo de imagem para o processo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </dl></td>
<td>Recupera um valor <strong>ULONG</strong> que indica se o processo é considerado crítico.<br/>
<blockquote>
[!Note]<br />
esse valor pode ser usado a partir do Windows XP com SP3. a partir do Windows 8.1, o <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> deve ser usado em vez disso.
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </dl></td>
<td>Recupera um valor de BYTE que indica o tipo de processo protegido e o signatário de processo protegido.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*ProcessInformation* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer fornecido pelo aplicativo de chamada no qual a função grava as informações solicitadas. O tamanho das informações gravadas varia dependendo do valor do parâmetro *ProcessInformationClass* :

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>\_informações básicas do processo \_
</dt> <dd>

Quando o parâmetro *ProcessInformationClass* é **ProcessBasicInformation**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para manter uma estrutura **de \_ \_ informações básica de processo** único com o seguinte layout:

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

O membro **UniqueProcessId** aponta para o identificador exclusivo do sistema para esse processo. É melhor usar a função [**Getprocessid**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) para recuperar essas informações.

O membro **PebBaseAddress** aponta para uma estrutura [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) .

Os outros membros dessa estrutura são reservados para uso interno pelo sistema operacional.

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>\_ponteiro ULONG
</dt> <dd>

Quando o parâmetro *ProcessInformationClass* é **ProcessWow64Information**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para conter um **ULONG \_ PTR**. Se esse valor for diferente de zero, o processo será executado em um ambiente WOW64; caso contrário, se o valor for igual a zero, o processo não será executado em um ambiente do WOW64.

É melhor usar a função [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) para determinar se um processo está sendo executado no ambiente WOW64.

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>\_cadeia de caracteres Unicode
</dt> <dd>

Quando o parâmetro *ProcessInformationClass* é **ProcessImageFileName**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para conter uma estrutura de **cadeia de \_ caracteres Unicode** , bem como a própria cadeia de caracteres. A cadeia de caracteres armazenada no membro do **buffer** é o nome do arquivo de imagem.

Se o buffer for muito pequeno, a função falhará com o \_ código de erro de comprimento incompatível das informações de status \_ \_ e o parâmetro *ReturnLength* será definido como o tamanho de buffer necessário.

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

Quando o parâmetro *ProcessInformationClass* é **ProcessProtectionInformation**, o buffer apontado pelo parâmetro *ProcessInformation* deve ser grande o suficiente para manter uma única estrutura de **PS_PROTECTION** com o seguinte layout:

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

Os três primeiros bits contêm o tipo de processo protegido:

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

Os quatro principais bits contêm o signatário de processo protegido:

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

*ProcessInformationLength* \[ no\]
</dt> <dd>

O tamanho do buffer apontado pelo parâmetro *ProcessInformation* , em bytes.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável na qual a função retorna o tamanho das informações solicitadas. Se a função foi bem-sucedida, esse é o tamanho das informações gravadas no buffer apontado pelo parâmetro *ProcessInformation* , mas se o buffer era muito pequeno, esse é o tamanho mínimo do buffer necessário para receber as informações com êxito.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um código de erro ou de êxito de NTSTATUS.

Os formulários e o significado dos códigos de erro NTSTATUS estão listados no arquivo de cabeçalho Ntstatus. h disponível no DDK e são descritos na documentação do DDK em Kernel-Mode guia de arquitetura/design do driver/erros de log/técnicas de programação.

## <a name="remarks"></a>Comentários

a função **ZwQueryInformationProcess** e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra. Para manter a compatibilidade do seu aplicativo, é melhor usar funções públicas mencionadas na descrição do parâmetro *ProcessInformationClass* em vez disso.

Se você usar **ZwQueryInformationProcess**, acesse a função por meio da [vinculação dinâmica em tempo de execução](../dlls/using-run-time-dynamic-linking.md). Isso dá ao seu código uma oportunidade de responder normalmente se a função tiver sido alterada ou removida do sistema operacional. As alterações de assinatura, no entanto, podem não ser detectáveis.

Esta função não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
