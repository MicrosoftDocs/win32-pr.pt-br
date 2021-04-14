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
# <a name="isolated-user-mode-ium-processes"></a><span data-ttu-id="0184e-103">Processos de modo de usuário isolado (IUM)</span><span class="sxs-lookup"><span data-stu-id="0184e-103">Isolated User Mode (IUM) Processes</span></span>

<span data-ttu-id="0184e-104">O Windows 10 introduziu um novo recurso de segurança chamado VSM (modo de segurança virtual).</span><span class="sxs-lookup"><span data-stu-id="0184e-104">Windows 10 introduced a new security feature named Virtual Secure Mode (VSM).</span></span> <span data-ttu-id="0184e-105">O VSM aproveita o hipervisor do Hyper-V e a SLAT (conversão de endereços de segundo nível) para criar um conjunto de modos chamados de VTLs (níveis de confiança virtual).</span><span class="sxs-lookup"><span data-stu-id="0184e-105">VSM leverages the Hyper-V Hypervisor and Second Level Address Translation (SLAT) to create a set of modes called Virtual Trust Levels (VTLs).</span></span> <span data-ttu-id="0184e-106">Essa nova arquitetura de software cria um limite de segurança para impedir que processos em execução em uma VTL acessem a memória de outra VTL.</span><span class="sxs-lookup"><span data-stu-id="0184e-106">This new software architecture creates a security boundary to prevent processes running in one VTL from accessing the memory of another VTL.</span></span> <span data-ttu-id="0184e-107">O benefício desse isolamento inclui mitigação adicional de explorações de kernel, ao mesmo tempo em que protege ativos como hashes de senha e chaves Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0184e-107">The benefit of this isolation includes additional mitigation from kernel exploits while protecting assets such as password hashes and Kerberos keys.</span></span>

<span data-ttu-id="0184e-108">O diagrama 1 descreve o modelo tradicional de modo kernel e o código de modo de usuário em execução na CPU anel 0 e anel 3, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0184e-108">Diagram 1 depicts the traditional model of Kernel mode and User mode code running in CPU ring 0 and ring 3, respectively.</span></span> <span data-ttu-id="0184e-109">Nesse novo modelo, o código em execução no modelo tradicional é executado em VTL0 e não pode acessar o VTL1 com privilégios mais altos, em que o kernel seguro e o modo de usuário isolado (IUM) executam o código.</span><span class="sxs-lookup"><span data-stu-id="0184e-109">In this new model, the code running in the traditional model executes in VTL0 and it cannot access the higher privileged VTL1, where the Secure Kernel and Isolated User Mode (IUM) execute code.</span></span> <span data-ttu-id="0184e-110">As VTLs são hierárquicas, o que significa que qualquer código em execução em VTL1 é mais privilegiado do que o código em execução no VTL0.</span><span class="sxs-lookup"><span data-stu-id="0184e-110">The VTLs are hierarchal meaning any code running in VTL1 is more privileged than code running in VTL0.</span></span>

<span data-ttu-id="0184e-111">O isolamento de VTL é criado pelo hipervisor Hyper-V que atribui memória no momento da inicialização usando a SLAT (conversão de endereços de segundo nível).</span><span class="sxs-lookup"><span data-stu-id="0184e-111">The VTL isolation is created by the Hyper-V Hypervisor which assigns memory at boot time using Second Level Address Translation (SLAT).</span></span> <span data-ttu-id="0184e-112">Ele continua dinamicamente à medida que o sistema é executado, protegendo a memória o kernel seguro especifica a necessidade de proteção do VTL0 porque ele será usado para conter segredos.</span><span class="sxs-lookup"><span data-stu-id="0184e-112">It continues this dynamically as the system runs, protecting memory the Secure Kernel specifies needing protection from VTL0 because it will be used to contain secrets.</span></span> <span data-ttu-id="0184e-113">À medida que blocos separados de memória são alocados para as duas VTLs, um ambiente de tempo de execução seguro é criado para VTL1 atribuindo blocos de memória exclusivos a VTL1 e VTL0 com as permissões de acesso apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0184e-113">As separate blocks of memory are allocated for the two VTLs, a secure runtime environment is created for VTL1 by assigning exclusive memory blocks to VTL1 and VTL0 with the appropriate access permissions.</span></span>

<span data-ttu-id="0184e-114">**Diagrama 1-arquitetura IUM**</span><span class="sxs-lookup"><span data-stu-id="0184e-114">**Diagram 1 - IUM Architecture**</span></span>

![diagrama 1-arquitetura ium](images/uim-architecture.png)

