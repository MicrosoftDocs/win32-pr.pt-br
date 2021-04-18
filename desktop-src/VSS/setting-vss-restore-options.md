---
description: As opções de restauração permitem que os solicitantes comuniquem opções de restauração personalizadas para gravadores.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Definindo opções de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788830"
---
# <a name="setting-vss-restore-options"></a><span data-ttu-id="ce8fa-103">Definindo opções de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="ce8fa-103">Setting VSS Restore Options</span></span>

<span data-ttu-id="ce8fa-104">As opções de restauração permitem que os solicitantes comuniquem opções de restauração personalizadas para gravadores.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-104">Restore options allow requesters to communicate customized restore options to writers.</span></span>

## <a name="restore-options"></a><span data-ttu-id="ce8fa-105">Opções de restauração</span><span class="sxs-lookup"><span data-stu-id="ce8fa-105">Restore Options</span></span>

<span data-ttu-id="ce8fa-106">Padronizar o formato das opções de restauração permite que gravadores e solicitantes manipulem solicitações personalizadas comuns.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-106">Standardizing the format of the restore options allow writers and requesters to handle common custom requests.</span></span> <span data-ttu-id="ce8fa-107">As opções de restauração são definidas pelo solicitante chamando o método [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) até uma vez por componente selecionado para backup antes de chamar o método [**IVssBackupComponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .</span><span class="sxs-lookup"><span data-stu-id="ce8fa-107">Restore options are set by the requester by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method up to once per selected-for-backup component before calling the [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) method.</span></span> <span data-ttu-id="ce8fa-108">A cadeia de caracteres passada no parâmetro *wszRestoreOptions* para o método **setrestore** pode conter vários valores, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-108">The string passed in the *wszRestoreOptions* parameter to the **SetRestoreOptions** method can contain multiple values, as described below.</span></span>

## <a name="format"></a><span data-ttu-id="ce8fa-109">Formatar</span><span class="sxs-lookup"><span data-stu-id="ce8fa-109">Format</span></span>

<span data-ttu-id="ce8fa-110">O formato das opções de restauração, é um ou mais pares de nome/valor separados por vírgula, e o nome é opcionalmente prefixado com o nome do subcomponente ao qual se aplica.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-110">The format of restore options, is one or more comma-separated name/value pairs, and the name is optionally prefixed with the name of the subcomponent to which it applies.</span></span> <span data-ttu-id="ce8fa-111">Os nomes de componente e os nomes de opção não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-111">The component names and option names are case-insensitive.</span></span> <span data-ttu-id="ce8fa-112">A diferenciação de maiúsculas e minúsculas dos valores é determinada pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-112">The case-sensitivity of the values is determined by the writer.</span></span> <span data-ttu-id="ce8fa-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ce8fa-113">For example:</span></span>

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

<span data-ttu-id="ce8fa-114">Neste exemplo, "opção 1" aplica-se apenas ao subcomponente "child1" e seus descendentes, "opção 2" aplica-se a todos os componentes e seus descendentes, e "Option3" aplica-se somente aos \\ Subcomponentes "child2 Grandchild3" e seus descendentes.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-114">In this example, "Option1" only applies to the "Child1" subcomponent and its descendants, "Option2" applies to all components and their descendants, and "Option3" applies only to the "Child2\\Grandchild3" subcomponents and its descendants.</span></span>

<span data-ttu-id="ce8fa-115">O método [**setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) só pode ser chamado em componentes que são selecionáveis para backup, enquanto os nós descendentes podem não ser selecionáveis para backup, podem ser selecionáveis para restauração.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-115">The [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method can only be called on components that are selectable for backup, while descendant nodes may not be selectable for backup, they may be selectable for restore.</span></span>

## <a name="common-restore-options"></a><span data-ttu-id="ce8fa-116">Opções comuns de restauração</span><span class="sxs-lookup"><span data-stu-id="ce8fa-116">Common Restore Options</span></span>

