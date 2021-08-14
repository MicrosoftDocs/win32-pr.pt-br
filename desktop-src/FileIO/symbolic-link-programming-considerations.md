---
description: Considerações sobre programação para trabalhar com links simbólicos.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considerações sobre programação (sistemas de arquivos locais)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a98c244dac3fb4a9f6b73d11067af64512e0cfd54e58078bd87a2582b0c2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981876"
---
# <a name="programming-considerations-local-file-systems"></a>Considerações sobre programação (sistemas de arquivos locais)

Lembre-se das seguintes considerações de programação ao trabalhar com links simbólicos:

-   Links simbólicos podem apontar para um destino inexistente.
-   Ao criar um link simbólico, o sistema operacional não verifica se o destino existe.
-   Se um aplicativo tentar abrir um destino inexistente, **ERROR \_ FILE NOT \_ \_ FOUND** será retornado.
-   Links simbólicos são pontos de reparse. Para obter mais informações, [consulte Determinando se um diretório é uma pasta montada.](determining-whether-a-directory-is-a-volume-mount-point.md)
-   Há um máximo de 63 pontos de novaparação (e, portanto, links simbólicos) permitidos em um caminho específico.

    **Windows Server 2003 e Windows XP:** Há um limite de 31 pontos de nova esparsa em qualquer caminho determinado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[Links rígidos e junções](hard-links-and-junctions.md)
</dt> </dl>

 

 