## <a name="trustlets"></a><span data-ttu-id="0184e-116">Trustlets</span><span class="sxs-lookup"><span data-stu-id="0184e-116">Trustlets</span></span>

<span data-ttu-id="0184e-117">Trustlets (também conhecido como processos confiáveis, processos seguros ou processos de IUM) são programas em execução como processos de IUM no VSM.</span><span class="sxs-lookup"><span data-stu-id="0184e-117">Trustlets (also known as trusted processes, secure processes, or IUM processes) are programs running as IUM processes in VSM.</span></span> <span data-ttu-id="0184e-118">Eles concluem chamadas do sistema por meio de Marshalling para o kernel do Windows em execução no VTL0 Ring 0.</span><span class="sxs-lookup"><span data-stu-id="0184e-118">They complete system calls by marshalling them over to the Windows kernel running in VTL0 ring 0.</span></span> <span data-ttu-id="0184e-119">O VSM cria um ambiente de execução pequeno que inclui o pequeno kernel seguro em execução no VTL1 (isolado do kernel e dos drivers em execução no VTL0).</span><span class="sxs-lookup"><span data-stu-id="0184e-119">VSM creates a small execution environment that includes the small Secure Kernel executing in VTL1 (isolated from the kernel and drivers running in VTL0).</span></span> <span data-ttu-id="0184e-120">O benefício de segurança claro é o isolamento das páginas de modo de usuário trustlet no VTL1 de drivers em execução no kernel VTL0.</span><span class="sxs-lookup"><span data-stu-id="0184e-120">The clear security benefit is isolation of trustlet user mode pages in VTL1 from drivers running in the VTL0 kernel.</span></span> <span data-ttu-id="0184e-121">Mesmo que o modo kernel de VTL0 seja comprometido por malware, ele não terá acesso às páginas de processo do IUM.</span><span class="sxs-lookup"><span data-stu-id="0184e-121">Even if kernel mode of VTL0 is compromised by malware, it will not have access to the IUM process pages.</span></span>

<span data-ttu-id="0184e-122">Com o VSM habilitado, o ambiente da autoridade de segurança local (LSASs) é executado como um trustlet.</span><span class="sxs-lookup"><span data-stu-id="0184e-122">With VSM enabled, the Local Security Authority (LSASS) environment runs as a trustlet.</span></span> <span data-ttu-id="0184e-123">O LSASs gerencia a diretiva do sistema local, a autenticação do usuário e a auditoria ao lidar com dados de segurança confidenciais, como hashes de senha e chaves Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0184e-123">LSASS manages the local system policy, user authentication, and auditing while handling sensitive security data such as password hashes and Kerberos keys.</span></span> <span data-ttu-id="0184e-124">Para aproveitar os benefícios de segurança do VSM, um trustlet chamado LSAISO.exe (LSA isolado) é executado no VTL1 e se comunica com LSASS.exe em execução no VTL0 por meio de um canal RPC.</span><span class="sxs-lookup"><span data-stu-id="0184e-124">To leverage the security benefits of VSM, a trustlet named LSAISO.exe (LSA Isolated) runs in VTL1 and communicates with LSASS.exe running in VTL0 through an RPC channel.</span></span> <span data-ttu-id="0184e-125">Os segredos do LSAISO são criptografados antes de serem enviados para o LSASs em execução no modo do VSM normal e as páginas de LSAISO são protegidas do código mal-intencionado em execução no VTL0.</span><span class="sxs-lookup"><span data-stu-id="0184e-125">The LSAISO secrets are encrypted before sending them over to LSASS running in VSM Normal Mode and the pages of LSAISO are protected from malicious code running in VTL0.</span></span>

<span data-ttu-id="0184e-126">**Diagrama 2 – design de Trustlet do LSASs**</span><span class="sxs-lookup"><span data-stu-id="0184e-126">**Diagram 2 – LSASS Trustlet Design**</span></span>

