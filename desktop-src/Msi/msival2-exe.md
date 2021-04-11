---
description: Msival2.exe é um utilitário de linha de comando que pode executar um conjunto de avaliadores de consistência internos-ICEs.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172019"
---
# <a name="msival2exe"></a><span data-ttu-id="59605-103">Msival2.exe</span><span class="sxs-lookup"><span data-stu-id="59605-103">Msival2.exe</span></span>

<span data-ttu-id="59605-104">Msival2.exe é um utilitário de linha de comando que pode executar um conjunto de [avaliadores de consistência internos-ICES](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="59605-104">Msival2.exe is a command line utility that can run a suite of [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="59605-105">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="59605-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="59605-106">Para obter mais informações sobre ICEs e o arquivo CUB, consulte [usando avaliadores de consistência internos](using-internal-consistency-evaluators.md).</span><span class="sxs-lookup"><span data-stu-id="59605-106">For more information about ICEs and the CUB file, see [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="59605-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59605-107">Syntax</span></span>

<span data-ttu-id="59605-108">**Msival2** *{Database} {arquivo Cub} \[ -f \] \[ -l {logfile} \] \[ -i {ID do Ice} \[ : {ID do Ice}. \] \] ..*</span><span class="sxs-lookup"><span data-stu-id="59605-108">**Msival2** *{database}{CUB file}\[-f\]\[-l {logfile}\]\[-i {ICE Id}\[:{ICE Id}...\]\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="59605-109">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="59605-109">Command Line Options</span></span>

<span data-ttu-id="59605-110">Msival2.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="59605-110">Msival2.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="59605-111">Um delimitador de barra também pode ser usado no lugar de um traço.</span><span class="sxs-lookup"><span data-stu-id="59605-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="59605-112">Opção</span><span class="sxs-lookup"><span data-stu-id="59605-112">Option</span></span> | <span data-ttu-id="59605-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="59605-113">Description</span></span>                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59605-114">-f</span><span class="sxs-lookup"><span data-stu-id="59605-114">-f</span></span>     | <span data-ttu-id="59605-115">Filtre todas as mensagens informativas dos resultados exibidos.</span><span class="sxs-lookup"><span data-stu-id="59605-115">Filter out all informational messages from the displayed results.</span></span> <span data-ttu-id="59605-116">Todos os outros tipos de mensagens são exibidos.</span><span class="sxs-lookup"><span data-stu-id="59605-116">All other types of messages are displayed.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="59605-117">-i</span><span class="sxs-lookup"><span data-stu-id="59605-117">-i</span></span>     | <span data-ttu-id="59605-118">Execute apenas o ICEs listado na linha de comando na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="59605-118">Run only the ICEs listed on the command line in the order specified.</span></span> <span data-ttu-id="59605-119">Cada ação personalizada de ICE deve ser listada como aparece na [tabela CustomAction](customaction-table.md) do arquivo Cub.</span><span class="sxs-lookup"><span data-stu-id="59605-119">Each ICE custom action should be listed as it appears in the [CustomAction table](customaction-table.md) of the CUB file.</span></span> <span data-ttu-id="59605-120">Se essa opção for omitida, a ferramenta executará o conjunto padrão de ICEs especificado pelo autor do arquivo CUB.</span><span class="sxs-lookup"><span data-stu-id="59605-120">If this option is omitted, the tool runs the default set of ICEs specified by the author of the CUB file.</span></span> |
| <span data-ttu-id="59605-121">-l</span><span class="sxs-lookup"><span data-stu-id="59605-121">-l</span></span>     | <span data-ttu-id="59605-122">Gravar resultados no arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="59605-122">Write results to the specified file.</span></span> <span data-ttu-id="59605-123">O arquivo ainda não deve existir.</span><span class="sxs-lookup"><span data-stu-id="59605-123">The file must not already exist.</span></span> <span data-ttu-id="59605-124">Se o arquivo existir, ele não será substituído.</span><span class="sxs-lookup"><span data-stu-id="59605-124">If the file exists, it is not overwritten.</span></span>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="59605-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59605-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59605-126">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="59605-126">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="59605-127">Avaliadores de consistência internos-ICEs</span><span class="sxs-lookup"><span data-stu-id="59605-127">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
</dt> <dt>

[<span data-ttu-id="59605-128">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="59605-128">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



