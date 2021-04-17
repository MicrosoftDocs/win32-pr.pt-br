---
description: Considerações sobre programação para trabalhar com links simbólicos.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considerações sobre programação (sistemas de arquivos locais)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "105775749"
---
# <a name="programming-considerations-local-file-systems"></a>Considerações sobre programação (sistemas de arquivos locais)

Lembre-se das seguintes considerações de programação ao trabalhar com links simbólicos:

-   Links simbólicos podem apontar para um destino não existente.
-   Ao criar um link simbólico, o sistema operacional não verifica se o destino existe.
-   Se um aplicativo tentar abrir um destino não existente, o **arquivo de \_ erro \_ não \_ encontrado** será retornado.
-   Links simbólicos são pontos de nova análise. Para obter mais informações, consulte [determinando se um diretório é uma pasta montada](determining-whether-a-directory-is-a-volume-mount-point.md).
-   Há um máximo de 63 pontos de nova análise (e, portanto, links simbólicos) permitidos em um caminho específico.

    **Windows Server 2003 e Windows XP:** Há um limite de 31 pontos de nova análise em qualquer caminho especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[Links físicos e junções](hard-links-and-junctions.md)
</dt> </dl>

 

 



