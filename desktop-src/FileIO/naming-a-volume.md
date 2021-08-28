---
description: Um rótulo é um nome amigável atribuído a um volume, geralmente por um usuário final, para facilitar o reconhecimento. Um volume pode ter um rótulo, uma letra da unidade, ambos ou nenhum. Para definir o rótulo de um volume, use a função SetVolumeLabel.
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: Nomeando um volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc0af7575f2fd6ad2f45fc5763666151c08e10f414e1b6e6610e163c4c811cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533328"
---
# <a name="naming-a-volume"></a>Nomeando um volume

Um rótulo é um nome amigável atribuído a um volume, geralmente por um usuário final, para facilitar o reconhecimento. Um volume pode ter um rótulo, uma letra da unidade, ambos ou nenhum. Para definir o rótulo de um volume, use a [**função SetVolumeLabel.**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)

Vários fatores podem dificultar a identificação de volumes específicos usando apenas letras de unidade e rótulos. Uma delas é que um volume não precisa ter uma letra da unidade ou um rótulo. Outra é que dois volumes diferentes podem ter o mesmo rótulo, o que os torna indistinguíveis, exceto por letra da unidade. Um terceiro fator é que as atribuições de letra da unidade podem mudar conforme os volumes são adicionados e removidos do computador.

Para resolver esse problema, o sistema operacional usa caminhos *GUID de volume* para identificar volumes. Estas são cadeias de caracteres deste formulário:

"\\\\?\\ Volume{*GUID*} \\ "

em *que GUID* é um GUID (identificador global exclusivo) que identifica o volume.

Às vezes, um caminho GUID de volume é conhecido como um nome *de volume* exclusivo, porque um caminho GUID de volume pode se referir apenas a um volume. No entanto, esse termo é enganoso, porque um volume pode ter mais de um caminho guid de volume.

O \\ \\ prefixo " ? \\ " desabilita a análise de caminho e não é considerado parte do caminho. Para obter mais informações sobre o prefixo " \\ \\ ? \\ ", consulte [Nomeando um arquivo ou diretório](naming-a-file.md).

Você deve especificar caminhos completos ao usar caminhos GUID de volume com o prefixo " \\ \\ \\ ? ".

Uma *pasta montada é* uma associação entre uma pasta em um volume e outro volume, para que o caminho da pasta possa ser usado para acessar o volume. Por exemplo, se você usar a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para criar uma pasta montada que associa o volume "D: " à pasta "C: MountD", poderá usar qualquer caminho \\ \\ \\ ("D: " ou "C: MountD ") para acessar o \\ \\ volume \\ "D: \\ ".

Um *ponto de montagem de* volume é qualquer caminho de modo de usuário que pode ser usado para acessar um volume. Há três tipos de pontos de montagem de volume:

-   Uma letra da unidade, por exemplo, "C: \\ ".
-   Um caminho GUID de volume, por exemplo, " \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ ".
-   Uma pasta montada, por exemplo, "C: \\ \\ Montado".

Todas as funções de volume e pasta montada que levam um caminho GUID de volume como um parâmetro de entrada exigem a faixa invertida à frente. Todas as funções de volume e pasta montadas que retornam um caminho GUID de volume fornecem a faixa invertida à frente, mas esse não é o caso com a [**função CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Você pode abrir um volume chamando **CreateFile** e omitir a faixa invertida à parte final do nome do volume especificado. **CreateFile** processa um caminho GUID de volume com uma faixa invertida anexada como o diretório raiz do volume.

O sistema operacional atribui um caminho GUID de volume a um volume quando o volume é instalado pela primeira vez e quando o volume é formatado. As funções de volume e pasta montada usam caminhos GUID de volume para acessar volumes. Para obter o caminho do GUID de volume para um volume, use a [**função GetVolumeNameForVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)

Os comprimentos do caminho podem ser uma preocupação quando uma pasta montada é criada que associa um volume que tem uma árvore de diretório profunda a um diretório em outro volume. Isso porque o caminho do volume é concatenado ao caminho do diretório. A constante MAX PATH definida **\_ globalmente** define o número máximo de caracteres que um caminho pode ter. (Para obter mais informações sobre **MAX \_ PATH**, consulte [Nomeando um arquivo ou diretório](naming-a-file.md).) Você pode evitar essa restrição fazendo o seguinte:

-   Consulte volumes por seus caminhos guid de volume.
-   Use as versões Unicode (W) das funções de arquivo, que suportam o \\ \\ \\ prefixo ? .

 

 



