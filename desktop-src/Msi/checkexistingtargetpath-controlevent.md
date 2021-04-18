---
description: Esse evento notifica o instalador que ele precisa verificar se o caminho selecionado é gravável. Se o caminho não puder ser gravado, o evento bloqueará ControlEvents adicionais associados ao controle.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1117de57c5474d196da1f40da6fda3cce60b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751449"
---
# <a name="checkexistingtargetpath-controlevent"></a><span data-ttu-id="965a3-104">CheckExistingTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="965a3-104">CheckExistingTargetPath ControlEvent</span></span>

<span data-ttu-id="965a3-105">Esse evento notifica o instalador que ele precisa verificar se o caminho selecionado é gravável.</span><span class="sxs-lookup"><span data-stu-id="965a3-105">This event notifies the installer that it has to verify that the selected path is writable.</span></span> <span data-ttu-id="965a3-106">Se o caminho não puder ser gravado, o evento bloqueará ControlEvents adicionais associados ao controle.</span><span class="sxs-lookup"><span data-stu-id="965a3-106">If the path is cannot be written, then the event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="965a3-107">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="965a3-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="965a3-108">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="965a3-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="965a3-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="965a3-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="965a3-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="965a3-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="965a3-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="965a3-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="965a3-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="965a3-112">Published By</span></span>

<span data-ttu-id="965a3-113">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="965a3-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="965a3-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="965a3-114">Argument</span></span>

<span data-ttu-id="965a3-115">O nome da propriedade que contém o caminho.</span><span class="sxs-lookup"><span data-stu-id="965a3-115">The name of the property containing the path.</span></span> <span data-ttu-id="965a3-116">Se a propriedade for indireta, o nome da propriedade será colocado entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="965a3-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="965a3-117">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="965a3-117">Action on Subscribers</span></span>

<span data-ttu-id="965a3-118">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="965a3-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="965a3-119">Usos comum</span><span class="sxs-lookup"><span data-stu-id="965a3-119">Typical Use</span></span>

<span data-ttu-id="965a3-120">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo de procura está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para verificar o caminho selecionado antes de retornar à caixa de diálogo de seleção.</span><span class="sxs-lookup"><span data-stu-id="965a3-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

 

 



