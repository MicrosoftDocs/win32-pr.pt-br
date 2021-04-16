---
description: A tabela a seguir mostra os vários métodos que o aplicativo pode usar para lidar com o cursor, a justificativa e os clusters.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Trabalhando com relações entre posições de cursor, pontos de justificações e clusters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757976"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a><span data-ttu-id="b7702-103">Trabalhando com relações entre posições de cursor, pontos de justificações e clusters</span><span class="sxs-lookup"><span data-stu-id="b7702-103">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>

<span data-ttu-id="b7702-104">A tabela a seguir mostra os vários métodos que o aplicativo pode usar para lidar com o cursor, a justificativa e os clusters.</span><span class="sxs-lookup"><span data-stu-id="b7702-104">The following table shows the various methods that the application can use to handle the caret, justification, and clusters.</span></span>



| <span data-ttu-id="b7702-105">Tarefa</span><span class="sxs-lookup"><span data-stu-id="b7702-105">Task</span></span>                             | <span data-ttu-id="b7702-106">Suporte ao Uniscribe</span><span class="sxs-lookup"><span data-stu-id="b7702-106">Uniscribe support</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7702-107">Movimento do cursor por cluster de caracteres</span><span class="sxs-lookup"><span data-stu-id="b7702-107">Caret move by character cluster</span></span>  | <span data-ttu-id="b7702-108">O parâmetro *pwLogClust* do [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** membro da estrutura de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="b7702-108">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="b7702-109">O membro **fCharStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="b7702-109">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="b7702-110">Quebra de linha entre caracteres</span><span class="sxs-lookup"><span data-stu-id="b7702-110">Line breaking between characters</span></span> | <span data-ttu-id="b7702-111">O parâmetro *pwLogClust* do [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** membro da estrutura de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="b7702-111">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="b7702-112">O membro **fCharStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="b7702-112">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="b7702-113">Mover o cursor por palavra</span><span class="sxs-lookup"><span data-stu-id="b7702-113">Caret move by word</span></span>               | <span data-ttu-id="b7702-114">O membro **fWordStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="b7702-114">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="b7702-115">Quebra de linha entre palavras</span><span class="sxs-lookup"><span data-stu-id="b7702-115">Line breaking between words</span></span>      | <span data-ttu-id="b7702-116">O membro **fWordStop** da estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="b7702-116">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="b7702-117">Justificativa</span><span class="sxs-lookup"><span data-stu-id="b7702-117">Justification</span></span>                    | <span data-ttu-id="b7702-118">O membro **uJustification** da estrutura [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="b7702-118">The **uJustification** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="b7702-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7702-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7702-120">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="b7702-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




