---
title: Usando TBS
description: Cada comando enviado ao TBS é associado a uma entidade específica. Isso é feito criando um ou mais contextos para uma entidade, que são então associados a cada comando subsequente enviado por essa entidade.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TBS de serviços base do TPM, exemplos
- TBS de serviços base do TPM, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916321"
---
# <a name="using-tbs"></a><span data-ttu-id="64dd5-106">Usando TBS</span><span class="sxs-lookup"><span data-stu-id="64dd5-106">Using TBS</span></span>

<span data-ttu-id="64dd5-107">O recurso de serviços base do TPM é dividido em quatro áreas funcionais:</span><span class="sxs-lookup"><span data-stu-id="64dd5-107">The TPM Base Services feature is divided into four functional areas:</span></span>

-   [<span data-ttu-id="64dd5-108">Virtualização de recursos</span><span class="sxs-lookup"><span data-stu-id="64dd5-108">Resource Virtualization</span></span>](resource-virtualization.md)
-   [<span data-ttu-id="64dd5-109">Agendamento de comandos</span><span class="sxs-lookup"><span data-stu-id="64dd5-109">Command Scheduling</span></span>](command-scheduling.md)
-   [<span data-ttu-id="64dd5-110">Gerenciamento de Energia</span><span class="sxs-lookup"><span data-stu-id="64dd5-110">Power Management</span></span>](power-management.md)
-   [<span data-ttu-id="64dd5-111">Bloqueio de comando</span><span class="sxs-lookup"><span data-stu-id="64dd5-111">Command Blocking</span></span>](command-blocking.md)

<span data-ttu-id="64dd5-112">Para garantir que entidades diferentes não possam acessar os recursos uns dos outros, cada comando enviado ao TBS é associado a uma entidade específica.</span><span class="sxs-lookup"><span data-stu-id="64dd5-112">To ensure that different entities cannot access each other's resources, each command submitted to the TBS is associated with a specific entity.</span></span> <span data-ttu-id="64dd5-113">Isso é feito criando um ou mais contextos para uma entidade, que são então associados a cada comando subsequente enviado por essa entidade.</span><span class="sxs-lookup"><span data-stu-id="64dd5-113">This is accomplished by creating one or more contexts for an entity, which are then associated with each subsequent command submitted by that entity.</span></span> <span data-ttu-id="64dd5-114">Cada comando inclui um objeto de contexto, que permite que o TBS execute comandos do TPM no contexto apropriado.</span><span class="sxs-lookup"><span data-stu-id="64dd5-114">Each command includes a context object, which allows the TBS to execute TPM commands under the appropriate context.</span></span> <span data-ttu-id="64dd5-115">Todos os objetos criados por comandos são liberados do TPM quando o contexto é fechado.</span><span class="sxs-lookup"><span data-stu-id="64dd5-115">All objects created by commands are flushed from the TPM when the context is closed.</span></span>

<span data-ttu-id="64dd5-116">Uma entidade cria o contexto antes de ele primeiro acessar o TBS e mantém o contexto até que ele termine de executar acessos TBS.</span><span class="sxs-lookup"><span data-stu-id="64dd5-116">An entity creates the context before it first accesses the TBS and maintains the context until it is finished performing TBS accesses.</span></span> <span data-ttu-id="64dd5-117">Por exemplo, no caso de um TSS, o recurso de TCS (serviços principais do TCG) do TSS criaria um contexto TBS quando ele for iniciado, e ele manterá esse contexto ativo até ser desligado.</span><span class="sxs-lookup"><span data-stu-id="64dd5-117">For example, in the case of a TSS, the TCG core services (TCS) feature of the TSS would create a TBS context when it starts up, and it would keep that context active until it shuts down.</span></span>

