---
description: A ação RegisterFonts registra as fontes instaladas com o sistema. Essa ação mapeia o nome da fonte na coluna FontTitle da tabela Font para o caminho do arquivo de fonte instalado.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Ação RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747949"
---
# <a name="registerfonts-action"></a><span data-ttu-id="ab519-104">Ação RegisterFonts</span><span class="sxs-lookup"><span data-stu-id="ab519-104">RegisterFonts Action</span></span>

<span data-ttu-id="ab519-105">A ação RegisterFonts registra as fontes instaladas com o sistema.</span><span class="sxs-lookup"><span data-stu-id="ab519-105">The RegisterFonts action registers installed fonts with the system.</span></span> <span data-ttu-id="ab519-106">Essa ação mapeia o nome da fonte na coluna FontTitle da [tabela Font](font-table.md) para o caminho do arquivo de fonte instalado.</span><span class="sxs-lookup"><span data-stu-id="ab519-106">This action maps the font name in the FontTitle column of the [Font table](font-table.md) to the path of the font file installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ab519-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="ab519-107">Sequence Restrictions</span></span>

<span data-ttu-id="ab519-108">A ação [InstallFiles](installfiles-action.md) deve ser chamada antes de chamar a ação RegisterFonts.</span><span class="sxs-lookup"><span data-stu-id="ab519-108">The [InstallFiles](installfiles-action.md) action must be called before calling the RegisterFonts action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ab519-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="ab519-109">ActionData Messages</span></span>



| <span data-ttu-id="ab519-110">Campo</span><span class="sxs-lookup"><span data-stu-id="ab519-110">Field</span></span> | <span data-ttu-id="ab519-111">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="ab519-111">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="ab519-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ab519-112">\[1\]</span></span> | <span data-ttu-id="ab519-113">Arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="ab519-113">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="ab519-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab519-114">Remarks</span></span>

<span data-ttu-id="ab519-115">A ação RegisterFonts será executada se o arquivo especificado na coluna arquivo \_ da tabela de [fontes](font-table.md) pertencer a um componente que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="ab519-115">The RegisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being installed.</span></span>

 

 



