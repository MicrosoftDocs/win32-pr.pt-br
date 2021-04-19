---
description: A ação UnregisterFonts remove informações de registro sobre as fontes instaladas do sistema.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Ação UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812904"
---
# <a name="unregisterfonts-action"></a><span data-ttu-id="7c01b-103">Ação UnregisterFonts</span><span class="sxs-lookup"><span data-stu-id="7c01b-103">UnregisterFonts Action</span></span>

<span data-ttu-id="7c01b-104">A ação UnregisterFonts remove informações de registro sobre as fontes instaladas do sistema.</span><span class="sxs-lookup"><span data-stu-id="7c01b-104">The UnregisterFonts action removes registration information about installed fonts from the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7c01b-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="7c01b-105">Sequence Restrictions</span></span>

<span data-ttu-id="7c01b-106">A ação [RemoveFiles](removefiles-action.md) deve ser chamada após UnregisterFonts.</span><span class="sxs-lookup"><span data-stu-id="7c01b-106">The [RemoveFiles](removefiles-action.md) action must be called after UnregisterFonts.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7c01b-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="7c01b-107">ActionData Messages</span></span>



| <span data-ttu-id="7c01b-108">Campo</span><span class="sxs-lookup"><span data-stu-id="7c01b-108">Field</span></span> | <span data-ttu-id="7c01b-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="7c01b-109">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="7c01b-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7c01b-110">\[1\]</span></span> | <span data-ttu-id="7c01b-111">Arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="7c01b-111">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="7c01b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c01b-112">Remarks</span></span>

<span data-ttu-id="7c01b-113">A ação UnregisterFonts será executada se o arquivo especificado na coluna arquivo \_ da tabela de [fontes](font-table.md) pertencer a um componente que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="7c01b-113">The UnregisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being uninstalled.</span></span>

 

 



