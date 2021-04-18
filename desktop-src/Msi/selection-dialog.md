---
description: Essa caixa de diálogo modal permite que os usuários selecionem itens específicos.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Caixa de diálogo de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751631"
---
# <a name="selection-dialog"></a><span data-ttu-id="4ecc8-103">Caixa de diálogo de seleção</span><span class="sxs-lookup"><span data-stu-id="4ecc8-103">Selection Dialog</span></span>

<span data-ttu-id="4ecc8-104">Essa caixa de diálogo modal permite que os usuários selecionem itens específicos.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-104">This modal dialog box enables users to select particular items.</span></span>

<span data-ttu-id="4ecc8-105">Uma caixa de diálogo de seleção contém um [controle SelectionTree](selectiontree-control.md) que publica vários ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-105">A Selection Dialog box contains a [SelectionTree control](selectiontree-control.md) that publishes several ControlEvents.</span></span> <span data-ttu-id="4ecc8-106">Normalmente, esses ControlEvents são assinados por [texto](text-control.md), [ícone](icon-control.md)ou controles de [bitmap](bitmap-control.md) que exibem uma descrição, o tamanho, o caminho e o ícone do item realçado.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-106">Commonly these ControlEvents are subscribed to by [Text](text-control.md), [Icon](icon-control.md), or [Bitmap](bitmap-control.md) controls that display a description, the size, the path, and the icon of the highlighted item.</span></span>

<span data-ttu-id="4ecc8-107">Há um [controle de pressão](pushbutton-control.md) na caixa de diálogo que publica o [SelectionBrowse ControlEvent,](selectionbrowse-controlevent.md) e gera uma caixa de [diálogo de procura](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="4ecc8-107">There is a [PushButton control](pushbutton-control.md) on the dialog box that publishes the [SelectionBrowse ControlEvent](selectionbrowse-controlevent.md) and spawns a [Browse Dialog](browse-dialog.md).</span></span> <span data-ttu-id="4ecc8-108">O controle procurar permite que o usuário selecione um diretório.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-108">The Browse control enables the user to select a directory.</span></span>

<span data-ttu-id="4ecc8-109">A árvore de seleção é preenchida somente depois que a [ação CostInitialize](costinitialize-action.md) e a [ação CostFinalize](costfinalize-action.md) são chamadas.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-109">The selection tree is populated only after the [CostInitialize action](costinitialize-action.md) and [CostFinalize action](costfinalize-action.md) are called.</span></span>

<span data-ttu-id="4ecc8-110">Uma caixa de diálogo de seleção é normalmente usada para selecionar recursos.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-110">A Selection dialog box is commonly used to select features.</span></span> <span data-ttu-id="4ecc8-111">Os recursos são listados como itens em um controle SelectionTree e rotulados com a cadeia de caracteres curta do texto que aparece na coluna título da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="4ecc8-111">The features are listed as items in a SelectionTree control and labeled with the short string of text appearing in the Title column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="4ecc8-112">A cadeia de texto na coluna Descrição da tabela de recursos é publicada como uma [SelectionDescription ControlEvent,](selectiondescription-controlevent.md) e exibida por um [controle de texto](text-control.md) na caixa de diálogo seleção.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-112">The text string in the Description column of the Feature table is published as a [SelectionDescription ControlEvent](selectiondescription-controlevent.md) and displayed by a [Text control](text-control.md) in the Selection Dialog box.</span></span> <span data-ttu-id="4ecc8-113">O controle de árvore de seleção também publica o identificador para o ícone do item realçado.</span><span class="sxs-lookup"><span data-stu-id="4ecc8-113">The Selection tree control also publishes the handle to the icon of the highlighted item.</span></span>

 

 



