---
description: Um rótulo é um nome amigável que é atribuído a um volume, geralmente por um usuário final, para facilitar o reconhecimento. Um volume pode ter um rótulo, uma letra da unidade, ambos ou nenhum. Para definir o rótulo de um volume, use a função SetVolumeLabel.
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: Nomeando um volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6435b6b5c7283cf2fb9a98951698f79646dfdffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829487"
---
# <a name="naming-a-volume"></a>Nomeando um volume

Um rótulo é um nome amigável que é atribuído a um volume, geralmente por um usuário final, para facilitar o reconhecimento. Um volume pode ter um rótulo, uma letra da unidade, ambos ou nenhum. Para definir o rótulo de um volume, use a função [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .

Vários fatores podem dificultar a identificação de volumes específicos usando apenas letras e rótulos de unidade. Um deles é que um volume não precisa ter uma letra de unidade ou um rótulo. Outro é que dois volumes diferentes podem ter o mesmo rótulo, o que os torna indistinguíveis, exceto por letra da unidade. Um terceiro fator é que as atribuições de letra da unidade podem ser alteradas à medida que os volumes são adicionados e removidos do computador.

Para resolver esse problema, o sistema operacional usa *caminhos GUID de volume* para identificar volumes. Estas são cadeias de caracteres deste formulário:

"\\\\?\\ Volume {*GUID*} \\ "

em que *GUID* é um GUID (identificador global exclusivo) que identifica o volume.

Um caminho de GUID de volume, às vezes, é chamado de *nome de volume exclusivo*, porque um caminho de GUID de volume só pode se referir a um volume. No entanto, esse termo é enganoso, pois um volume pode ter mais de um caminho de GUID de volume.

O \\ \\ prefixo "? \\ " desabilita a análise de caminho e não é considerado parte do caminho. Para obter mais informações sobre o \\ \\ prefixo "? \\ ", consulte [nomeando um arquivo ou diretório](naming-a-file.md).

Você deve especificar caminhos completos ao usar caminhos de GUID de volume com o \\ \\ prefixo "? \\ ".

Uma *pasta montada* é uma associação entre uma pasta em um volume e outro volume, para que o caminho da pasta possa ser usado para acessar o volume. Por exemplo, se você usar a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para criar uma pasta montada que associa o volume "d: \\ " à pasta "c: \\ montado \\ ", você poderá usar qualquer um dos dois caminhos ("d: \\ " ou "c: \\ montado \\ ") para acessar o volume "D: \\ ".

Um *ponto de montagem de volume* é qualquer caminho de modo de usuário que possa ser usado para acessar um volume. Há três tipos de pontos de montagem de volume:

-   Uma letra da unidade, por exemplo, "C: \\ ".
-   Um caminho de GUID de volume, por exemplo, " \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ ".
-   Uma pasta montada, por exemplo, "C: \\ montado \\ ".

Todas as funções de volume e pasta montadas que usam um caminho de GUID de volume como um parâmetro de entrada exigem a barra invertida à direita. Todas as funções de volume e pasta montadas que retornam um caminho de GUID de volume fornecem a barra invertida à direita, mas esse não é o caso com a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Você pode abrir um volume chamando **CreateFile** e omitir a barra invertida à direita do nome do volume que você especificar. **CreateFile** processa um caminho de GUID de volume com uma barra invertida anexada como o diretório raiz do volume.

O sistema operacional atribui um caminho de GUID de volume a um volume quando o volume é instalado pela primeira vez e quando o volume é formatado. O volume e as funções de pasta montadas usam caminhos GUID de volume para acessar volumes. Para obter o caminho do GUID do volume para um volume, use a função [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

Os comprimentos de caminho podem ser uma preocupação quando uma pasta montada é criada que associa um volume que tem uma árvore de diretórios profunda com um diretório em outro volume. Isso ocorre porque o caminho do volume é concatenado ao caminho do diretório. O **\_ caminho máximo** de constante definido globalmente define o número máximo de caracteres que um caminho pode ter. (Para obter mais informações sobre o **\_ caminho máximo**, consulte [nomeando um arquivo ou diretório](naming-a-file.md).) Você pode evitar essa restrição seguindo um destes procedimentos:

-   Consulte volumes por seus caminhos de GUID de volume.
-   Use as versões Unicode (W) das funções de arquivo, que dão suporte ao \\ \\ \\ prefixo?.

 

 



