---
description: No processamento de um backup no VSS, os solicitantes e os gravadores trabalharam juntos para produzir uma imagem de sistema estável da qual fazer backup dos dados, o que exigia a coordenação e a criação de uma cópia de sombra do sistema atual.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Visão geral do processamento de uma restauração no VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781305"
---
# <a name="overview-of-processing-a-restore-under-vss"></a><span data-ttu-id="70d81-103">Visão geral do processamento de uma restauração no VSS</span><span class="sxs-lookup"><span data-stu-id="70d81-103">Overview of Processing a Restore Under VSS</span></span>

<span data-ttu-id="70d81-104">No processamento de um backup no VSS, os solicitantes e os gravadores trabalharam juntos para produzir uma imagem de sistema estável da qual fazer backup dos dados, o que exigia a coordenação e a criação de uma cópia de sombra do sistema atual.</span><span class="sxs-lookup"><span data-stu-id="70d81-104">In processing a backup under VSS, requesters and writers worked together to produce a stable system image from which to back up data, which required coordination and the creation of a shadow copy of the current system.</span></span>

<span data-ttu-id="70d81-105">Ao contrário de um backup do VSS, onde a finalidade da coordenação do solicitante e dos gravadores é produzir uma imagem do sistema estável da qual os dados serão copiados, o objetivo de uma restauração baseada em VSS é retornar arquivos para o disco de maneira mais útil para os aplicativos (gravadores) em execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="70d81-105">In contrast to a VSS backup, where the purpose of requester and writers coordination is to produce a stable system image from which to copy data, the objective of a VSS-based restore is to return files to disk in a manner most useful to applications (writers) currently running on the system.</span></span> <span data-ttu-id="70d81-106">Isso não requer uma imagem de sistema estável, portanto, nenhuma cópia de sombra é necessária.</span><span class="sxs-lookup"><span data-stu-id="70d81-106">This does not require a stable system image, so no shadow copy is necessary.</span></span>

<span data-ttu-id="70d81-107">Em vez disso, a atenção está concentrada em evitar a interrupção da atividade do gravador, impedindo a criação de conjuntos de dados inconsistentes em disco e permitindo que os gravadores o escopo necessário avaliem e mesclem os dados quando necessário.</span><span class="sxs-lookup"><span data-stu-id="70d81-107">Instead, attention is focused on avoiding disruption of writer activity, preventing the creation of inconsistent data sets on disk, and allowing writers the necessary scope to evaluate and merge data when necessary.</span></span>

<span data-ttu-id="70d81-108">Como uma operação de backup, uma restauração do VSS requer acesso ao documento de componentes de backup e aos documentos de metadados do gravador.</span><span class="sxs-lookup"><span data-stu-id="70d81-108">Like a backup operation, a VSS restore requires access to both a Backup Components Document and to Writer Metadata Documents.</span></span> <span data-ttu-id="70d81-109">Em geral, esses documentos não são obtidos pela consulta de aplicativos em execução, mas são recuperados de versões armazenadas como documentos XML na mídia de backup.</span><span class="sxs-lookup"><span data-stu-id="70d81-109">These documents are not generally obtained by querying running applications, but instead are retrieved from versions stored as XML documents on backup media.</span></span>

<span data-ttu-id="70d81-110">Como é o caso durante operações de backup, os documentos de metadados do gravador permanecem objetos somente leitura e (uma vez recuperados) o documento de componentes de backup ainda pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="70d81-110">As is the case during backup operations, the Writer Metadata Documents remain read-only objects, and (once retrieved) the Backup Components Document can still be modified.</span></span> <span data-ttu-id="70d81-111">As modificações do documento de componentes de backup permitem que gravadores e solicitante se comuniquem sobre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="70d81-111">Modifications of the Backup Components Document allow writers and requester to communicate about the following:</span></span>

-   <span data-ttu-id="70d81-112">Substituindo [*métodos de restauração*](vssgloss-r.md) por [*destinos de restauração*](vssgloss-r.md)</span><span class="sxs-lookup"><span data-stu-id="70d81-112">Overriding [*restore methods*](vssgloss-r.md) with [*restore targets*](vssgloss-r.md)</span></span>
-   <span data-ttu-id="70d81-113">Usando [ *mapeamentos de local alternativos*](vssgloss-a.md)</span><span class="sxs-lookup"><span data-stu-id="70d81-113">Using [*alternate location mappings*](vssgloss-a.md)</span></span>
-   <span data-ttu-id="70d81-114">Restaurando arquivos para novos locais no disco</span><span class="sxs-lookup"><span data-stu-id="70d81-114">Restoring files to new locations on disk</span></span>
-   <span data-ttu-id="70d81-115">Usando regras de seleção diferentes daquelas usadas durante o backup</span><span class="sxs-lookup"><span data-stu-id="70d81-115">Using different selection rules from those used during backup</span></span>

<span data-ttu-id="70d81-116">Para entender com mais detalhes as tarefas básicas envolvidas na execução de uma restauração, é útil dividir esta visão geral nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="70d81-116">To more fully understand the basic tasks involved in performing a restore, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="70d81-117">Visão geral da inicialização da restauração</span><span class="sxs-lookup"><span data-stu-id="70d81-117">Overview of Restore Initialization</span></span>](overview-of-restore-initialization.md)
-   [<span data-ttu-id="70d81-118">Visão geral da preparação para restauração</span><span class="sxs-lookup"><span data-stu-id="70d81-118">Overview of Preparing for Restore</span></span>](overview-of-preparing-for-restore.md)
-   [<span data-ttu-id="70d81-119">Visão geral da restauração de arquivo real</span><span class="sxs-lookup"><span data-stu-id="70d81-119">Overview of Actual File Restoration</span></span>](overview-of-actual-file-restoration.md)
-   [<span data-ttu-id="70d81-120">Visão geral da limpeza e término da restauração</span><span class="sxs-lookup"><span data-stu-id="70d81-120">Overview of Restore Clean up and Termination</span></span>](overview-of-restore-clean-up-and-termination.md)

 

 



