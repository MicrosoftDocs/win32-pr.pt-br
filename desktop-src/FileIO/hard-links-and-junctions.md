---
description: Descreve links e junções difíceis.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Links físicos e junções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760076"
---
# <a name="hard-links-and-junctions"></a>Links físicos e junções

Há três tipos de links de arquivo com suporte no sistema de arquivos NTFS: links físicos, junções e links simbólicos. Este tópico é uma visão geral dos links e junções difíceis. Para obter informações sobre links simbólicos, consulte [criando links simbólicos](creating-symbolic-links.md).

## <a name="hard-links"></a>Links físicos

Um *vínculo físico* é a representação do sistema de arquivos de um arquivo pelo qual mais de um caminho faz referência a um único arquivo no mesmo volume. Para criar um link físico, use a função [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) . Qualquer alteração no arquivo é imediatamente visível para aplicativos que o acessam por meio de links físicos que fazem referência a ele. No entanto, as informações de tamanho e atributo de entrada de diretório são atualizadas somente para o link pelo qual a alteração foi feita. Observe que os atributos no arquivo são refletidos em cada link físico para esse arquivo e as alterações nos atributos desse arquivo se propagam para todos os links físicos. Por exemplo, se você redefinir o atributo READONLY em um link físico para excluir esse link físico específico e houver vários links físicos para o arquivo real, será necessário redefinir o bit READONLY no arquivo de um dos links físicos restantes para trazer o arquivo e todos os links físicos restantes de volta para o estado READONLY.

Por exemplo, em um sistema em que C: e D: são unidades locais e Z: é uma unidade de rede mapeada para \\ \\ Fred \\ share, as seguintes referências são permitidas como um link físico:

-   C: \\ dira \\ethel.txt vinculado a C: \\ dirb \\ dirc \\lucy.txt
-   D: \\ dir1 \\tinker.txt a D: \\ dir2 \\ Dirx \\bell.txt
-   C: \\ diry \\ Bob. bak vinculado a C: \\ dir2 \\mina.txt

Os itens a seguir não são:

-   C: \\ dira vinculado a C: \\ dirb
-   C: \\ dira \\ethel.txt vinculado a D: \\ dirb \\lucy.txt
-   C: \\ dira \\ethel.txt vinculado a Z: \\ dirb \\lucy.txt

Para excluir um link físico, use a função [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) . Você pode excluir links físicos em qualquer ordem, independentemente da ordem em que eles são criados.

## <a name="junctions"></a>Junções

Uma *junção* (também chamada de *link suave*) difere de um link físico no qual os objetos de armazenamento referenciados são diretórios separados e uma junção pode vincular diretórios localizados em diferentes volumes locais no mesmo computador. Caso contrário, as junções operam de forma idêntica a links físicos. As junções são implementadas por meio de [pontos de nova análise](reparse-points.md).

Supondo que as mesmas condições na seção de links físicos, as referências a seguir são permitidas como junções:

-   C: \\ dira vinculado a C: \\ dirb \\ dirc
-   C: \\ Dirx vinculado a D: \\ diry

Os itens a seguir não são:

-   C: \\ dira \\one.txt vinculados a C \\ : \\ dirbtwo.txt
-   C: \\ dir1 vinculado a Z: \\ dir2

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando links simbólicos](creating-symbolic-links.md)
</dt> </dl>

 

 



