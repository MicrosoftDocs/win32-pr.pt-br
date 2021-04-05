---
description: ICEM14 valida a coluna Value da tabela ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091020"
---
# <a name="icem14"></a><span data-ttu-id="ae00b-103">ICEM14</span><span class="sxs-lookup"><span data-stu-id="ae00b-103">ICEM14</span></span>

<span data-ttu-id="ae00b-104">ICEM14 valida a coluna Value da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae00b-104">ICEM14 validates the Value Column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="ae00b-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="ae00b-105">Result</span></span>

<span data-ttu-id="ae00b-106">ICEM14 posta os erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae00b-106">ICEM14 posts the following errors.</span></span>



| <span data-ttu-id="ae00b-107">Erro</span><span class="sxs-lookup"><span data-stu-id="ae00b-107">Error</span></span>                                                                                                                                                         | <span data-ttu-id="ae00b-108">Significado</span><span class="sxs-lookup"><span data-stu-id="ae00b-108">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae00b-109">A cadeia de caracteres de substituição na coluna ModuleSubstitution. Value na linha \[ 1 \] . \[ 2 \] . \[ 3 \] não foi encontrado na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae00b-109">The replacement string in ModuleSubstitution.Value column in row \[1\].\[2\].\[3\] is not found in ModuleConfiguration table.</span></span>                                 | <span data-ttu-id="ae00b-110">\[1 \] . \[ 2 \] . \[ 3 \] refere-se a uma chave primária *Table. Row. Column* para uma linha na tabela ModuleSubstitution.</span><span class="sxs-lookup"><span data-stu-id="ae00b-110">\[1\].\[2\].\[3\] refers to a *table.row.column* primary key for a row in the ModuleSubstitution table.</span></span> <span data-ttu-id="ae00b-111">O modelo de formatação no campo valor dessa linha não corresponde a uma linha de atributos configuráveis na [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae00b-111">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                            |
| <span data-ttu-id="ae00b-112">Na tabela ModuleSubstitution na linha \[ 1 \] . \[ 2 \] . \[ 3 \] , um item configurável é indicado na tabela '% s'.</span><span class="sxs-lookup"><span data-stu-id="ae00b-112">In ModuleSubstitution table in row \[1\].\[2\].\[3\], a configurable item is indicated in the table '%s'.</span></span> <span data-ttu-id="ae00b-113">A tabela '% s' não deve conter itens configuráveis.</span><span class="sxs-lookup"><span data-stu-id="ae00b-113">The table '%s' must not contain configurable items.</span></span> | <span data-ttu-id="ae00b-114">Uma das tabelas a seguir está listada na coluna tabela da tabela ModuleSubstitution: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)ou [ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae00b-114">One of the following tables is listed in the Table column of the ModuleSubstitution table: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md), or [ModuleSignature](modulesignature-table.md).</span></span> <span data-ttu-id="ae00b-115">Essas tabelas não podem conter campos configuráveis.</span><span class="sxs-lookup"><span data-stu-id="ae00b-115">These tables cannot contain configurable fields.</span></span> |
| <span data-ttu-id="ae00b-116">Na tabela ModuleSubstitution na linha \[ 1 \] . \[ 2 \] . \[ 3 \] , uma cadeia de caracteres de substituição vazia foi especificada.</span><span class="sxs-lookup"><span data-stu-id="ae00b-116">In ModuleSubstitution table in row \[1\].\[2\].\[3\], an empty replacement string is specified.</span></span>                                                               | <span data-ttu-id="ae00b-117">O modelo de formatação no campo valor dessa linha não corresponde a uma linha de atributos configuráveis na [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae00b-117">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="ae00b-118">ICEM14 posta o aviso a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae00b-118">ICEM14 posts the following warning.</span></span>



| <span data-ttu-id="ae00b-119">Aviso</span><span class="sxs-lookup"><span data-stu-id="ae00b-119">Warning</span></span>                                                                  | <span data-ttu-id="ae00b-120">Significado</span><span class="sxs-lookup"><span data-stu-id="ae00b-120">Meaning</span></span>                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="ae00b-121">A tabela ModuleSubstitution existe, mas a Tabela ModuleConfiguration está ausente</span><span class="sxs-lookup"><span data-stu-id="ae00b-121">ModuleSubstitution table exists but ModuleConfiguration table is missing</span></span> | <span data-ttu-id="ae00b-122">A Tabela ModuleConfiguration está ausente.</span><span class="sxs-lookup"><span data-stu-id="ae00b-122">The ModuleConfiguration table is absent.</span></span> |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="ae00b-123">Tabela usada durante a execução</span><span class="sxs-lookup"><span data-stu-id="ae00b-123">Table Used During Execution</span></span>

[<span data-ttu-id="ae00b-124">Tabela ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="ae00b-124">ModuleSubstitution table</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="ae00b-125">Tabela ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae00b-125">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)

## <a name="related-topics"></a><span data-ttu-id="ae00b-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae00b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae00b-127">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="ae00b-127">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



