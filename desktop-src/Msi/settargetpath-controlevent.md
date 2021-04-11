---
description: O evento SetTargetPath notifica o instalador para verificar e definir o caminho selecionado. Se o caminho não for válido para gravação, o instalador bloqueará ControlEvents adicionais associados ao controle.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170421"
---
# <a name="settargetpath-controlevent"></a><span data-ttu-id="2ce3c-104">SetTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="2ce3c-104">SetTargetPath ControlEvent</span></span>

<span data-ttu-id="2ce3c-105">O evento SetTargetPath notifica o instalador para verificar e definir o caminho selecionado.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-105">The SetTargetPath event notifies the installer to check and set the selected path.</span></span> <span data-ttu-id="2ce3c-106">Se o caminho não for válido para gravação, o instalador bloqueará ControlEvents adicionais associados ao controle.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-106">If the path is not valid to be written to, then the installer blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="2ce3c-107">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="2ce3c-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="2ce3c-108">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ce3c-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="2ce3c-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2ce3c-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2ce3c-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2ce3c-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2ce3c-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="2ce3c-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="2ce3c-112">Published By</span></span>

<span data-ttu-id="2ce3c-113">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="2ce3c-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="2ce3c-114">Argument</span></span>

<span data-ttu-id="2ce3c-115">O nome da propriedade que contém o caminho.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-115">The name of the property containing the path.</span></span> <span data-ttu-id="2ce3c-116">Se a propriedade for indireta, o nome da propriedade será colocado entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2ce3c-117">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="2ce3c-117">Action on Subscribers</span></span>

<span data-ttu-id="2ce3c-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2ce3c-119">Usos comum</span><span class="sxs-lookup"><span data-stu-id="2ce3c-119">Typical Use</span></span>

<span data-ttu-id="2ce3c-120">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo de procura está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para verificar o caminho selecionado antes de retornar à caixa de diálogo de seleção.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce3c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ce3c-121">Remarks</span></span>

<span data-ttu-id="2ce3c-122">Não tente configurar o caminho de destino se os componentes que usam esses caminhos já estiverem instalados para o usuário atual ou para um usuário diferente.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-122">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="2ce3c-123">Verifique a propriedade [**productstate**](productstate.md) antes de publicar o SetTargetPath ControlEvent, para determinar se o produto que contém o componente está instalado.</span><span class="sxs-lookup"><span data-stu-id="2ce3c-123">Check the [**ProductState**](productstate.md) property before publishing the SetTargetPath ControlEvent to determine if the product containing the component is installed.</span></span>

 

 



