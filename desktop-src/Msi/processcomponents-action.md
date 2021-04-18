---
description: A ação ProcessComponents registra e cancela o registro de componentes, seus caminhos de chave e os clientes de componente.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Ação ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752636"
---
# <a name="processcomponents-action"></a><span data-ttu-id="80ceb-103">Ação ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="80ceb-103">ProcessComponents Action</span></span>

<span data-ttu-id="80ceb-104">A ação ProcessComponents registra e cancela o registro de componentes, seus caminhos de chave e os clientes de componente.</span><span class="sxs-lookup"><span data-stu-id="80ceb-104">The ProcessComponents action registers and unregisters components, their key paths, and the component clients.</span></span> <span data-ttu-id="80ceb-105">A ação ProcessComponents consulta a coluna KeyPath da [tabela de componentes](component-table.md) para determinar os caminhos.</span><span class="sxs-lookup"><span data-stu-id="80ceb-105">The ProcessComponents action queries the KeyPath column of the [Component table](component-table.md) to determine keypaths.</span></span> <span data-ttu-id="80ceb-106">Esse registro é usado pelo [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para retornar o caminho de um componente para um cliente de produto.</span><span class="sxs-lookup"><span data-stu-id="80ceb-106">This registration is used by [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to return the path of a component for a product client.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="80ceb-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="80ceb-107">Sequence Restrictions</span></span>

<span data-ttu-id="80ceb-108">A ação ProcessComponents deve vir após a ação [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="80ceb-108">The ProcessComponents action must come after the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="80ceb-109">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="80ceb-109">ActionData Messages</span></span>

<span data-ttu-id="80ceb-110">Para cada componente que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="80ceb-110">For each component being registered.</span></span>



| <span data-ttu-id="80ceb-111">Campo</span><span class="sxs-lookup"><span data-stu-id="80ceb-111">Field</span></span> | <span data-ttu-id="80ceb-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="80ceb-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="80ceb-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="80ceb-113">\[1\]</span></span> | <span data-ttu-id="80ceb-114">ProductId</span><span class="sxs-lookup"><span data-stu-id="80ceb-114">ProductId</span></span>                       |
| <span data-ttu-id="80ceb-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="80ceb-115">\[2\]</span></span> | <span data-ttu-id="80ceb-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="80ceb-116">ComponentId</span></span>                     |
| <span data-ttu-id="80ceb-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="80ceb-117">\[3\]</span></span> | <span data-ttu-id="80ceb-118">O caminho da chave para o componente.</span><span class="sxs-lookup"><span data-stu-id="80ceb-118">The key path for the component.</span></span> |



 

<span data-ttu-id="80ceb-119">Para cada componente que está sendo cancelado.</span><span class="sxs-lookup"><span data-stu-id="80ceb-119">For each component being unregistered.</span></span>



| <span data-ttu-id="80ceb-120">Campo</span><span class="sxs-lookup"><span data-stu-id="80ceb-120">Field</span></span> | <span data-ttu-id="80ceb-121">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="80ceb-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="80ceb-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="80ceb-122">\[1\]</span></span> | <span data-ttu-id="80ceb-123">ProductId</span><span class="sxs-lookup"><span data-stu-id="80ceb-123">ProductId</span></span>                  |
| <span data-ttu-id="80ceb-124">\[2\]</span><span class="sxs-lookup"><span data-stu-id="80ceb-124">\[2\]</span></span> | <span data-ttu-id="80ceb-125">ComponentId</span><span class="sxs-lookup"><span data-stu-id="80ceb-125">ComponentId</span></span>                |



 

 

 



