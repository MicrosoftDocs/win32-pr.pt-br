---
description: O sistema de arquivos NTFS usa a compactação Lempel-Ziv, que é um algoritmo de compactação sem perdas.
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: Compactação e descompactação de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d1aa9d8d3540eff85413c03358fd1ba7e21300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778605"
---
# <a name="file-compression-and-decompression"></a>Compactação e descompactação de arquivos

Os volumes do sistema de arquivos NTFS dão suporte à compactação de arquivo em uma base de arquivo individual. O algoritmo de compactação de arquivo usado pelo sistema de arquivos NTFS é Lempel-Ziv compactação. Esse é um algoritmo de compactação *sem perdas* , o que significa que nenhum dado é perdido ao compactar e descomprimir o arquivo, em oposição a algoritmos de compactação com *perdas* , como JPEG, em que alguns dados são perdidos cada vez que a compactação de dados e a descompactação ocorrem.

A compactação de dados reduz o tamanho de um arquivo, minimizando os dados redundantes. Em um arquivo de texto, os dados redundantes podem ocorrer com frequência caracteres, como o caractere de espaço, ou vogais comuns, como as letras e e a; Ele também pode estar ocorrendo com frequência cadeias de caracteres. A compactação de dados cria uma versão compactada de um arquivo, minimizando esses dados redundantes.

Cada tipo de algoritmo de compactação de dados minimiza os dados redundantes de maneira exclusiva. Por exemplo, o *algoritmo de codificação Huffman* atribui um código a caracteres em um arquivo com base na frequência com que esses caracteres ocorrem. Outro algoritmo de compactação, chamado de *codificação de comprimento de execução*, gera um valor de duas partes para caracteres repetidos: a primeira parte especifica o número de vezes que o caractere é repetido e a segunda parte identifica o caractere. Outro algoritmo de compactação, conhecido como o *Algoritmo Lempel-Ziv*, converte cadeias de caracteres de comprimento variável em códigos de comprimento fixo que consomem menos espaço do que as cadeias de caracteres originais.

## <a name="the-ntfs-file-system-file-compression"></a>A compactação de arquivo do sistema de arquivos NTFS

No sistema de arquivos NTFS, a compactação é executada de forma transparente. Isso significa que ele pode ser usado sem a necessidade de alterações em aplicativos existentes. Os bytes compactados do arquivo não estão acessíveis aos aplicativos; Eles veem apenas os dados descompactados. Portanto, os aplicativos que abrem um arquivo compactado podem operar nele como se não estivessem compactados. No entanto, esses arquivos não podem ser copiados para outro sistema de arquivos.

Se você compactar um arquivo com mais de 30 gigabytes, talvez a compactação não seja realizada com sucesso.

Os tópicos a seguir identificam a compactação de arquivo do sistema de arquivos NTFS:

-   [Atributo de compactação](compression-attribute.md)
-   [Estado de compactação](compression-state.md)
-   [Obtendo o tamanho de um arquivo compactado](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>Bibliotecas de compactação e descompactação de arquivos

As bibliotecas de compactação e descompactação de arquivo usam um arquivo ou arquivos existentes e produzem um arquivo ou arquivos que são versões compactadas dos originais. A compactação também é sem perdas, mas a compactação não é transparente para os aplicativos. Um aplicativo só pode operar nesses arquivos com a assistência de uma biblioteca de compactação de arquivos. Além disso, as únicas operações que podem ser executadas nesses arquivos estão criando um arquivo compactado de um original e recuperando os dados originais da versão descompactada. A edição normalmente não tem suporte e a busca é limitada, se houver suporte.

Normalmente, um aplicativo chama funções no Lz32.dll para descompactar dados que foram compactados usando Compress.exe. As funções também podem processar arquivos sem tentar descompactá-los.

Você pode usar as funções no Lz32.dll para descompactar um ou vários arquivos. Você também pode usá-los para descompactar arquivos compactados uma parte por vez.

Os tópicos a seguir identificam a descompactação de arquivo fornecida pelas funções no Lz32.dll:

-   [Descompactando um único arquivo](decompressing-a-single-file.md)
-   [Descompactando vários arquivos](decompressing-multiple-files.md)
-   [Lendo de arquivos compactados](reading-from-compressed-files.md)

## <a name="cabinets"></a>Pelos

Os gabinetes são criados por uma biblioteca de compactação que oferece suporte a recursos como distribuição de disco e compactação de vários arquivos. Para obter informações adicionais, consulte o gabinete Software Development Kit: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) .

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Atributo de compactação](compression-attribute.md)<br/>                                     | Em um volume do sistema de arquivos NTFS, cada arquivo e diretório têm um *atributo de compactação*.<br/>                                         |
| [Estado de compactação](compression-state.md)<br/>                                             | Cada arquivo e diretório em um volume que dá suporte à compactação para arquivos e diretórios individuais tem um *estado de compactação*.<br/> |
| [Obtendo o tamanho de um arquivo compactado](obtaining-the-size-of-a-compressed-file.md)<br/> | Para obter o tamanho compactado de um arquivo, use a função GetCompressedFileSize.<br/>                                               |
| [Descompactando um único arquivo](decompressing-a-single-file.md)<br/>                         | Um aplicativo pode descompactar um único arquivo compactado usando as funções LZOpenFile, LZCopy e LZClose.<br/>                |
| [Descompactando vários arquivos](decompressing-multiple-files.md)<br/>                       | Um aplicativo pode descompactar vários arquivos usando as funções LZOpenFile, LZCopy e LZClose.<br/>                          |
| [Lendo de arquivos compactados](reading-from-compressed-files.md)<br/>                     | Um aplicativo pode descompactar uma parte de um arquivo compactado por vez usando as funções LZSeek e LZRead.<br/>                 |



 

 

