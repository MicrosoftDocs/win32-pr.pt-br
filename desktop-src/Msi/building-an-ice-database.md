---
description: Depois de selecionar o ICEs apropriado para validação, um desenvolvedor deve coletar as ações personalizadas em um banco de dados ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Criando um banco de dados ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828043"
---
# <a name="building-an-ice-database"></a><span data-ttu-id="ba702-103">Criando um banco de dados ICE</span><span class="sxs-lookup"><span data-stu-id="ba702-103">Building an ICE Database</span></span>

<span data-ttu-id="ba702-104">Depois de selecionar o [ICES](internal-consistency-evaluators-ices.md) apropriado para validação, um desenvolvedor deve coletar as ações personalizadas em um banco de dados Ice.</span><span class="sxs-lookup"><span data-stu-id="ba702-104">After selecting the appropriate [ICEs](internal-consistency-evaluators-ices.md) for validation, a developer must collect the custom actions together into an ICE database.</span></span> <span data-ttu-id="ba702-105">Um arquivo. Cub é um banco de dados Standard. msi que contém apenas ICEs e suas tabelas necessárias.</span><span class="sxs-lookup"><span data-stu-id="ba702-105">A .cub file is a standard .msi database that contains only ICEs and their required tables.</span></span> <span data-ttu-id="ba702-106">Um arquivo. Cub não pode ser instalado e usado somente para armazenar e fornecer acesso a ações personalizadas do ICE.</span><span class="sxs-lookup"><span data-stu-id="ba702-106">A .cub file cannot be installed and is used only to store and provide access to ICE custom actions.</span></span>

<span data-ttu-id="ba702-107">Um arquivo. Cub contém as tabelas de banco de dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba702-107">A .cub file contains the following database tables.</span></span>



| <span data-ttu-id="ba702-108">Tabela</span><span class="sxs-lookup"><span data-stu-id="ba702-108">Table</span></span>                                  | <span data-ttu-id="ba702-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba702-109">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba702-110">Binary</span><span class="sxs-lookup"><span data-stu-id="ba702-110">Binary</span></span>](binary-table.md)             | <span data-ttu-id="ba702-111">Os arquivos de script, DLLs e EXEs das ações alfandegárias do ICE que são referenciadas na tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="ba702-111">The script files, DLLs, and EXEs of the ICE customs actions that are referenced in the CustomAction table.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="ba702-112">CustomAction</span><span class="sxs-lookup"><span data-stu-id="ba702-112">CustomAction</span></span>](customaction-table.md) | <span data-ttu-id="ba702-113">Cada registro nessa tabela corresponde a uma ação personalizada de ICE incluída no arquivo. cub.</span><span class="sxs-lookup"><span data-stu-id="ba702-113">Each record in this table corresponds to an ICE custom action included in the .cub file.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="ba702-114">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="ba702-114">\_ICESequence</span></span>                          | <span data-ttu-id="ba702-115">Esta tabela lista as ações de Alfândegas do ICE incluídas no arquivo. Cub em sua sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="ba702-115">This table lists the ICE customs actions included in the .cub file in their execution sequence.</span></span> <span data-ttu-id="ba702-116">As ações personalizadas do ICE listadas nesta tabela são executadas chamando [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)ou individualmente executadas usando [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span><span class="sxs-lookup"><span data-stu-id="ba702-116">The ICE custom actions listed in this table are executed by calling [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), or individually executed using [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> |
| [<span data-ttu-id="ba702-117">\_Validação</span><span class="sxs-lookup"><span data-stu-id="ba702-117">\_Validation</span></span>](-validation-table.md)  | <span data-ttu-id="ba702-118">Esta tabela contém as entradas de arquivo. Cub que devem ser mescladas na \_ tabela de validação.</span><span class="sxs-lookup"><span data-stu-id="ba702-118">This table contains the .cub file entries that are to be merged into the \_Validation table.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="ba702-119">\_Especial</span><span class="sxs-lookup"><span data-stu-id="ba702-119">\_Special</span></span>                              | <span data-ttu-id="ba702-120">Todas as tabelas de processamento especial exigidas por ações personalizadas específicas do ICE devem ser incluídas no arquivo. cub.</span><span class="sxs-lookup"><span data-stu-id="ba702-120">Any special processing tables required by particular ICE custom actions must be included in the .cub file.</span></span> <span data-ttu-id="ba702-121">O nome dessas tabelas deve ter um sublinhado à esquerda.</span><span class="sxs-lookup"><span data-stu-id="ba702-121">The name of these tables must have a leading underscore.</span></span>                                                                                                        |



 

<span data-ttu-id="ba702-122">Consulte o [arquivo. Cub de exemplo](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="ba702-122">See [Sample .cub File](sample--cub-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba702-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba702-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba702-124">Criando uma ICE</span><span class="sxs-lookup"><span data-stu-id="ba702-124">Building An ICE</span></span>](building-an-ice.md)
</dt> </dl>

 

 



