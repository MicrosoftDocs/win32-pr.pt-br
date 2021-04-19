---
description: Use as diretrizes a seguir para criar um Windows Installer instalação que exibe uma caixa de mensagem solicitando que o usuário insira um disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Criando mensagens de prompt de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747989"
---
# <a name="authoring-disk-prompt-messages"></a><span data-ttu-id="ad40c-103">Criando mensagens de prompt de disco</span><span class="sxs-lookup"><span data-stu-id="ad40c-103">Authoring Disk Prompt Messages</span></span>

<span data-ttu-id="ad40c-104">Use as diretrizes a seguir para criar um Windows Installer instalação que exibe uma caixa de mensagem solicitando que o usuário insira um disco.</span><span class="sxs-lookup"><span data-stu-id="ad40c-104">Use the following guidelines to author a Windows Installer installation that displays a message box prompting the user to insert a disk.</span></span>

<span data-ttu-id="ad40c-105">**Para exibir uma caixa de mensagem solicitando que o usuário insira um disco**</span><span class="sxs-lookup"><span data-stu-id="ad40c-105">**To display a message box prompting the user to insert a disk**</span></span>

1.  <span data-ttu-id="ad40c-106">Use os recursos de criação do instalador para definir a cadeia de caracteres da propriedade [**DiskPrompt**](diskprompt.md) na tabela de [Propriedades](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ad40c-106">Use the authoring capabilities of the installer to set the [**DiskPrompt**](diskprompt.md) property string in the [Property](property-table.md) table.</span></span> <span data-ttu-id="ad40c-107">Isso deve incluir o nome do produto que está sendo instalado e um parâmetro de espaço reservado na cadeia de caracteres para o título impresso no disco.</span><span class="sxs-lookup"><span data-stu-id="ad40c-107">This should include the name of the product being installed and a placeholder parameter within the string for the title printed on the disk.</span></span> <span data-ttu-id="ad40c-108">Por exemplo, para o Microsoft Publisher, a propriedade **DiskPrompt** poderia ser "Microsoft Publisher: disco \[ 1 \] ", em que \[ 1 \] é o espaço reservado para o título do disco.</span><span class="sxs-lookup"><span data-stu-id="ad40c-108">For example, for Microsoft Publisher the **DiskPrompt** property could be "Microsoft Publisher: Disk \[1\]", where \[1\] is the placeholder for the disk title.</span></span>
2.  <span data-ttu-id="ad40c-109">Insira os títulos de cada um dos discos que estão sendo solicitados em linhas separadas da coluna DiskPrompt da tabela de [mídia](media-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ad40c-109">Enter the titles of each of the disks being prompted for into separate rows of the DiskPrompt column of the [Media](media-table.md) table.</span></span> <span data-ttu-id="ad40c-110">Por exemplo, a primeira e única entrada na tabela de mídia poderia ser "1 – instalar".</span><span class="sxs-lookup"><span data-stu-id="ad40c-110">For example, the first and only entry into the Media table could be "1–Install."</span></span>
3.  <span data-ttu-id="ad40c-111">Durante a ação [InstallFiles](installfiles-action.md) , o valor da coluna DiskPrompt da tabela de [mídia](media-table.md) é substituído pelo espaço reservado na cadeia de caracteres da propriedade [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="ad40c-111">During the [InstallFiles](installfiles-action.md) action the value from the DiskPrompt column of the [Media](media-table.md) table is substituted for the placeholder in the string of the [**DiskPrompt**](diskprompt.md) property.</span></span>
4.  <span data-ttu-id="ad40c-112">A mensagem exibida pela caixa de mensagem é criada a partir de uma cadeia de caracteres de modelo interna na [tabela de erros](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="ad40c-112">The message displayed by the message box is created from a built-in template string in the [Error table](error-table.md).</span></span> <span data-ttu-id="ad40c-113">Esse é o erro 1302 e a cadeia de caracteres do modelo é: "Insira o disco: \[ 2 \] " e o \[ 2 \] representa um espaço reservado para a propriedade [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="ad40c-113">This is Error 1302 and the template string is: "Please insert the disk: \[2\]", and the \[2\] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.</span></span>

<span data-ttu-id="ad40c-114">O exemplo exibe a seguinte mensagem para o usuário: "Insira o disco: Microsoft Publisher: disco 1 – instalar."</span><span class="sxs-lookup"><span data-stu-id="ad40c-114">The example displays the following message to the user: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."</span></span>

<span data-ttu-id="ad40c-115">Observe que as mensagens de prompt de disco são exibidas por todos os [níveis de interface do usuário](user-interface-levels.md) , exceto nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ad40c-115">Note that disk prompt messages get displayed by all [User Interface Levels](user-interface-levels.md) except None.</span></span>

 

 



