---
description: A ação createshortcuts gerencia a criação de atalhos.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Ação createatalhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011602"
---
# <a name="createshortcuts-action"></a><span data-ttu-id="65b38-103">Ação createatalhos</span><span class="sxs-lookup"><span data-stu-id="65b38-103">CreateShortcuts Action</span></span>

<span data-ttu-id="65b38-104">A ação createshortcuts gerencia a criação de atalhos.</span><span class="sxs-lookup"><span data-stu-id="65b38-104">The CreateShortcuts action manages the creation of shortcuts.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="65b38-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="65b38-105">Sequence Restrictions</span></span>

<span data-ttu-id="65b38-106">A ação createshortcuts deve vir após a ação [InstallFiles](installfiles-action.md) e a ação [RemoveShortcuts](removeshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="65b38-106">The CreateShortcuts action must come after the [InstallFiles](installfiles-action.md) action and the [RemoveShortcuts](removeshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="65b38-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="65b38-107">ActionData Messages</span></span>



| <span data-ttu-id="65b38-108">Campo</span><span class="sxs-lookup"><span data-stu-id="65b38-108">Field</span></span> | <span data-ttu-id="65b38-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="65b38-109">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="65b38-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="65b38-110">\[1\]</span></span> | <span data-ttu-id="65b38-111">Identificador do atalho criado.</span><span class="sxs-lookup"><span data-stu-id="65b38-111">Identifier of created shortcut.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="65b38-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="65b38-112">Remarks</span></span>

<span data-ttu-id="65b38-113">A ação createshortcuts cria atalhos para os principais arquivos de componentes dos recursos selecionados para instalação ou anúncio.</span><span class="sxs-lookup"><span data-stu-id="65b38-113">The CreateShortcuts action creates shortcuts to the key files of components of features that are selected for installation or advertisement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65b38-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65b38-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65b38-115">Tabela de atalho</span><span class="sxs-lookup"><span data-stu-id="65b38-115">Shortcut Table</span></span>](shortcut-table.md)
</dt> <dt>

[<span data-ttu-id="65b38-116">Tabela MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="65b38-116">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
</dt> </dl>

 

 



