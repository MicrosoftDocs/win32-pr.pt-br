---
title: Estado do cache na raiz de virtualização
description: Descreve os diferentes estados de cache que um arquivo ou diretório gerenciado pelo provedor pode ter.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 378973075017cc1ac06bf46840ea9d2d1058150a46587eb537374d501396ce30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792863"
---
# <a name="cache-state-in-the-virtualization-root"></a>Estado do cache na raiz de virtualização

O provedor usa o sistema de arquivos local na raiz de virtualização como um cache dos itens que ele gerencia.  Um item (arquivo ou diretório) pode estar em um dos seis estados no sistema de arquivos local:

* Máquina

  O item não existe localmente no disco.  Ele é projetado, ou seja, sintetizado durante enumerações de seu diretório pai.  Os itens virtuais são mesclados com todos os itens que podem existir no disco para apresentar o conteúdo completo do diretório pai.

* Espaço reservado

  Para arquivos: o conteúdo do arquivo (fluxo de dados primário) não está presente no disco.  Os metadados do arquivo (nome, tamanho, timestamps, atributos etc.) são armazenados em cache no disco.
  
  Para diretórios: alguns ou todos os descendentes imediatos do diretório (os arquivos e diretórios no diretório) não estão presentes no disco, ou seja, ainda são virtuais.  Os metadados do diretório (nome, timestamps, atributos etc.) são armazenados em cache no disco.

* Espaço reservado Dratado

  Para arquivos: o conteúdo e os metadados do arquivo foram armazenados em cache no disco.  Também conhecido como um "arquivo parcial".
  
  Para diretórios: um diretório que foi criado no disco como um espaço reservado nunca se torna um diretório de espaço reservado tado.  Isso permite que o provedor adicione ou remova itens do diretório em seu armazenamento de back-back e que essas alterações sejam refletidas no cache local.

* Espaço reservado sujo (tado ou não)

  Os metadados do item foram modificados localmente e não são mais um cache de seu estado no armazenamento do provedor. Observe que criar ou excluir um arquivo ou diretório em um diretório de espaço reservado faz com que esse diretório de espaço reservado se torne sujo.

* Arquivo/diretório completo

  Para arquivos: o conteúdo do arquivo (fluxo de dados primário) foi modificado.  O arquivo não é mais um cache de seu estado no armazenamento do provedor.  Arquivos que foram criados no sistema de arquivos local (ou seja, que não existem no armazenamento do provedor) também são considerados arquivos completos.
  
  Para diretórios: os diretórios que foram criados no sistema de arquivos local (ou seja, que não existem no armazenamento do provedor) são considerados diretórios completos.  Um diretório que foi criado no disco como um espaço reservado nunca se torna um diretório completo.
  
* Lápide

  Um espaço reservado oculto especial que representa um item que foi excluído do sistema de arquivos local.  Quando um diretório é enumerado, o ProjFS mescla o conjunto de itens locais (espaço reservados, arquivos completos etc.) com o conjunto de itens projetados virtuais.  Se um item aparecer nos conjuntos local e projetado, o item local tem precedência.  Se um arquivo não existir no sistema de arquivos local, não haverá nenhum estado local, portanto, ele aparecerá na enumeração .  No entanto, se esse item tivesse sido excluído, ter ele exibido na enumeração seria inesperado.  Substituir um item excluído por uma chave de exclusão resulta nos seguintes efeitos:

  * Enumerações para não revelar o item.
  * O arquivo aberto que espera que o item exista falhe, por exemplo, "arquivo não encontrado".
  * Cria arquivos que esperam ter êxito somente se o item não existir com êxito; O ProjFS remove a lápis como parte da operação.

Para ilustrar os estados acima, considere a sequência a seguir, considerando um provedor ProjFS que tem um único arquivo "foo.txt" localizado na raiz de virtualização C:\root.

1. Um aplicativo enumera C:\root.  Ele vê o arquivo virtual "foo.txt".  Como o arquivo ainda não foi acessado, o arquivo não existe no disco.
1. O aplicativo abre um handle para C:\root\foo.txt.  O ProjFS informa ao provedor para criar um espaço reservado para ele.
1. O aplicativo lê o conteúdo do arquivo.  O provedor fornece o conteúdo do arquivo para o ProjFS e é armazenado em cache para C:\root\foo.txt.  O arquivo agora é um espaço reservado com seção.
1. O aplicativo atualiza o data/hora da Última Modificação.  O arquivo agora é um espaço reservado sujo.
1. O aplicativo abre um handle para acesso de gravação ao arquivo.  C:\root\foo.txt agora é um arquivo completo.
1. O aplicativo exclui C:\root\foo.txt.  O ProjFS substitui o arquivo por uma chave de lápis.  Agora, quando o aplicativo enumera C:\root, ele não vê foo.txt.  Se ele tentar abrir o arquivo, o abrir falhará com ERROR_FILE_NOT_FOUND.
