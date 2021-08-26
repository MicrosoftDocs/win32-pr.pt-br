---
description: Descreve links rígidos e junções.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Links rígidos e junções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ed8b3bbe163d2bad4b8c51715537e194633f02ec200ceb5df02df7d582ae3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107445"
---
# <a name="hard-links-and-junctions"></a>Links rígidos e junções

Há três tipos de links de arquivo com suporte no sistema de arquivos NTFS: links rígidos, junções e links simbólicos. Este tópico é uma visão geral de links rígidos e junções. Para obter informações sobre links simbólicos, consulte [Criando links simbólicos.](creating-symbolic-links.md)

## <a name="hard-links"></a>Links físicos

Um *link rígido* é a representação do sistema de arquivos de um arquivo pelo qual mais de um caminho faz referência a um único arquivo no mesmo volume. Para criar um link rígido, use a [**função CreateHardLink.**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) Todas as alterações nesse arquivo são instantaneamente visíveis para aplicativos que o acessam por meio dos links rígidos que o referenciam. No entanto, o tamanho da entrada do diretório e as informações de atributo são atualizados apenas para o link por meio do qual a alteração foi feita. Observe que os atributos no arquivo são refletidos em cada link rígido para esse arquivo e as alterações nos atributos desse arquivo se propagam para todos os links rígidos. Por exemplo, se você redefinir o atributo READONLY em um link rígido para excluir esse link rígido específico e houver vários links rígidos para o arquivo real, será necessário redefinir o bit READONLY no arquivo de um dos links rígidos restantes para trazer o arquivo e todos os links rígidos restantes de volta para o estado READONLY.

Por exemplo, em um sistema em que C: e D: são unidades locais e Z: é uma unidade de rede mapeada para o compartilhamento de compartilhamento, as seguintes referências são permitidas como \\ \\ um link \\ rígido:

-   C: \\ dira \\ethel.txt vinculado a C: \\ dirb \\ dirc \\lucy.txt
-   D: \\ dir1 \\tinker.txt para D: \\ dir2 \\ dirx \\bell.txt
-   C: \\ diry \\ bob.bak vinculado a C: \\ dir2 \\mina.txt

Os seguintes não são:

-   C: \\ dira vinculado a C: \\ dirb
-   C: \\ dira \\ethel.txt vinculado a D: \\ dirb \\lucy.txt
-   C: \\ dira \\ethel.txt vinculado a Z: \\ dirb \\lucy.txt

Para excluir um link rígido, use a [**função DeleteFile.**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) Você pode excluir links rígidos em qualquer ordem, independentemente da ordem em que eles são criados.

## <a name="junctions"></a>Junções

Uma  junção (também chamada de link *soft)* difere de um link rígido, já que os objetos de armazenamento referenciados são diretórios separados e uma junção pode vincular diretórios localizados em diferentes volumes locais no mesmo computador. Caso contrário, as junções operam de forma idêntica aos links rígidos. Junções são implementadas por meio [de pontos de reparse](reparse-points.md).

Supondo as mesmas condições na seção Links Rígidos, as seguintes referências são permitidas como junções:

-   C: \\ dira vinculado a C: \\ dirb \\ dirc
-   C: \\ dirx vinculado a D: \\ diry

Os seguintes não são:

-   C: \\ dira \\one.txt vinculado a C: \\ dirb \\two.txt
-   C: \\ dir1 vinculado a Z: \\ dir2

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando links simbólicos](creating-symbolic-links.md)
</dt> </dl>

 

 



