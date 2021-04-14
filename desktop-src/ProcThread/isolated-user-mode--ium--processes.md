---
description: O Windows 10 introduziu um novo recurso de segurança chamado VSM (modo de segurança virtual).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Processos de modo de usuário isolado (IUM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a176421174a58abe4ab595bb37ab75434edade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565899"
---
# <a name="isolated-user-mode-ium-processes"></a>Processos de modo de usuário isolado (IUM)

O Windows 10 introduziu um novo recurso de segurança chamado VSM (modo de segurança virtual). O VSM aproveita o hipervisor do Hyper-V e a SLAT (conversão de endereços de segundo nível) para criar um conjunto de modos chamados de VTLs (níveis de confiança virtual). Essa nova arquitetura de software cria um limite de segurança para impedir que processos em execução em uma VTL acessem a memória de outra VTL. O benefício desse isolamento inclui mitigação adicional de explorações de kernel, ao mesmo tempo em que protege ativos como hashes de senha e chaves Kerberos.

O diagrama 1 descreve o modelo tradicional de modo kernel e o código de modo de usuário em execução na CPU anel 0 e anel 3, respectivamente. Nesse novo modelo, o código em execução no modelo tradicional é executado em VTL0 e não pode acessar o VTL1 com privilégios mais altos, em que o kernel seguro e o modo de usuário isolado (IUM) executam o código. As VTLs são hierárquicas, o que significa que qualquer código em execução em VTL1 é mais privilegiado do que o código em execução no VTL0.

O isolamento de VTL é criado pelo hipervisor Hyper-V que atribui memória no momento da inicialização usando a SLAT (conversão de endereços de segundo nível). Ele continua dinamicamente à medida que o sistema é executado, protegendo a memória o kernel seguro especifica a necessidade de proteção do VTL0 porque ele será usado para conter segredos. À medida que blocos separados de memória são alocados para as duas VTLs, um ambiente de tempo de execução seguro é criado para VTL1 atribuindo blocos de memória exclusivos a VTL1 e VTL0 com as permissões de acesso apropriadas.

**Diagrama 1-arquitetura IUM**

![diagrama 1-arquitetura ium](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Trustlets (também conhecido como processos confiáveis, processos seguros ou processos de IUM) são programas em execução como processos de IUM no VSM. Eles concluem chamadas do sistema por meio de Marshalling para o kernel do Windows em execução no VTL0 Ring 0. O VSM cria um ambiente de execução pequeno que inclui o pequeno kernel seguro em execução no VTL1 (isolado do kernel e dos drivers em execução no VTL0). O benefício de segurança claro é o isolamento das páginas de modo de usuário trustlet no VTL1 de drivers em execução no kernel VTL0. Mesmo que o modo kernel de VTL0 seja comprometido por malware, ele não terá acesso às páginas de processo do IUM.

Com o VSM habilitado, o ambiente da autoridade de segurança local (LSASs) é executado como um trustlet. O LSASs gerencia a diretiva do sistema local, a autenticação do usuário e a auditoria ao lidar com dados de segurança confidenciais, como hashes de senha e chaves Kerberos. Para aproveitar os benefícios de segurança do VSM, um trustlet chamado LSAISO.exe (LSA isolado) é executado no VTL1 e se comunica com LSASS.exe em execução no VTL0 por meio de um canal RPC. Os segredos do LSAISO são criptografados antes de serem enviados para o LSASs em execução no modo do VSM normal e as páginas de LSAISO são protegidas do código mal-intencionado em execução no VTL0.

**Diagrama 2 – design de Trustlet do LSASs**

![diagrama 2 – design de trustlet do Lsass ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Implicações de modo de usuário isolado (IUM)

Não é possível anexar a um processo IUM, inibindo a capacidade de depurar o código VTL1. Isso inclui a depuração de morte de despejos de memória e a anexação das ferramentas de depuração para depuração dinâmica. Ele também inclui tentativas por contas privilegiadas ou drivers de kernel para carregar uma DLL em um processo IUM, injetar um thread ou fornecer uma APC de modo de usuário. Essas tentativas podem resultar na desestabilização de todo o sistema. As APIs do Windows que comprometeriam a segurança de um Trustlet podem falhar de maneiras inesperadas. Por exemplo, carregar uma DLL em um Trustlet a tornará disponível em VTL0, mas não VTL1. QueueUserApc poderá falhar silenciosamente se o thread-alvo estiver em um Trustlet. Outras APIs, como CreateRemoteThread, VirtualAllocEx e Read/WriteProcessMemory também não funcionarão conforme o esperado quando usadas em relação a Trustlets.

Use o código de exemplo abaixo para impedir a chamada de qualquer função que tente anexar ou injetar código em um processo IUM. Isso inclui drivers de kernel que enfileiram APCs para execução de código em um trustlet.

## <a name="remarks"></a>Comentários

Se o status de retorno de IsSecureProcess for Success, examine o \_ parâmetro SecureProcess out \_ para determinar se o processo é um processo ium. Os processos IUM são marcados pelo sistema para serem "processos seguros". Um resultado booleano de TRUE significa que o processo de destino é do tipo IUM.


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



O WDK para Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", contém a definição necessária da estrutura de \_ informações básicas estendida do processo \_ \_ . A versão atualizada da estrutura é definida em ntddk. h com o novo campo IsSecureProcess.


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



 

 



