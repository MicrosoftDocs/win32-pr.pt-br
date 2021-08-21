---
title: Formatos de disco
description: O IMAPI dá suporte a três formatos de sistema de arquivos ISO 9660, Ltdt e UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af71733ec2747ae227ac412a7b49f0faa73639cf1000f1332db5ec1d1d55db9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758598"
---
# <a name="disc-formats"></a>Formatos de disco

O IMAPI dá suporte a três formatos de sistema de arquivos: [ISO 9660,](#iso-9660) [Filet](#joliet)e [UDF.](#universal-disk-format-udf)

## <a name="iso-9660"></a>ISO 9660

O formato ISO 9660 é o sistema de arquivos padrão original para discos de dados de CD. O formato é reconhecido em vários sistemas operacionais, incluindo MSDOS, Mac OS, UNIX e o Windows operacional. O formato ISO 9660 é publicado pela Organização Internacional de Normalização (ISO).

O formato começa no setor 16 com o header do volume, CD0001; o restante do header segue. Outros formatos derivados também começam no setor 16, mas usam outra cadeia de caracteres para o header de volume. Por exemplo, os discos High Sierra usam a cadeia de caracteres CD-ROM0001 e o formato Interativo do Disco Compacto usa CD-I0001.

O título aponta para áreas do disco que armazenam os nomes de arquivo no formato ISO 9660. A convenção de nomeação de arquivo e diretório consiste em 8 caracteres, um ponto e mais três caracteres. Essa é a mesma convenção de nomen entre as usadas pelo sistema operacional MSDOS.

Os títulos adicionais do sistema de arquivos, para formatos como o Codt e o UDF, podem existir em um disco sem afetar a capacidade de leitura do formato ISO 9660. Após os índices, um conjunto de arquivos de dados ocupa o disco. Os índices de cada sistema de arquivos referenciam arquivos de dados independentemente no disco.

A especificação ISO 9660 define três níveis do formato:

-   O nível 1 define os nomes de arquivo para usar o formato de 8,3 caracteres.
-   O nível 2 permite nomes de arquivo mais longos, conforme encontrado nas plataformas DOS 6.xx, MacIntosh e UNIX.
-   O nível 3 permite que arquivos de áudio e dados intercalados melhorem o desempenho da recuperação (reprodução). Esse nível também remove o limite de arquivo de 2 GB. Não há suporte **para** esse nível na API de Controle de Imagem.

Os discos de DVD também podem usar ISO 9660; no entanto, o sistema de arquivos UDF é o sistema de arquivos mais predominante usado com mídia de DVD.

## <a name="joliet"></a>Joliet

O formato Det é um derivado de ISO 9660. Esse formato grava o índice do sistema de arquivos Dot na imagem do disco, além do índice do sistema de arquivos ISO 9660.

O índice Dot fornece as seguintes melhorias no índice do sistema de arquivos:

-   Reconhece nomes de arquivo longos de até 32 caracteres.
-   Distingue entre letras maiúsculas e inferiores nos nomes de arquivo.
-   Dá suporte a caracteres Unicode no nome do arquivo.

O título de formato Det começa no setor 17 do disco.

Como o formato Dot preserva o sistema de arquivos ISO 9660 em um disco, a compatibilidade com dispositivos compatíveis com ISO 9660 é mantida.

## <a name="universal-disk-format-udf"></a>UDF (Formato de Disco Universal)

O UDF (Formato de Disco Universal) é um sistema de arquivos mais novo desenvolvido para mídia óptica pela OSTA (Associação De Tecnologia Armazenamento Óptico). UDF é um formato portátil que é reconhecido por vários sistemas operacionais. O UDF está substituindo ISO 9660 como o novo padrão, especialmente pela mídia de leitura/gravação.

Os recursos da UDF incluem o seguinte:

-   Dá suporte a mídia de até 2 TB de tamanho.
-   Dá suporte a mídia flash, discos REV Iomô e discos CD-MRW.
-   Armazena arquivos com menos de 2 KB de comprimento no bloco Entrada de Arquivo.
-   Dá suporte a arquivos de até 2 TB com nomes de arquivo de até 255 caracteres.
-   Dá suporte a um conjunto rico de atributos de arquivo que se adequam a vários sistemas operacionais.
-   Dá suporte a um formato de ponte em que os formatos ISO 9660, Ltdt e UDF residem no mesmo disco. Isso é usado em aplicativos de vídeo, como DVD-Video, DVD+VR e DVD-VR.
-   Dá suporte a fluxos nomeados e arquivos 'em tempo real'.

 

 




