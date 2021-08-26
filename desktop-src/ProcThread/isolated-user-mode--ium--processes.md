---
description: Windows 10 um novo recurso de segurança chamado VSM (Modo de Segurança Virtual).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Processos de IUM (modo de usuário isolado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982d9924f60d02a74aa7237e5c3bb16e787f1d3a0cc07e9693e9cd47335cedc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032527"
---
# <a name="isolated-user-mode-ium-processes"></a>Processos de IUM (modo de usuário isolado)

Windows 10 um novo recurso de segurança chamado VSM (Modo de Segurança Virtual). O VSM aproveita o Hipervisor do Hyper-V e a SLAT (Conversão de Endereços de Segundo Nível) para criar um conjunto de modos chamados VTLs (Níveis de Confiança Virtual). Essa nova arquitetura de software cria um limite de segurança para impedir que processos em execução em uma VTL acessem a memória de outra VTL. O benefício desse isolamento inclui mitigação adicional de explorações de kernel enquanto protege ativos, como hashes de senha e chaves Kerberos.

O Diagrama 1 ilustra o modelo tradicional do modo kernel e o código do modo de usuário em execução no anel de CPU 0 e no anel 3, respectivamente. Nesse novo modelo, o código em execução no modelo tradicional é executado em VTL0 e não pode acessar a VTL1 com privilégios mais altos, em que o kernel seguro e o modo de usuário isolado (IUM) executam código. As VTLs são hierarquias, o que significa que qualquer código em execução na VTL1 é mais privilegiado do que o código em execução na VTL0.

O isolamento de VTL é criado pelo Hipervisor do Hyper-V, que atribui memória no momento da inicialização usando a SLAT (Conversão de Endereços de Segundo Nível). Ele continua isso dinamicamente à medida que o sistema é executado, protegendo a memória que o Kernel Seguro especifica que precisa de proteção contra VTL0 porque ele será usado para conter segredos. À medida que blocos separados de memória são alocados para as duas VTLs, um ambiente de runtime seguro é criado para VTL1 atribuindo blocos de memória exclusivos a VTL1 e VTL0 com as permissões de acesso apropriadas.

**Diagrama 1 – Arquitetura de IUM**

![diagrama 1 – arquitetura de ium](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Os trustlets (também conhecidos como processos confiáveis, processos seguros ou processos IUM) são programas em execução como processos IUM no VSM. Eles concluem chamadas do sistema fazendo marshaling delas para o kernel Windows em execução no anel VTL0 0. O VSM cria um ambiente de execução pequeno que inclui o pequeno Kernel Seguro em execução no VTL1 (isolado do kernel e dos drivers em execução no VTL0). O benefício claro de segurança é o isolamento de páginas de modo de usuário trustlet na VTL1 de drivers em execução no kernel VTL0. Mesmo que o modo kernel do VTL0 seja comprometido por malware, ele não terá acesso às páginas de processo do IUM.

Com o VSM habilitado, o ambiente LSASS (Autoridade de Segurança Local) é executado como um trustlet. O LSASS gerencia a política do sistema local, a autenticação de usuário e a auditoria ao lidar com dados confidenciais de segurança, como hashes de senha e chaves Kerberos. Para aproveitar os benefícios de segurança do VSM, um trustlet chamado LSAISO.exe (LSA Isolado) é executado na VTL1 e se comunica com LSASS.exe em execução na VTL0 por meio de um canal RPC. Os segredos LSAISO são criptografados antes de enviá-los ao LSASS em execução no Modo Normal do VSM e as páginas de LSAISO são protegidas contra código mal-intencionado em execução na VTL0.

**Diagrama 2 – Design de trustlet LSASS**

![diagrama 2 – design de trustlet lsass ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Implicações do IUM (modo de usuário isolado)

Não é possível anexar a um processo de IUM, inibindo a capacidade de depurar o código VTL1. Isso inclui a depuração pós-mortem de despejos de memória e a anexação das Ferramentas de Depuração para depuração ao vivo. Ele também inclui tentativas por contas privilegiadas ou drivers de kernel para carregar uma DLL em um processo de IUM, injetar um thread ou entregar um APC no modo de usuário. Essas tentativas podem resultar na desestabilização de todo o sistema. Windows As APIs que comprometeriam a segurança de um Trustlet podem falhar de maneiras inesperadas. Por exemplo, carregar uma DLL em um Trustlet o disponibiliza em VTL0, mas não VTL1. QueueUserApc poderá falhar silenciosamente se o thread de destino estiver em um Trustlet. Outras APIs, como CreateRemoteThread, VirtualAllocEx e Read/WriteProcessMemory, também não funcionarão conforme o esperado quando usados em Trustlets.

Use o código de exemplo abaixo para evitar chamar funções que tentam anexar ou injetar código em um processo IUM. Isso inclui drivers de kernel que enfileiram APCs para execução de código em um trustlet.

## <a name="remarks"></a>Comentários

Se o status de retorno de IsSecureProcess for bem-sucedido, examine o parâmetro SecureProcess Out para determinar se o \_ processo é um processo \_ IUM. Os processos de IUM são marcados pelo sistema como "Processos Seguros". Um resultado booliana de TRUE significa que o processo de destino é do tipo IUM.


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



O WDK para Windows 10, "kit de driver Windows – Windows 10.0.15063.0", contém a definição necessária da estrutura PROCESS \_ EXTENDED \_ BASIC \_ INFORMATION. A versão atualizada da estrutura é definida em ntddk.h com o novo campo IsSecureProcess.


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 



