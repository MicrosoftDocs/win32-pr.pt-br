---
description: Uma caixa de diálogo de procura permite que o usuário selecione um diretório. O diretório não precisa existir e pode ser criado usando esse controle.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Procurar caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370695"
---
# <a name="browse-dialog"></a><span data-ttu-id="2e136-104">Procurar caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="2e136-104">Browse Dialog</span></span>

<span data-ttu-id="2e136-105">Uma caixa de diálogo de procura permite que o usuário selecione um diretório.</span><span class="sxs-lookup"><span data-stu-id="2e136-105">A Browse dialog box enables the user to select a directory.</span></span> <span data-ttu-id="2e136-106">O diretório não precisa existir e pode ser criado usando esse controle.</span><span class="sxs-lookup"><span data-stu-id="2e136-106">The directory does not have to exist and may be created by using this control.</span></span>

<span data-ttu-id="2e136-107">Esse tipo de caixa de diálogo normalmente contém os três controles a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e136-107">This type of dialog box commonly contains the following three controls.</span></span> <span data-ttu-id="2e136-108">Esses controles são conectados à mesma propriedade.</span><span class="sxs-lookup"><span data-stu-id="2e136-108">These controls are connected to the same property.</span></span> <span data-ttu-id="2e136-109">Essa propriedade é o caminho que está sendo selecionado.</span><span class="sxs-lookup"><span data-stu-id="2e136-109">That property is the path being selected.</span></span>

-   <span data-ttu-id="2e136-110">Um [controle PathEdit](pathedit-control.md) para selecionar a seção final do caminho.</span><span class="sxs-lookup"><span data-stu-id="2e136-110">A [PathEdit control](pathedit-control.md) to select the tail section of the path.</span></span> <span data-ttu-id="2e136-111">Esse controle não pode perder o foco se a parte final inserida não for válida no volume atual.</span><span class="sxs-lookup"><span data-stu-id="2e136-111">This control cannot lose focus if the entered tail is not valid on the present volume.</span></span>
-   <span data-ttu-id="2e136-112">Um [controle DirectoryCombo](directorycombo-control.md) para mostrar o caminho selecionado no momento que é exibido pelo controle PathEdit.</span><span class="sxs-lookup"><span data-stu-id="2e136-112">A [DirectoryCombo control](directorycombo-control.md) to show the presently selected path that is displayed by the PathEdit control.</span></span> <span data-ttu-id="2e136-113">Esse controle não mostra o último segmento do caminho.</span><span class="sxs-lookup"><span data-stu-id="2e136-113">This control does not show the last segment of the path.</span></span>
-   <span data-ttu-id="2e136-114">Um [controle directorylist](directorylist-control.md) para mostrar as pastas abaixo do diretório exibido atualmente pelo DirectoryCombo.</span><span class="sxs-lookup"><span data-stu-id="2e136-114">A [DirectoryList control](directorylist-control.md) to show the folders below the directory currently displayed by the DirectoryCombo.</span></span> <span data-ttu-id="2e136-115">Isso também pode mostrar uma pasta que ainda não foi criada.</span><span class="sxs-lookup"><span data-stu-id="2e136-115">This can also show a folder that is not yet created.</span></span>

<span data-ttu-id="2e136-116">Uma caixa de diálogo de procura geralmente contém um [controle DirectoryCombo](directorycombo-control.md) que especifica os tipos de volume a serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="2e136-116">A Browse dialog box also usually contains a [DirectoryCombo control](directorycombo-control.md) that specifies the volume types to display.</span></span> <span data-ttu-id="2e136-117">É comum que todos os tipos de volumes sejam exibidos em uma caixa de diálogo de procura.</span><span class="sxs-lookup"><span data-stu-id="2e136-117">It is common for all volume types to be displayed on a Browse dialog box.</span></span>

<span data-ttu-id="2e136-118">As caixas de diálogo de procura normalmente contêm três [controles de pressão](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="2e136-118">Browse dialog boxes commonly contain three [PushButton controls](pushbutton-control.md).</span></span> <span data-ttu-id="2e136-119">Esses botões estão vinculados a seus respectivos ControlEvents na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="2e136-119">These buttons are linked to their respective ControlEvents in [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="2e136-120">Esses botões são usados para ativar as opções de controle a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e136-120">These buttons are used for activating the following control options.</span></span>



| <span data-ttu-id="2e136-121">Opção de controle</span><span class="sxs-lookup"><span data-stu-id="2e136-121">Control option</span></span> | <span data-ttu-id="2e136-122">ControlEvent</span><span class="sxs-lookup"><span data-stu-id="2e136-122">ControlEvent</span></span>                                            |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="2e136-123">Um nível acima</span><span class="sxs-lookup"><span data-stu-id="2e136-123">Up One Level</span></span>   | [<span data-ttu-id="2e136-124">DirectoryListUp</span><span class="sxs-lookup"><span data-stu-id="2e136-124">DirectoryListUp</span></span>](directorylistup-controlevent.md)     |
| <span data-ttu-id="2e136-125">Nova Pasta</span><span class="sxs-lookup"><span data-stu-id="2e136-125">New Folder</span></span>     | [<span data-ttu-id="2e136-126">DirectoryListNew</span><span class="sxs-lookup"><span data-stu-id="2e136-126">DirectoryListNew</span></span>](directorylistnew-controlevent.md)   |
| <span data-ttu-id="2e136-127">Aberto</span><span class="sxs-lookup"><span data-stu-id="2e136-127">Open</span></span>           | [<span data-ttu-id="2e136-128">DirectoryListOpen</span><span class="sxs-lookup"><span data-stu-id="2e136-128">DirectoryListOpen</span></span>](directorylistopen-controlevent.md) |



 

<span data-ttu-id="2e136-129">Para que a nova opção de pasta funcione com um nome de pasta não padrão, o caminho da nova pasta deve ser especificado na [tabela UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="2e136-129">For the New Folder option to work with a non-default folder name, the new folder's path must be specified in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="2e136-130">A cadeia de caracteres de caminho deve usar o formulário "nome de arquivo longo do nome de arquivo curto \| " para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2e136-130">The path string should use the "short file name\|long file name" form for the file name.</span></span> <span data-ttu-id="2e136-131">Por exemplo, use um nome de arquivo como "myprod ~ 1 \| meu produto fabuloso".</span><span class="sxs-lookup"><span data-stu-id="2e136-131">For example, use a file name such as "MyProd~1\|My Fabulous Product".</span></span> <span data-ttu-id="2e136-132">Confira o tipo de dados coluna de [nome](filename.md) de arquivo para obter mais informações sobre o formato de nome.</span><span class="sxs-lookup"><span data-stu-id="2e136-132">See the [Filename](filename.md) column data type for more information about the file name format.</span></span> <span data-ttu-id="2e136-133">Se o caminho não estiver presente na tabela UIText ou se estiver definido como um valor inválido, ele será definido como um valor de "Fldr \| nova pasta" por padrão.</span><span class="sxs-lookup"><span data-stu-id="2e136-133">If the path is not present in the UIText table, or if it is set to an invalid value, then it is set to a value of "Fldr\|New Folder" by default.</span></span> <span data-ttu-id="2e136-134">O botão **nova pasta** pode ser omitido se a caixa de diálogo precisar apenas pesquisar pastas existentes.</span><span class="sxs-lookup"><span data-stu-id="2e136-134">The **New Folder** button can be omitted if the dialog box only need to search for existing folders.</span></span>

 

 



