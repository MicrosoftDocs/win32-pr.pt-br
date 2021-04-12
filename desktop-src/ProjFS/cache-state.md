---
title: Estado do cache na raiz de virtualização
description: Descreve os diferentes Estados de cache que um arquivo ou diretório gerenciado pelo provedor pode ter.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 43d62ceb1f5ef5bf07000666f336077270b1e86a
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "104365422"
---
# <a name="cache-state-in-the-virtualization-root"></a>Estado do cache na raiz de virtualização

O provedor usa o sistema de arquivos local na raiz de virtualização como um cache dos itens que ele gerencia.  Um item (arquivo ou diretório) pode estar em um dos seis Estados no sistema de arquivos local:

* Máquina

  O item não existe localmente no disco.  Ele é projetado, ou seja, sintetizado, durante as enumerações de seu diretório pai.  Os itens virtuais são mesclados com os itens que podem existir no disco para apresentar o conteúdo completo do diretório pai.

* Espaço reservado

  Para arquivos: o conteúdo do arquivo (fluxo de dados primário) não está presente no disco.  Os metadados do arquivo (nome, tamanho, carimbos de data/hora, atributos, etc.) são armazenados em cache no disco.
  
  Para diretórios: alguns ou todos os descendentes imediatos do diretório (os arquivos e diretórios no diretório) não estão presentes no disco, ou seja, eles ainda são virtuais.  Os metadados do diretório (nome, carimbos de data/hora, atributos, etc.) são armazenados em cache no disco.

* Espaço reservado para alimentador

  Para arquivos: o conteúdo e os metadados do arquivo foram armazenados em cache no disco.  Também conhecido como um "arquivo parcial".
  
  Para diretórios: um diretório que foi criado no disco como um espaço reservado nunca se torna um diretório de espaço reservado alimentado.  Isso permite que o provedor adicione ou remova itens do diretório em seu repositório de backup e que essas alterações sejam refletidas no cache local.

* Espaço reservado sujo (alimentado ou não)

  Os metadados do item foram modificados localmente e não são mais um cache de seu estado no repositório do provedor. Observe que a criação ou exclusão de um arquivo ou diretório em um diretório de espaço reservado faz com que o diretório de espaço reservado fique sujo.

* Arquivo/diretório completo

  Para arquivos: o conteúdo do arquivo (fluxo de dados primário) foi modificado.  O arquivo não é mais um cache de seu estado no repositório do provedor.  Os arquivos que foram criados no sistema de arquivos local (ou seja, que não existem no repositório do provedor) também são considerados arquivos completos.
  
  Para diretórios: diretórios que foram criados no sistema de arquivos local (ou seja, que não existem no repositório do provedor) são considerados diretórios completos.  Um diretório que foi criado no disco como um espaço reservado nunca se torna um diretório completo.
  
* Marca para exclusão

  Um espaço reservado especial oculto que representa um item que foi excluído do sistema de arquivos local.  Quando um diretório é enumerado, o ProjFS mescla o conjunto de itens locais (espaços reservados, arquivos completos, etc.) com o conjunto de itens de projeto virtual.  Se um item aparecer nos conjuntos local e projetado, o item local terá precedência.  Se um arquivo não existir no sistema de arquivos local, não haverá nenhum estado local, portanto, ele apareceria na enumeração.  No entanto, se esse item tivesse sido excluído, tê-lo exibido na enumeração seria inesperado.  Substituir um item excluído por uma marca para exclusão resulta nos seguintes efeitos:

  * Enumerações não revelam o item.
  * Abre o arquivo que espera que o item exista falha com, por exemplo, "arquivo não encontrado".
  * O arquivo cria o que esperará ter sucesso apenas se o item não existir com sucesso; ProjFS remove a marca para exclusão como parte da operação.

Para ilustrar os Estados acima, considere a seguinte sequência, dado um provedor de ProjFS que tem um único arquivo "foo.txt" localizado na raiz de virtualização C:\root.

1. Um aplicativo enumera C:\root.  Ele vê o arquivo virtual "foo.txt".  Como o arquivo ainda não foi acessado, o arquivo não existe no disco.
1. O aplicativo abre um identificador para C:\root\foo.txt.  ProjFS informa o provedor para criar um espaço reservado para ele.
1. O aplicativo lê o conteúdo do arquivo.  O provedor fornece o conteúdo do arquivo para ProjFS e é armazenado em cache para C:\root\foo.txt.  O arquivo agora é um espaço reservado para o alimentador.
1. O aplicativo atualiza o carimbo de data/hora da última modificação.  O arquivo agora é um espaço reservado com problemas.
1. O aplicativo abre um identificador para acesso de gravação ao arquivo.  C:\root\foo.txt agora é um arquivo completo.
1. O aplicativo exclui C:\root\foo.txt.  ProjFS substitui o arquivo por uma marca para exclusão.  Agora, quando o aplicativo enumera C:\root, ele não vê foo.txt.  Se ele tentar abrir o arquivo, a abertura falhará com ERROR_FILE_NOT_FOUND.
