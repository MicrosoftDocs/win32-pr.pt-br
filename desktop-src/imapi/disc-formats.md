---
title: Formatos de disco
description: O IMAPi dá suporte a três formatos de sistema de arquivos ISO 9660, Joliet e UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292211"
---
# <a name="disc-formats"></a>Formatos de disco

O IMAPi dá suporte a três formatos de sistema de arquivos: [ISO 9660](#iso-9660), [Joliet](#joliet)e [UDF](#universal-disk-format-udf).

## <a name="iso-9660"></a>ISO 9660

O formato ISO 9660 é o sistema de arquivos padrão original para os discos de dados do CD. O formato é reconhecido em vários sistemas operacionais, incluindo o MSDOS, o Mac OS, o UNIX e o sistema operacional Windows. O formato ISO 9660 é publicado pelo Organização Internacional de Normalização (ISO).

O formato começa no setor 16 com o cabeçalho do volume, CD0001; segue o restante do cabeçalho. Outros formatos derivados também começam no setor 16, mas usam outra cadeia de caracteres para o cabeçalho do volume. Por exemplo, discos de alta serra usam a cadeia de caracteres CD-ROM0001 e o formato interativo do CD Interactive usam o CD-I0001.

O cabeçalho aponta para áreas do disco que armazenam os nomes de arquivo no formato ISO 9660. A Convenção de nomenclatura de arquivo e diretório consiste em 8 caracteres, um ponto e mais três caracteres. Essa é a mesma convenção de nomenclatura usada pelo sistema operacional MSDOS.

Cabeçalhos de sistema de arquivos adicionais, para formatos como Joliet e UDF, podem coexistir em um disco sem afetar a legibilidade do formato ISO 9660. Depois dos índices, um conjunto de arquivos de dados ocupa o disco. Os índices para cada sistema de arquivos referenciam arquivos de dados de forma independente no disco.

A especificação ISO 9660 define três níveis do formato:

-   O nível 1 define os nomes de arquivo para usar o formato de caractere 8,3.
-   O nível 2 permite nomes de arquivo mais longos, conforme encontrado em plataformas DOS 6. XX, MacIntosh e UNIX.
-   O nível 3 permite dados intercalados e arquivos de áudio para melhorar o desempenho da recuperação (reprodução). Esse nível também remove o limite de arquivos de 2GB. **Não** há suporte para esse nível na API de mestre de imagem.

Os discos de DVD também podem usar o ISO 9660; no entanto, o sistema de arquivos UDF é o sistema de arquivos mais predominante usado com mídia de DVD.

## <a name="joliet"></a>Joliet

O formato Joliet é um derivativo do ISO 9660. Esse formato grava o índice do sistema de arquivos Joliet na imagem do disco, além do índice do sistema de arquivos ISO 9660.

O índice Joliet fornece os seguintes aprimoramentos para o índice do sistema de arquivos:

-   Reconhece nomes de arquivo longos de até 32 caracteres.
-   Distingue entre letras maiúsculas e minúsculas nos nomes de arquivo.
-   Dá suporte a caracteres Unicode no nome do arquivo.

O cabeçalho de formato Joliet começa no setor 17 do disco.

Como o formato Joliet preserva o sistema de arquivos ISO 9660 em um disco, a compatibilidade com dispositivos ISO 9660 em conformidade é mantida.

## <a name="universal-disk-format-udf"></a>UDF (Formato de Disco Universal)

O UDF (formato de disco universal) é um sistema de arquivos mais recente desenvolvido para mídia óptica pela OSTA (Associação de tecnologia de armazenamento óptico). UDF é um formato portátil que é reconhecido por vários sistemas operacionais. O UDF está substituindo o ISO 9660 como o novo padrão, especialmente com mídia de leitura/gravação.

Os recursos do UDF incluem o seguinte:

-   Dá suporte à mídia de até 2TB de tamanho.
-   Dá suporte a Flash Media, discos Iomega REV e discos CD-MRW.
-   Armazena arquivos com menos de 2 KB de comprimento no bloco de entrada de arquivo.
-   Dá suporte a arquivos de até 2TB com nomes de arquivo, desde 255 caracteres.
-   O oferece suporte a um conjunto avançado de atributos de arquivo que atendam a vários sistemas operacionais.
-   Dá suporte a um formato de ponte em que os formatos ISO 9660, Joliet e UDF residem no mesmo disco. Isso é usado em aplicativos de vídeo, como DVD-Video, DVD + VR e DVD-VR.
-   Dá suporte a fluxos nomeados e arquivos ' em tempo real '.

 

 