<span data-ttu-id="64dd5-118">Para o Windows Server 2008 e o Windows Vista, o TBS restringe o acesso à API TBS para as contas de administradores, NT e LocalService da autoridade \\ NT \\ .</span><span class="sxs-lookup"><span data-stu-id="64dd5-118">For Windows Server 2008 and Windows Vista, the TBS restricts access to the TBS API to the Administrators, NT AUTHORITY\\LocalService, and NT AUTHORITY\\NetworkService accounts.</span></span> <span data-ttu-id="64dd5-119">Por padrão, essas contas são as únicas que podem se conectar a TBS e criar contextos.</span><span class="sxs-lookup"><span data-stu-id="64dd5-119">By default, these accounts are the only ones that can connect to TBS and create contexts.</span></span> <span data-ttu-id="64dd5-120">As restrições de acesso podem ser modificadas com a criação de um **acesso à** chave do registro com um nome de valor do registro de cadeia de caracteres (**reg \_ sz**) **SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="64dd5-120">Access restrictions can be modified by creating a registry key **Access** with a string (**REG\_SZ**) registry value name **SecurityDescriptor**</span></span> <dl> <dt>

<span data-ttu-id="64dd5-121">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="64dd5-121">Data type</span></span>
</dt> <dd><span data-ttu-id="64dd5-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="64dd5-122">REG_SZ</span></span></dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

<span data-ttu-id="64dd5-123">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="64dd5-123">Example:</span></span>

<span data-ttu-id="64dd5-124">**O:BAG: INADEQUADO: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**</span><span class="sxs-lookup"><span data-stu-id="64dd5-124">**O:BAG:BAD:(A;;0x00000001;;;BA)(A;;0x00000001;;;NS)(A;;0x00000001;;;LS)**</span></span>

<span data-ttu-id="64dd5-125">Por padrão, o número máximo de contextos com suporte no TBS é 25.</span><span class="sxs-lookup"><span data-stu-id="64dd5-125">By default, the maximum number of contexts supported by the TBS is 25.</span></span> <span data-ttu-id="64dd5-126">Esse número pode ser alterado criando ou modificando um valor de registro **DWORD** chamado **MaxContexts** em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**.</span><span class="sxs-lookup"><span data-stu-id="64dd5-126">This number can be altered by creating or modifying a **DWORD** registry value named **MaxContexts** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="64dd5-127">O uso de contexto TBS em tempo real pode ser observado usando a ferramenta Monitor de desempenho para controlar o número de contextos TBS.</span><span class="sxs-lookup"><span data-stu-id="64dd5-127">Real-time TBS context usage can be observed by using the performance monitor tool to track the number of TBS contexts.</span></span>

<span data-ttu-id="64dd5-128">Para o Windows 8, o Windows Server 2012 e posterior, o TBS permite o acesso a usuários e administradores padrão.</span><span class="sxs-lookup"><span data-stu-id="64dd5-128">For Windows 8, Windows Server 2012 and later, the TBS allows access to standard users and administrators.</span></span> <span data-ttu-id="64dd5-129">As chaves do registro **SecurityDescriptor** e **MaxContexts** se tornaram obsoletas.</span><span class="sxs-lookup"><span data-stu-id="64dd5-129">The **SecurityDescriptor** and **MaxContexts** registry keys became obsolete.</span></span> <span data-ttu-id="64dd5-130">Para o Windows 8, o Windows Server 2012 e posterior, o TBS restringe o acesso a certos comandos usando o bloqueio de comando.</span><span class="sxs-lookup"><span data-stu-id="64dd5-130">For Windows 8, Windows Server 2012 and later, the TBS restricts access to certain commands using Command Blocking.</span></span>

<span data-ttu-id="64dd5-131">Para o Windows 10, versão 1607, o TBS permite o acesso de aplicativos do AppContainer.</span><span class="sxs-lookup"><span data-stu-id="64dd5-131">For Windows 10, version 1607, the TBS allows access from AppContainer applications.</span></span> <span data-ttu-id="64dd5-132">Para cada versão do TPM, as chaves **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands** foram adicionadas com as listas correspondentes de comandos do TPM bloqueados e permitidos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="64dd5-132">For each TPM version, the keys **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands** have been added with the matching lists of blocked and allowed TPM commands, respectively.</span></span>

<span data-ttu-id="64dd5-133">Para o Windows 10, versão 1803, as chaves do registro em **AllowedW8AppContainerCommands** não são mais suportadas.</span><span class="sxs-lookup"><span data-stu-id="64dd5-133">For Windows 10, version 1803, the registry keys under **AllowedW8AppContainerCommands** are no longer supported.</span></span>

 

 