<span data-ttu-id="ce8fa-117">Essas opções de restauração comuns foram definidas para aumentar a interoperabilidade entre gravadores e solicitantes.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-117">These common restore options have been defined to increase interoperability between writers and requesters.</span></span>

-   <span data-ttu-id="ce8fa-118">Autoriza</span><span class="sxs-lookup"><span data-stu-id="ce8fa-118">Authoritative</span></span>

    <span data-ttu-id="ce8fa-119">A opção "autoritativo" dá suporte a vários valores "item", mas apenas um valor "All".</span><span class="sxs-lookup"><span data-stu-id="ce8fa-119">The "Authoritative" option supports multiple "Item" values, but only one "All" value.</span></span>

    <span data-ttu-id="ce8fa-120">Todo o componente é autoritativo.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-120">This entire component is authoritative.</span></span>

    ``` syntax
    "Authoritative"="All"
    ```

    <span data-ttu-id="ce8fa-121">Somente o item especificado é autoritativo.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-121">Only the specified item is authoritative.</span></span> <span data-ttu-id="ce8fa-122">O formato do item nomeado é definido pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-122">The format of the named item is defined by the writer.</span></span> <span data-ttu-id="ce8fa-123">Designações comuns são " \* " para indicar todos os arquivos, "..." para indicar todos os arquivos e subdiretórios do componente especificado.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-123">Common designations are "\*" to indicate all files, "..." to indicate all files and subdirectories of the specified component.</span></span>

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   <span data-ttu-id="ce8fa-124">Rolar para frente</span><span class="sxs-lookup"><span data-stu-id="ce8fa-124">Roll Forward</span></span>

    <span data-ttu-id="ce8fa-125">Depois que um banco de dados é restaurado, os gravadores geralmente passam pelos logs para atualizar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-125">After a database is restored, writers usually roll forward through logs to bring the database up to date.</span></span> <span data-ttu-id="ce8fa-126">No caso de restaurações incrementais ou diferenciais, o solicitante usa o método [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) para controlar parcialmente o comportamento de manipulação de log – essa opção de restauração permite um controle mais granular.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-126">In the case of incremental or differential restores, the requester uses the [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) method to partially control the log-handling behavior - this restore option allows more granular control.</span></span>

    <span data-ttu-id="ce8fa-127">Não faça a distribuição de logs.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-127">Do not roll through logs.</span></span>

    ``` syntax
    "Roll Forward"="None"
    ```

    <span data-ttu-id="ce8fa-128">Faça o roll-through de todos os logs.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-128">Roll through all logs.</span></span>

    ``` syntax
    "Roll Forward"="All"
    ```

    <span data-ttu-id="ce8fa-129">Faça o roll-through dos logs até o ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-129">Roll through logs up to specified point.</span></span> <span data-ttu-id="ce8fa-130">O formato do ponto especificado é definido pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-130">The format of the specified point is defined by the writer.</span></span>

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   <span data-ttu-id="ce8fa-131">Novo nome do componente</span><span class="sxs-lookup"><span data-stu-id="ce8fa-131">New Component Name</span></span>

    <span data-ttu-id="ce8fa-132">Um gravador pode querer restaurar um componente para um novo nome.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-132">A writer may want to restore a component to a new name.</span></span> <span data-ttu-id="ce8fa-133">Por exemplo, restaurar um banco de dados para um nome diferente para restaurar um item individual; a restauração para o mesmo nome faria todos os dados que recomendamos que os gravadores aceitem um caminho lógico e um nome de componente válidos como valor de opções.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-133">For example, restoring a database to a different name to restore an individual item; restoring to the same name would please all data We recommend that writers accept a valid logical path and component name as this options' value.</span></span> <span data-ttu-id="ce8fa-134">Isso geralmente será usado com um [*destino direcionado*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="ce8fa-134">This will often be used with a [*directed target*](vssgloss-d.md).</span></span>

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



