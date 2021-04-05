---
title: Sistema de arquivos resiliente
description: Sistema de arquivos resiliente
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104008543"
---
# <a name="resilient-file-system"></a><span data-ttu-id="e6fc9-103">Sistema de arquivos resiliente</span><span class="sxs-lookup"><span data-stu-id="e6fc9-103">Resilient file system</span></span>

## <a name="platform"></a><span data-ttu-id="e6fc9-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="e6fc9-104">Platform</span></span>

<span data-ttu-id="e6fc9-105">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6fc9-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="e6fc9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6fc9-106">Description</span></span>

<span data-ttu-id="e6fc9-107">O ReFS (sistema de arquivos resiliente) é um novo sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-107">Resilient File System (ReFS) is a new local file system.</span></span> <span data-ttu-id="e6fc9-108">Ela maximiza a disponibilidade dos dados, apesar dos erros que, historicamente, causam perda de dados ou tempo de inatividade.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-108">It maximizes data availability, despite errors that would historically cause data loss or downtime.</span></span> <span data-ttu-id="e6fc9-109">A integridade dos dados garante que os dados críticos dos negócios sejam protegidos contra erros e disponíveis quando necessário.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-109">Data integrity ensures that business critical data is protected from errors and available when needed.</span></span> <span data-ttu-id="e6fc9-110">Sua arquitetura foi projetada para fornecer escalabilidade e desempenho em uma época de crescimento constante de tamanhos de conjuntos de dados e cargas de trabalho dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-110">Its architecture is designed to provide scalability and performance in an era of constantly growing data set sizes and dynamic workloads.</span></span>

<span data-ttu-id="e6fc9-111">Os principais recursos do ReFS são:</span><span class="sxs-lookup"><span data-stu-id="e6fc9-111">The key features of ReFS are:</span></span>

-   <span data-ttu-id="e6fc9-112">**Integridade**: ReFS armazena dados para que eles sejam protegidos de muitos dos erros comuns que podem causar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-112">**Integrity**: ReFS stores data so that it is protected from many of the common errors that can cause data loss.</span></span> <span data-ttu-id="e6fc9-113">Os metadados do sistema de arquivos são sempre protegidos.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-113">File system metadata is always protected.</span></span> <span data-ttu-id="e6fc9-114">Opcionalmente, os dados do usuário podem ser protegidos em uma base por volume, por diretório ou por arquivo.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-114">Optionally, user data can be protected on a per-volume, per-directory, or per-file basis.</span></span> <span data-ttu-id="e6fc9-115">Se ocorrer corrupção, o ReFS poderá detectar e, quando configurado com espaços de armazenamento, corrigir automaticamente o dano.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-115">If corruption occurs, ReFS can detect and, when configured with Storage Spaces, automatically correct the corruption.</span></span> <span data-ttu-id="e6fc9-116">No caso de um erro do sistema, o ReFS foi projetado para se recuperar rapidamente desse erro, sem perda de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-116">In the event of a system error, ReFS is designed to recover from that error rapidly, with no loss of user data.</span></span>
-   <span data-ttu-id="e6fc9-117">**Disponibilidade**: ReFS foi projetado para priorizar a disponibilidade de dados.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-117">**Availability**: ReFS is designed to prioritize the availability of data.</span></span> <span data-ttu-id="e6fc9-118">Com ReFS, se ocorrer corrupção e não puder ser reparado automaticamente, o processo de resgate online será localizado na área de corrupção, não exigindo nenhum tempo de inatividade de volume.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-118">With ReFS, if corruption occurs, and it cannot be repaired automatically, the online salvage process is localized to the area of corruption, requiring no volume down-time.</span></span> <span data-ttu-id="e6fc9-119">Em resumo, se a corrupção ocorrer, ReFS permanecerá online.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-119">In short, if corruption occurs, ReFS will stay online.</span></span>
-   <span data-ttu-id="e6fc9-120">**Escalabilidade**: ReFS foi projetado para os tamanhos de conjunto de dados atuais e os tamanhos de conjunto de dados de amanhã; Ele é otimizado para alta escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-120">**Scalability**: ReFS is designed for the data set sizes of today and the data set sizes of tomorrow; it’s optimized for high scalability.</span></span>
-   <span data-ttu-id="e6fc9-121">**Compatibilidade de aplicativos**: para maximizar o AppCompat, o ReFS dá suporte a um subconjunto de recursos NTFS, além de APIs do Win32 amplamente adotadas.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-121">**App Compatibility**: To maximize AppCompat, ReFS supports a subset of NTFS features plus Win32 APIs that are widely adopted.</span></span>
-   <span data-ttu-id="e6fc9-122">**Identificação de erro proativo**: os recursos de integridade de ReFS são aproveitados por um verificador de integridade de dados (um "scrubbing") que examina periodicamente o volume, tenta identificar a corrupção latente e, em seguida, dispara proativamente um reparo desses dados corrompidos.</span><span class="sxs-lookup"><span data-stu-id="e6fc9-122">**Proactive Error Identification**: The integrity capabilities of ReFS are leveraged by a data integrity scanner (a “scrubber”) that periodically scans the volume, attempts to identify latent corruption, and then proactively triggers a repair of that corrupt data.</span></span>

## <a name="resources"></a><span data-ttu-id="e6fc9-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="e6fc9-123">Resources</span></span>

-   [<span data-ttu-id="e6fc9-124">Postagem do blog criando o Windows 8 – criando o sistema de arquivos da próxima geração para Windows: ReFS</span><span class="sxs-lookup"><span data-stu-id="e6fc9-124">Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS</span></span>](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [<span data-ttu-id="e6fc9-125">Compatibilidade de aplicativos e ReFS</span><span class="sxs-lookup"><span data-stu-id="e6fc9-125">Application Compatibility and ReFS</span></span>](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 