---
description: Os valores do registro devem ser definidos para verbos para lidar com situações em que um usuário pode selecionar um único item, vários itens ou uma seleção de um item. Um verbo requer valores de registro separados para cada uma dessas três situações às quais o verbo dá suporte.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Como empregar o modelo de seleção de verbo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967906"
---
# <a name="how-to-employ-the-verb-selection-model"></a><span data-ttu-id="156ec-104">Como empregar o modelo de seleção de verbo</span><span class="sxs-lookup"><span data-stu-id="156ec-104">How to Employ the Verb Selection Model</span></span>

<span data-ttu-id="156ec-105">Os valores do registro devem ser definidos para verbos para lidar com situações em que um usuário pode selecionar um único item, vários itens ou uma seleção de um item.</span><span class="sxs-lookup"><span data-stu-id="156ec-105">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="156ec-106">Um verbo requer valores de registro separados para cada uma dessas três situações às quais o verbo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="156ec-106">A verb requires separate registry values for each of these three situations that the verb supports.</span></span>

## <a name="instructions"></a><span data-ttu-id="156ec-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="156ec-107">Instructions</span></span>


<span data-ttu-id="156ec-108">Especifique o valor de MultiSelectModel para todos os verbos.</span><span class="sxs-lookup"><span data-stu-id="156ec-108">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="156ec-109">Se o valor de MultiSelectModel não for especificado, ele será inferido do tipo de implementação de verbo que você escolheu.</span><span class="sxs-lookup"><span data-stu-id="156ec-109">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="156ec-110">Para métodos baseados em COM (como DropTarget e ExecuteCommand), o **Player** é assumido e, para os outros métodos, o **documento** é assumido.</span><span class="sxs-lookup"><span data-stu-id="156ec-110">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>

<span data-ttu-id="156ec-111">Os valores possíveis para o modelo de seleção de verbo são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="156ec-111">The possible values for the verb selection model are as follows:</span></span>

1.  <span data-ttu-id="156ec-112">Especifique **single** para verbos que dão suporte a apenas uma única seleção.</span><span class="sxs-lookup"><span data-stu-id="156ec-112">Specify **Single** for verbs that support only a single selection.</span></span>
2.  <span data-ttu-id="156ec-113">Especifique o **Player** para verbos que dão suporte a qualquer número de itens.</span><span class="sxs-lookup"><span data-stu-id="156ec-113">Specify **Player** for verbs that support any number of items.</span></span>
3.  <span data-ttu-id="156ec-114">Especifique o **documento** para verbos que criam uma janela de nível superior para cada item.</span><span class="sxs-lookup"><span data-stu-id="156ec-114">Specify **Document** for verbs that create a top-level window for each item.</span></span> <span data-ttu-id="156ec-115">Isso limita o número de itens que são ativados e ajuda a evitar a execução de recursos do sistema se o usuário abrir muitas janelas.</span><span class="sxs-lookup"><span data-stu-id="156ec-115">Doing so limits the number of items that are activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

## <a name="remarks"></a><span data-ttu-id="156ec-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="156ec-116">Remarks</span></span>

<span data-ttu-id="156ec-117">Quando o número de itens selecionados não corresponde ao modelo de seleção de verbo ou é maior que os limites padrão descritos na tabela a seguir, o verbo não aparece.</span><span class="sxs-lookup"><span data-stu-id="156ec-117">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="156ec-118">Tipo de implementação de verbo</span><span class="sxs-lookup"><span data-stu-id="156ec-118">Type of verb implementation</span></span> | <span data-ttu-id="156ec-119">Documento</span><span class="sxs-lookup"><span data-stu-id="156ec-119">Document</span></span> | <span data-ttu-id="156ec-120">Jogador</span><span class="sxs-lookup"><span data-stu-id="156ec-120">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="156ec-121">Herdada</span><span class="sxs-lookup"><span data-stu-id="156ec-121">Legacy</span></span>                      | <span data-ttu-id="156ec-122">15 itens</span><span class="sxs-lookup"><span data-stu-id="156ec-122">15 items</span></span> | <span data-ttu-id="156ec-123">100 itens</span><span class="sxs-lookup"><span data-stu-id="156ec-123">100 items</span></span> |
| <span data-ttu-id="156ec-124">COM</span><span class="sxs-lookup"><span data-stu-id="156ec-124">COM</span></span>                         | <span data-ttu-id="156ec-125">15 itens</span><span class="sxs-lookup"><span data-stu-id="156ec-125">15 items</span></span> | <span data-ttu-id="156ec-126">Sem limite</span><span class="sxs-lookup"><span data-stu-id="156ec-126">No limit</span></span>  |



 

<span data-ttu-id="156ec-127">Veja a seguir as entradas de registro de exemplo que usam o valor MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="156ec-127">The following are example registry entries that use the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



