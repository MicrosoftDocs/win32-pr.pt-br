---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: O FRS (serviço de replicação de arquivo) foi preterido no Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764226"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="8698e-103">O FRS (serviço de replicação de arquivo) foi preterido no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8698e-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="8698e-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="8698e-104">Platform</span></span>

 <span data-ttu-id="8698e-105">**Servidores-** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8698e-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="8698e-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="8698e-106">Feature Impact</span></span>

 <span data-ttu-id="8698e-107">**Severidade-** Elevada</span><span class="sxs-lookup"><span data-stu-id="8698e-107">**Severity -** High</span></span>  
<span data-ttu-id="8698e-108">**Frequência-** Elevada</span><span class="sxs-lookup"><span data-stu-id="8698e-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="8698e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8698e-109">Description</span></span>

<span data-ttu-id="8698e-110">No Windows Server 2008 R2, o FRS (serviço de replicação de arquivo) não pode ser usado para replicar pastas Sistema de Arquivos Distribuído (DFS) ou dados personalizados (não SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="8698e-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="8698e-111">Um controlador de domínio do Windows Server 2008 R2 ainda pode usar o FRS para replicar o conteúdo do compartilhamento SYSVOL em um domínio que usa o FRS para replicar o compartilhamento SYSVOL entre controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="8698e-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="8698e-112">No entanto, os servidores Windows Server 2008 R2 não podem usar o FRS para replicar o conteúdo de qualquer conjunto de réplicas além do compartilhamento de SYSVOL.</span><span class="sxs-lookup"><span data-stu-id="8698e-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="8698e-113">O serviço de Replicação do DFS é uma substituição para o FRS e pode ser usado para replicar o conteúdo do compartilhamento SYSVOL, pastas DFS, bem como outros dados personalizados (não SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="8698e-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="8698e-114">Migre todos os conjuntos de réplicas do FRS não SYSVOL para Replicação do DFS.</span><span class="sxs-lookup"><span data-stu-id="8698e-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="8698e-115">Também é altamente recomendável que você migre a replicação do compartilhamento SYSVOL do FRS para o Replicação do DFS porque Replicação do DFS é mais robusto, escalonável e tem melhor desempenho de replicação do que o FRS.</span><span class="sxs-lookup"><span data-stu-id="8698e-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8698e-116">Manifestação</span><span class="sxs-lookup"><span data-stu-id="8698e-116">Manifestation</span></span>

<span data-ttu-id="8698e-117">A replicação FRS de dados personalizados interromperá a irreversíveis na atualização in-loco.</span><span class="sxs-lookup"><span data-stu-id="8698e-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="8698e-118">A única maneira de se recuperar dessa situação seria reinstalar um sistema operacional mais antigo no servidor e reinicializar a replicação do FRS.</span><span class="sxs-lookup"><span data-stu-id="8698e-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="8698e-119">Os servidores que foram atualizados para o Windows Server 2008 R2 não têm permissão para participar de grupos de replicação do FRS existentes.</span><span class="sxs-lookup"><span data-stu-id="8698e-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="8698e-120">Mitigação do impacto</span><span class="sxs-lookup"><span data-stu-id="8698e-120">Mitigation of Impact</span></span>

<span data-ttu-id="8698e-121">Para evitar problemas que possam ocorrer como resultado dessas alterações, migre conjuntos de replicação do FRS personalizados para Replicação do DFS.</span><span class="sxs-lookup"><span data-stu-id="8698e-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="8698e-122">O serviço de Replicação do DFS tem muitos benefícios sobre o FRS, incluindo ferramentas de gerenciamento aprimoradas, melhor desempenho e gerenciamento delegado.</span><span class="sxs-lookup"><span data-stu-id="8698e-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="8698e-123">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="8698e-123">Links to Other Resources</span></span>

-   <span data-ttu-id="8698e-124">[Visão geral do FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="8698e-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="8698e-125">Replicação do sistema de arquivos distribuído: perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="8698e-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="8698e-126">Guia de Migração de Replicação SYSVOL: Replicação FRS para DFS</span><span class="sxs-lookup"><span data-stu-id="8698e-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
