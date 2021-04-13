---
description: ICE84 verifica a tabela AdvtExecuteSequence, a tabela AdminExecuteSequence e a tabela InstallExecuteSequence para verificar se as seguintes ações padrão não foram definidas com condições no campo condição.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297204"
---
# <a name="ice84"></a><span data-ttu-id="10a0b-103">ICE84</span><span class="sxs-lookup"><span data-stu-id="10a0b-103">ICE84</span></span>

<span data-ttu-id="10a0b-104">ICE84 verifica a tabela [AdvtExecuteSequence](advtexecutesequence-table.md), a [tabela AdminExecuteSequence](adminexecutesequence-table.md)e a [tabela InstallExecuteSequence](installexecutesequence-table.md) para verificar se as seguintes [ações padrão](standard-actions.md) não foram definidas com condições no campo condição.</span><span class="sxs-lookup"><span data-stu-id="10a0b-104">ICE84 checks the [AdvtExecuteSequence table](advtexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), and the [InstallExecuteSequence table](installexecutesequence-table.md) to verify that the following [standard actions](standard-actions.md) have not been set with conditions in the Condition field.</span></span>

-   [<span data-ttu-id="10a0b-105">Ação CostInitialize</span><span class="sxs-lookup"><span data-stu-id="10a0b-105">CostInitialize action</span></span>](costinitialize-action.md)
-   [<span data-ttu-id="10a0b-106">Ação CostFinalize</span><span class="sxs-lookup"><span data-stu-id="10a0b-106">CostFinalize action</span></span>](costfinalize-action.md)
-   [<span data-ttu-id="10a0b-107">Ação de custo de</span><span class="sxs-lookup"><span data-stu-id="10a0b-107">FileCost action</span></span>](filecost-action.md)
-   [<span data-ttu-id="10a0b-108">Ação InstallValidate</span><span class="sxs-lookup"><span data-stu-id="10a0b-108">InstallValidate action</span></span>](installvalidate-action.md)
-   [<span data-ttu-id="10a0b-109">Ação InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="10a0b-109">InstallInitialize action</span></span>](installinitialize-action.md)
-   [<span data-ttu-id="10a0b-110">Ação InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="10a0b-110">InstallFinalize action</span></span>](installfinalize-action.md)
-   [<span data-ttu-id="10a0b-111">Ação ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="10a0b-111">ProcessComponents action</span></span>](processcomponents-action.md)
-   [<span data-ttu-id="10a0b-112">Ação PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="10a0b-112">PublishFeatures action</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="10a0b-113">Ação PublishProduct</span><span class="sxs-lookup"><span data-stu-id="10a0b-113">PublishProduct action</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="10a0b-114">Ação RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="10a0b-114">RegisterProduct action</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="10a0b-115">Ação UnpublishFeatures</span><span class="sxs-lookup"><span data-stu-id="10a0b-115">UnpublishFeatures action</span></span>](unpublishfeatures-action.md)

<span data-ttu-id="10a0b-116">Se condições forem encontradas, o ICE84 lançará um aviso.</span><span class="sxs-lookup"><span data-stu-id="10a0b-116">If conditions are found, ICE84 posts a warning.</span></span>

## <a name="result"></a><span data-ttu-id="10a0b-117">Resultado</span><span class="sxs-lookup"><span data-stu-id="10a0b-117">Result</span></span>

<span data-ttu-id="10a0b-118">ICE84 posta o aviso a seguir.</span><span class="sxs-lookup"><span data-stu-id="10a0b-118">ICE84 posts the following warning.</span></span>



| <span data-ttu-id="10a0b-119">Erro de ICE84</span><span class="sxs-lookup"><span data-stu-id="10a0b-119">ICE84 error</span></span>                                                             | <span data-ttu-id="10a0b-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="10a0b-120">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="10a0b-121">A ação ' \[ 1 \] ' encontrada na tabela% s é uma ação necessária com uma condição.</span><span class="sxs-lookup"><span data-stu-id="10a0b-121">Action '\[1\]' found in %s table is a required action with a condition.</span></span> | <span data-ttu-id="10a0b-122">Uma ação necessária foi criada com uma condição.</span><span class="sxs-lookup"><span data-stu-id="10a0b-122">A required action has been authored with a condition.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="10a0b-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10a0b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10a0b-124">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="10a0b-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