![<span data-ttu-id="0184e-127">diagrama 2 – design de trustlet do Lsass</span><span class="sxs-lookup"><span data-stu-id="0184e-127">diagram 2 – lsass trustlet design</span></span> ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a><span data-ttu-id="0184e-128">Implicações de modo de usuário isolado (IUM)</span><span class="sxs-lookup"><span data-stu-id="0184e-128">Isolated User Mode (IUM) Implications</span></span>

<span data-ttu-id="0184e-129">Não é possível anexar a um processo IUM, inibindo a capacidade de depurar o código VTL1.</span><span class="sxs-lookup"><span data-stu-id="0184e-129">It is not possible to attach to an IUM process, inhibiting the ability to debug VTL1 code.</span></span> <span data-ttu-id="0184e-130">Isso inclui a depuração de morte de despejos de memória e a anexação das ferramentas de depuração para depuração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0184e-130">This includes post mortem debugging of memory dumps and attaching the Debugging Tools for live debugging.</span></span> <span data-ttu-id="0184e-131">Ele também inclui tentativas por contas privilegiadas ou drivers de kernel para carregar uma DLL em um processo IUM, injetar um thread ou fornecer uma APC de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="0184e-131">It also includes attempts by privileged accounts or kernel drivers to load a DLL into an IUM process, to inject a thread, or deliver a user-mode APC.</span></span> <span data-ttu-id="0184e-132">Essas tentativas podem resultar na desestabilização de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="0184e-132">Such attempts may result in destabilization of the entire system.</span></span> <span data-ttu-id="0184e-133">As APIs do Windows que comprometeriam a segurança de um Trustlet podem falhar de maneiras inesperadas.</span><span class="sxs-lookup"><span data-stu-id="0184e-133">Windows APIs that would compromise the security of a Trustlet may fail in unexpected ways.</span></span> <span data-ttu-id="0184e-134">Por exemplo, carregar uma DLL em um Trustlet a tornará disponível em VTL0, mas não VTL1.</span><span class="sxs-lookup"><span data-stu-id="0184e-134">For example, loading a DLL into a Trustlet will make it available in VTL0 but not VTL1.</span></span> <span data-ttu-id="0184e-135">QueueUserApc poderá falhar silenciosamente se o thread-alvo estiver em um Trustlet.</span><span class="sxs-lookup"><span data-stu-id="0184e-135">QueueUserApc may silently fail if the target thread is in a Trustlet.</span></span> <span data-ttu-id="0184e-136">Outras APIs, como CreateRemoteThread, VirtualAllocEx e Read/WriteProcessMemory também não funcionarão conforme o esperado quando usadas em relação a Trustlets.</span><span class="sxs-lookup"><span data-stu-id="0184e-136">Other APIs, such as CreateRemoteThread, VirtualAllocEx, and Read/WriteProcessMemory will also not work as expected when used against Trustlets.</span></span>

<span data-ttu-id="0184e-137">Use o código de exemplo abaixo para impedir a chamada de qualquer função que tente anexar ou injetar código em um processo IUM.</span><span class="sxs-lookup"><span data-stu-id="0184e-137">Use the sample code below to prevent calling any functions which attempt to attach or inject code into an IUM process.</span></span> <span data-ttu-id="0184e-138">Isso inclui drivers de kernel que enfileiram APCs para execução de código em um trustlet.</span><span class="sxs-lookup"><span data-stu-id="0184e-138">This includes kernel drivers that queue APCs for execution of code in a trustlet.</span></span>

## <a name="remarks"></a><span data-ttu-id="0184e-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="0184e-139">Remarks</span></span>

<span data-ttu-id="0184e-140">Se o status de retorno de IsSecureProcess for Success, examine o \_ parâmetro SecureProcess out \_ para determinar se o processo é um processo ium.</span><span class="sxs-lookup"><span data-stu-id="0184e-140">If the return status of IsSecureProcess is success, examine the SecureProcess \_Out\_ parameter to determine if the process is an IUM process.</span></span> <span data-ttu-id="0184e-141">Os processos IUM são marcados pelo sistema para serem "processos seguros".</span><span class="sxs-lookup"><span data-stu-id="0184e-141">IUM processes are marked by the system to be “Secure Processes”.</span></span> <span data-ttu-id="0184e-142">Um resultado booleano de TRUE significa que o processo de destino é do tipo IUM.</span><span class="sxs-lookup"><span data-stu-id="0184e-142">A Boolean result of TRUE means the target process is of type IUM.</span></span>


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



<span data-ttu-id="0184e-143">O WDK para Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", contém a definição necessária da estrutura de \_ informações básicas estendida do processo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0184e-143">The WDK for Windows 10, “Windows Driver Kit - Windows 10.0.15063.0”, contains the required definition of the PROCESS\_EXTENDED\_BASIC\_INFORMATION structure.</span></span> <span data-ttu-id="0184e-144">A versão atualizada da estrutura é definida em ntddk. h com o novo campo IsSecureProcess.</span><span class="sxs-lookup"><span data-stu-id="0184e-144">The updated version of the structure is defined in ntddk.h with the new IsSecureProcess field.</span></span>


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



 

 



