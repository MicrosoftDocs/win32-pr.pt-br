---
description: A propriedade transformações contém a lista de transformações de um pacote de instalação. O instalador aplica todas as transformações na lista transformações em cada instalação, anúncio, instalação sob demanda ou instalação de manutenção do pacote.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Aplicando transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf6c1bd60a084b745df14d89772008867b618f3b21116ca20c5313747950b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264246"
---
# <a name="applying-transforms"></a>Aplicando transformações

A propriedade [**TRANSformações**](transforms.md) contém a lista de transformações de um pacote de instalação. O instalador aplica todas as transformações na lista transformações em cada instalação, anúncio, instalação sob demanda ou instalação de manutenção do pacote.

A propriedade [**TRANSformações**](transforms.md) é definida especificando a lista de transformações na linha de comando; no entanto, ao usar a opção de [linha de comando](command-line-options.md)/JM ou/Ju, a lista transformações deve ser especificada usando a opção/t.

Observe que a lista transformações não pode ser modificada depois de instalada e só pode ser removida pela desinstalação do aplicativo.

> [!Note]  
> um pacote Windows Installer pode aplicar no máximo 255 transformações ao instalar um aplicativo ou atualizar. Quando muitas transformações são necessárias, elas devem ser combinadas e as transformações obsoletas anteriores devem ser eliminadas.

 

A tabela a seguir fornece exemplos de várias cadeias de caracteres de transformações que podem ser adicionadas à lista transformações.



| Cadeia de caracteres de transformações                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1. MST;: preform2. MST;: transform3. MST                                                                                 | O transform2. MST e o transform3. MST são [transformações incorporadas](embedded-transforms.md). o preform1. MST é uma [transformação segura no código-fonte](secure-at-source-transforms.md) somente se a propriedade [**TRANSFORMSSECURE**](transformssecure.md) ou a [política TRANSFORMSSECURE](transformssecure-policy.md) for definida; caso contrário, transform1 será uma [transformação não segura](unsecured-transforms.md). |
| \\\\caminho de compartilhamento de servidor \\ \\ \\ transform1. MST;: preform2. MST                                                                        | O transform2. MST é uma [transformação inserida](embedded-transforms.md). o transform1. MST é uma [transformação de caminho completo seguro](secure-full-path-transforms.md) somente se a propriedade [**TRANSFORMSSECURE**](transformssecure.md) ou a [política TRANSFORMSSECURE](transformssecure-policy.md) estiver definida; caso contrário, transform1 será uma [transformação não segura](unsecured-transforms.md).                   |
| @: exform2. MST; transform1. MST @transform1.mst ;: preform2. MST<br/>                                                     | O transform2. MST é uma transformação inserida. o preform1. MST é uma [transformações seguras de origem](secure-at-source-transforms.md)autônoma.                                                                                                                                                                                                                                                |
| \|\\\\caminho de compartilhamento de servidor \\ \\ \\ transform1. MST;: preform2. MST \| : transform2. MST; \\ \\ caminho de compartilhamento de servidor \\ \\ \\ transform1. MST<br/> | O transform2. MST é uma transformação inserida. o preform1. MST é uma [transformações de caminho completo e seguro](secure-full-path-transforms.md)autônomo.                                                                                                                                                                                                                                                 |



 

 

 




