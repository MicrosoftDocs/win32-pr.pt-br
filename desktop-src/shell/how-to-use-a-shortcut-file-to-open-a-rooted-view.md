---
description: Você pode iniciar uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho para esse ponto de junção.
title: Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9337caa955164dad36456feb7d58efd8768928429c06d22e90d9fbbf28e68bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714886"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a>Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho

Você pode iniciar uma exibição com raiz de um ponto de junção por meio de um [arquivo de atalho](./links.md) para esse ponto de junção.

## <a name="instructions"></a>Instruções


Defina a linha de destino do arquivo de atalho para Explorer.exe com um sinalizador/root. A forma exata do comando depende do local do ponto de junção:

-   Se o ponto de junção for uma subpasta da área de trabalho, use:

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   Se o ponto de junção for uma pasta do sistema de arquivos, use:

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   Se o ponto de junção for uma subpasta de uma pasta virtual do sistema, use:

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    As pastas virtuais do sistema que podem conter pontos de junção têm os seguintes identificadores de classe (CLSIDs):

    

    | Pasta do sistema     | Identificador de classe                       |
    |-------------------|----------------------------------------|
    | Meu Computador       | {20D04FE0-3AEA-1069-A2D8-08002B30309D} |
    | Meus locais de rede | {208D2C60-3AEA-1069-A2D7-08002B30309D} |
    | Painel de Controle     | {21EC2020-3AEA-1069-A2DD-08002B30309D} |
    | Internet Explorer | {871C5380-42A0-1069-A2EA-08002B30309D} |

    

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando o local de uma extensão de namespace](nse-junction.md)
</dt> <dt>

[Como abrir uma exibição com raiz de um ponto de junção no registro](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
