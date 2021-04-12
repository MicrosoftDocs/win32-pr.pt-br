---
description: O controle SelectionTree usa o evento SelectionBrowse para gerar uma caixa de diálogo de procura, tornando possível modificar o caminho do item realçado.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297694"
---
# <a name="selectionbrowse-controlevent"></a><span data-ttu-id="97773-103">SelectionBrowse ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="97773-103">SelectionBrowse ControlEvent</span></span>

<span data-ttu-id="97773-104">O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionBrowse para gerar uma caixa de diálogo de **procura** , tornando possível modificar o caminho do item realçado.</span><span class="sxs-lookup"><span data-stu-id="97773-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionBrowse event to spawn a **Browse** dialog box making it possible to modify the path of the highlighted item.</span></span>

<span data-ttu-id="97773-105">Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento.</span><span class="sxs-lookup"><span data-stu-id="97773-105">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="97773-106">O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="97773-106">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="97773-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="97773-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="97773-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="97773-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="97773-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="97773-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="97773-110">Todos os controles que publicarem um evento SelectionBrowse serão desabilitados se um recurso tiver sido selecionado e já estiver instalado, não configurável ou não estiver selecionado para instalação local.</span><span class="sxs-lookup"><span data-stu-id="97773-110">Any controls that publish a SelectionBrowse event become disabled if a feature has been selected that is already installed, not configurable, or not selected for local installation.</span></span> <span data-ttu-id="97773-111">Para ser configurável, o recurso deve ter uma [propriedade pública](public-properties.md) inserida no \_ campo diretório da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="97773-111">To be configurable, the feature must have a [public property](public-properties.md) entered in the Directory\_ field of the [Feature table](feature-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="97773-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="97773-112">Published By</span></span>

[<span data-ttu-id="97773-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="97773-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="97773-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="97773-114">Argument</span></span>

<span data-ttu-id="97773-115">O nome da caixa de diálogo a ser gerada.</span><span class="sxs-lookup"><span data-stu-id="97773-115">The name of the dialog to be spawned.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="97773-116">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="97773-116">Action on Subscribers</span></span>

<span data-ttu-id="97773-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="97773-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="97773-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="97773-118">Typical Use</span></span>

<span data-ttu-id="97773-119">Um controle de [pressão](pushbutton-control.md) na mesma caixa de diálogo modal que o SelectionTree usa esse evento para disparar a caixa de diálogo **procurar** .</span><span class="sxs-lookup"><span data-stu-id="97773-119">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the SelectionTree uses this event to trigger the **Browse** dialog box.</span></span>

 

 



