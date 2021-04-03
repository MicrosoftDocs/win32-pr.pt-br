---
description: A ação UnregisterComPlus remove aplicativos COM+ do registro.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Ação UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922899"
---
# <a name="unregistercomplus-action"></a><span data-ttu-id="a1297-103">Ação UnregisterComPlus</span><span class="sxs-lookup"><span data-stu-id="a1297-103">UnregisterComPlus Action</span></span>

<span data-ttu-id="a1297-104">A ação UnregisterComPlus remove aplicativos COM+ do registro.</span><span class="sxs-lookup"><span data-stu-id="a1297-104">The UnregisterComPlus action removes COM+ applications from the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a1297-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="a1297-105">Sequence Restrictions</span></span>

<span data-ttu-id="a1297-106">A [ação RegisterComPlus](registercomplus-action.md) deve seguir a [ação InstallFiles](installfiles-action.md) e a ação UnregisterComPlus.</span><span class="sxs-lookup"><span data-stu-id="a1297-106">The [RegisterComPlus action](registercomplus-action.md) must follow the [InstallFiles action](installfiles-action.md) and the UnregisterComPlus action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a1297-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="a1297-107">ActionData Messages</span></span>



| <span data-ttu-id="a1297-108">Campo</span><span class="sxs-lookup"><span data-stu-id="a1297-108">Field</span></span> | <span data-ttu-id="a1297-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="a1297-109">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="a1297-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a1297-110">\[1\]</span></span> | <span data-ttu-id="a1297-111">Identificador de aplicativo do aplicativo COM+ que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="a1297-111">Application identifier of the COM+ application being removed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1297-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1297-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1297-113">Ação RegisterComPlus</span><span class="sxs-lookup"><span data-stu-id="a1297-113">RegisterComPlus action</span></span>](registercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="a1297-114">Tabela ComPlus</span><span class="sxs-lookup"><span data-stu-id="a1297-114">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="a1297-115">Instalando um aplicativo COM+ com o Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a1297-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



