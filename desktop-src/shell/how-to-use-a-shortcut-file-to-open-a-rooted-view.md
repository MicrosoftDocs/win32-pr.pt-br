---
description: Você pode iniciar uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho para esse ponto de junção.
title: Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb83a6628b0dcffdf7d3bad66a25fc671c1feea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169424"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="f2441-103">Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho</span><span class="sxs-lookup"><span data-stu-id="f2441-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="f2441-104">Você pode iniciar uma exibição com raiz de um ponto de junção por meio de um [arquivo de atalho](./links.md) para esse ponto de junção.</span><span class="sxs-lookup"><span data-stu-id="f2441-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="f2441-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="f2441-105">Instructions</span></span>


<span data-ttu-id="f2441-106">Defina a linha de destino do arquivo de atalho para Explorer.exe com um sinalizador/root.</span><span class="sxs-lookup"><span data-stu-id="f2441-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="f2441-107">A forma exata do comando depende do local do ponto de junção:</span><span class="sxs-lookup"><span data-stu-id="f2441-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="f2441-108">Se o ponto de junção for uma subpasta da área de trabalho, use:</span><span class="sxs-lookup"><span data-stu-id="f2441-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="f2441-109">Se o ponto de junção for uma pasta do sistema de arquivos, use:</span><span class="sxs-lookup"><span data-stu-id="f2441-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="f2441-110">Se o ponto de junção for uma subpasta de uma pasta virtual do sistema, use:</span><span class="sxs-lookup"><span data-stu-id="f2441-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="f2441-111">As pastas virtuais do sistema que podem conter pontos de junção têm os seguintes identificadores de classe (CLSIDs):</span><span class="sxs-lookup"><span data-stu-id="f2441-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    |                   |                                        |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="f2441-112">Meu Computador</span><span class="sxs-lookup"><span data-stu-id="f2441-112">My Computer</span></span>       | <span data-ttu-id="f2441-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="f2441-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="f2441-114">Meus locais de rede</span><span class="sxs-lookup"><span data-stu-id="f2441-114">My Network Places</span></span> | <span data-ttu-id="f2441-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="f2441-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="f2441-116">Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="f2441-116">Control Panel</span></span>     | <span data-ttu-id="f2441-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="f2441-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="f2441-118">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f2441-118">Internet Explorer</span></span> | <span data-ttu-id="f2441-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="f2441-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="f2441-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2441-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2441-121">Especificando o local de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="f2441-121">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="f2441-122">Como abrir uma exibição com raiz de um ponto de junção no registro</span><span class="sxs-lookup"><span data-stu-id="f2441-122">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
