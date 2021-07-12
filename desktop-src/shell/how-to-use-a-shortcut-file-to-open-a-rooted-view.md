---
description: Você pode iniciar uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho para esse ponto de junção.
title: Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581604"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="8c809-103">Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho</span><span class="sxs-lookup"><span data-stu-id="8c809-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="8c809-104">Você pode iniciar uma exibição com raiz de um ponto de junção por meio de um [arquivo de atalho](./links.md) para esse ponto de junção.</span><span class="sxs-lookup"><span data-stu-id="8c809-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="8c809-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="8c809-105">Instructions</span></span>


<span data-ttu-id="8c809-106">Defina a linha de destino do arquivo de atalho para Explorer.exe com um sinalizador/root.</span><span class="sxs-lookup"><span data-stu-id="8c809-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="8c809-107">A forma exata do comando depende do local do ponto de junção:</span><span class="sxs-lookup"><span data-stu-id="8c809-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="8c809-108">Se o ponto de junção for uma subpasta da área de trabalho, use:</span><span class="sxs-lookup"><span data-stu-id="8c809-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="8c809-109">Se o ponto de junção for uma pasta do sistema de arquivos, use:</span><span class="sxs-lookup"><span data-stu-id="8c809-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="8c809-110">Se o ponto de junção for uma subpasta de uma pasta virtual do sistema, use:</span><span class="sxs-lookup"><span data-stu-id="8c809-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="8c809-111">As pastas virtuais do sistema que podem conter pontos de junção têm os seguintes identificadores de classe (CLSIDs):</span><span class="sxs-lookup"><span data-stu-id="8c809-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    | <span data-ttu-id="8c809-112">Pasta do sistema</span><span class="sxs-lookup"><span data-stu-id="8c809-112">System folder</span></span>     | <span data-ttu-id="8c809-113">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="8c809-113">Class identifier</span></span>                       |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="8c809-114">Meu Computador</span><span class="sxs-lookup"><span data-stu-id="8c809-114">My Computer</span></span>       | <span data-ttu-id="8c809-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="8c809-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="8c809-116">Meus locais de rede</span><span class="sxs-lookup"><span data-stu-id="8c809-116">My Network Places</span></span> | <span data-ttu-id="8c809-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="8c809-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="8c809-118">Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="8c809-118">Control Panel</span></span>     | <span data-ttu-id="8c809-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="8c809-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="8c809-120">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="8c809-120">Internet Explorer</span></span> | <span data-ttu-id="8c809-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="8c809-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="8c809-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c809-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c809-123">Especificando o local de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="8c809-123">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="8c809-124">Como abrir uma exibição com raiz de um ponto de junção no registro</span><span class="sxs-lookup"><span data-stu-id="8c809-124">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
