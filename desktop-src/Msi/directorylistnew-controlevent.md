---
description: Esse evento notifica o controle Directorylist que uma nova pasta deve ser criada; Ele cria a nova pasta e seleciona o campo nome da pasta para edição.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768470"
---
# <a name="directorylistnew-controlevent"></a><span data-ttu-id="2b4d7-103">DirectoryListNew ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="2b4d7-103">DirectoryListNew ControlEvent</span></span>

<span data-ttu-id="2b4d7-104">Esse evento notifica o [controle directorylist](directorylist-control.md) que uma nova pasta deve ser criada; Ele cria a nova pasta e seleciona o campo nome da pasta para edição.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-104">This event notifies the [DirectoryList control](directorylist-control.md) that a new folder must be created; it creates the new folder, and selects the name field of the folder for editing.</span></span> <span data-ttu-id="2b4d7-105">O nome padrão da nova pasta pode ser criado na [tabela UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b4d7-105">The default name of the new folder may be authored in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="2b4d7-106">Insira "NewFolder" na coluna de chave.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-106">Enter "NewFolder" into the Key column.</span></span> <span data-ttu-id="2b4d7-107">Insira o valor para o nome padrão da nova pasta na coluna de texto.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-107">Enter the value for the default name of the new folder into the Text column.</span></span> <span data-ttu-id="2b4d7-108">Esse valor deve estar na forma de um tipo de dados de coluna de [nome de arquivo](filename.md) e usar a \| sintaxe SFN LFN.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-108">This value must be in the form of a [Filename](filename.md) column data type and use the SFN\|LFN syntax.</span></span> <span data-ttu-id="2b4d7-109">Se esse valor não estiver presente na tabela UIText ou for um valor inválido, o instalador usará um valor padrão de "Fldr \| nova pasta".</span><span class="sxs-lookup"><span data-stu-id="2b4d7-109">If this value is not present in the UIText table or is an invalid value, the installer uses a default value of "Fldr\|New Folder."</span></span> <span data-ttu-id="2b4d7-110">Para obter informações relacionadas, consulte [caixa de diálogo Procurar](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="2b4d7-110">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="2b4d7-111">Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-111">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="2b4d7-112">O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b4d7-112">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="2b4d7-113">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-113">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2b4d7-114">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2b4d7-114">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2b4d7-115">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2b4d7-115">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="2b4d7-116">Observe que, se esse ControlEvent, for chamado novamente quando uma nova pasta já existir, uma segunda pasta nova não será criada.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-116">Note that if this ControlEvent is called again when a new folder already exists, a second new folder will not be created.</span></span> <span data-ttu-id="2b4d7-117">Nesse caso, chamar DirectoryListNew seleciona o nome da nova pasta existente para edição.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-117">In this case, calling DirectoryListNew selects the existing new folder's name for editing.</span></span>

## <a name="published-by"></a><span data-ttu-id="2b4d7-118">Publicada por</span><span class="sxs-lookup"><span data-stu-id="2b4d7-118">Published By</span></span>

[<span data-ttu-id="2b4d7-119">Directorylist</span><span class="sxs-lookup"><span data-stu-id="2b4d7-119">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="2b4d7-120">Argumento</span><span class="sxs-lookup"><span data-stu-id="2b4d7-120">Argument</span></span>

<span data-ttu-id="2b4d7-121">Este ControlEvent, não usa um argumento.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-121">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2b4d7-122">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="2b4d7-122">Action on Subscribers</span></span>

<span data-ttu-id="2b4d7-123">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-123">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2b4d7-124">Usos comum</span><span class="sxs-lookup"><span data-stu-id="2b4d7-124">Typical Use</span></span>

<span data-ttu-id="2b4d7-125">Um controle de [supressão](pushbutton-control.md) na mesma caixa de diálogo modal que a directorylist é usado para disparar a criação de uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="2b4d7-125">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger the creation of a new folder.</span></span>

 

 



