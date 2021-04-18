---
description: A ação InstallSFPCatalogFile instala os catálogos usados pela proteção de arquivo do Windows me para Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Ação InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759656"
---
# <a name="installsfpcatalogfile-action"></a><span data-ttu-id="e0663-103">Ação InstallSFPCatalogFile</span><span class="sxs-lookup"><span data-stu-id="e0663-103">InstallSFPCatalogFile Action</span></span>

<span data-ttu-id="e0663-104">A ação InstallSFPCatalogFile instala os catálogos usados pela proteção de arquivo do Windows me para Windows.</span><span class="sxs-lookup"><span data-stu-id="e0663-104">The InstallSFPCatalogFile action installs the catalogs used by Windows Me for Windows File Protection.</span></span> <span data-ttu-id="e0663-105">InstallSFPCatalogFile consulta a [tabela de componentes](component-table.md), a [tabela de arquivos](file-table.md), a tabela [FileSFPCatalog](filesfpcatalog-table.md) e a [tabela SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0663-105">InstallSFPCatalogFile queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and [SFPCatalog table](sfpcatalog-table.md).</span></span> <span data-ttu-id="e0663-106">Os catálogos são instalados se estiverem associados a um arquivo em um componente definido para instalação local ou se estiverem associados a um arquivo que está sendo reparado em um componente instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="e0663-106">Catalogs are installed if they are associated with a file in a component that is set for local installation or if they are associated with a file being repaired in a locally installed component.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e0663-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="e0663-107">Sequence Restrictions</span></span>

<span data-ttu-id="e0663-108">A ação InstallSFPCatalogFile deve ser sequenciada antes de [InstallFiles](installfiles-action.md) e depois de [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e0663-108">The InstallSFPCatalogFile action must be sequenced before [InstallFiles](installfiles-action.md) and after [CostFinalize](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e0663-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="e0663-109">ActionData Messages</span></span>



| <span data-ttu-id="e0663-110">Campo</span><span class="sxs-lookup"><span data-stu-id="e0663-110">Field</span></span> | <span data-ttu-id="e0663-111">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="e0663-111">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="e0663-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e0663-112">\[1\]</span></span> | <span data-ttu-id="e0663-113">Nome do catálogo que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="e0663-113">Name of the catalog being installed.</span></span>                          |
| <span data-ttu-id="e0663-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e0663-114">\[2\]</span></span> | <span data-ttu-id="e0663-115">Nome do catálogo no qual a instalação do catálogo depende.</span><span class="sxs-lookup"><span data-stu-id="e0663-115">Name of the catalog this catalog's installation depends upon.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e0663-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0663-116">Remarks</span></span>

<span data-ttu-id="e0663-117">Um catálogo que é dependente de outro catálogo instalado após o catálogo pai.</span><span class="sxs-lookup"><span data-stu-id="e0663-117">A catalog that is dependent on another catalog installed after the parent catalog.</span></span>

 

 



