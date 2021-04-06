---
description: A ação de BindImage associa cada executável ou DLL que deve ser associado às DLLs importadas por ele.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Ação de BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828049"
---
# <a name="bindimage-action"></a><span data-ttu-id="d11e4-103">Ação de BindImage</span><span class="sxs-lookup"><span data-stu-id="d11e4-103">BindImage Action</span></span>

<span data-ttu-id="d11e4-104">A ação de BindImage associa cada executável ou DLL que deve ser associado às DLLs importadas por ele.</span><span class="sxs-lookup"><span data-stu-id="d11e4-104">The BindImage action binds each executable or DLL that must be bound to the DLLs imported by it.</span></span> <span data-ttu-id="d11e4-105">A ação de BindImage atua em cada arquivo na tabela [BindImage](bindimage-table.md) , mas somente os que devem ser instalados localmente.</span><span class="sxs-lookup"><span data-stu-id="d11e4-105">The BindImage action acts on each file in the [BindImage](bindimage-table.md) table, but only those that are to be installed locally.</span></span> <span data-ttu-id="d11e4-106">O instalador computa o endereço virtual de cada função importada de todas as DLLs e salva o endereço virtual calculado na tabela de endereços de [*importação*](i-gly.md) da imagem de importação (IAT).</span><span class="sxs-lookup"><span data-stu-id="d11e4-106">The installer computes the virtual address of each function imported from all DLLs, then saves the computed virtual address in the importing image's [*import address table*](i-gly.md) (IAT).</span></span>

<span data-ttu-id="d11e4-107">A ação de BindImage chama internamente a API do Windows **BindImageEx** .</span><span class="sxs-lookup"><span data-stu-id="d11e4-107">The BindImage Action internally calls the **BindImageEx** Windows API.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d11e4-108">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="d11e4-108">Sequence Restrictions</span></span>

<span data-ttu-id="d11e4-109">A ação de BindImage deve vir após a ação [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d11e4-109">The BindImage action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d11e4-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="d11e4-110">ActionData Messages</span></span>



| <span data-ttu-id="d11e4-111">Campo</span><span class="sxs-lookup"><span data-stu-id="d11e4-111">Field</span></span> | <span data-ttu-id="d11e4-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="d11e4-112">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="d11e4-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d11e4-113">\[1\]</span></span> | <span data-ttu-id="d11e4-114">Identificador de arquivo do executável.</span><span class="sxs-lookup"><span data-stu-id="d11e4-114">File identifier of executable.</span></span> |



 

 

 



