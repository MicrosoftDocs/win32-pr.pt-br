---
description: O IgnoreChange ControlEvent, é publicado pelo controle Directorylist quando a pasta selecionada é alterada de um diretório para outro no controle. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751653"
---
# <a name="ignorechange-controlevent"></a><span data-ttu-id="edab8-104">IgnoreChange ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="edab8-104">IgnoreChange ControlEvent</span></span>

<span data-ttu-id="edab8-105">O IgnoreChange ControlEvent, é publicado pelo [controle directorylist](directorylist-control.md) quando a pasta selecionada é alterada de um diretório para outro no controle.</span><span class="sxs-lookup"><span data-stu-id="edab8-105">The IgnoreChange ControlEvent is published by the [DirectoryList control](directorylist-control.md) when the selected folder is changed from one directory to another directory in the control.</span></span> <span data-ttu-id="edab8-106">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="edab8-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="edab8-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="edab8-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="edab8-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="edab8-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="edab8-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="edab8-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="edab8-110">Publicada por</span><span class="sxs-lookup"><span data-stu-id="edab8-110">Published By</span></span>

[<span data-ttu-id="edab8-111">Directorylist</span><span class="sxs-lookup"><span data-stu-id="edab8-111">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="edab8-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="edab8-112">Argument</span></span>

<span data-ttu-id="edab8-113">Este ControlEvent, não usa um argumento.</span><span class="sxs-lookup"><span data-stu-id="edab8-113">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="edab8-114">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="edab8-114">Action on Subscribers</span></span>

<span data-ttu-id="edab8-115">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="edab8-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="edab8-116">Usos comum</span><span class="sxs-lookup"><span data-stu-id="edab8-116">Typical Use</span></span>

<span data-ttu-id="edab8-117">O [controle DirectoryCombo](directorycombo-control.md) normalmente emprega o IgnoreChange ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="edab8-117">The [DirectoryCombo control](directorycombo-control.md) commonly employs the IgnoreChange ControlEvent.</span></span>

 

 



