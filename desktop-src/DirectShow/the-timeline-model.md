---
description: O modelo de linha do tempo
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: O modelo de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554846"
---
# <a name="the-timeline-model"></a>O modelo de linha do tempo

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Uma *linha do tempo* é um objeto que o [serviço de edição do DirectShow](directshow-editing-services.md) (des) usa para representar um projeto de edição de vídeo. Um projeto de edição é iniciado como uma coleção de clipes de origem, extraídos de arquivos de vídeo, arquivos de som ou arquivos de imagem ainda. Uma sequência linear de clipes formam uma *faixa*. Em serviços de edição do DirectShow (DES), áudio e vídeo são colocados em faixas separadas.

As faixas também podem ser em camadas. Várias faixas de áudio são misturadas e podem incluir efeitos de áudio, como fade ou reverberação. Várias faixas de vídeo são usadas para criar transições. Por exemplo, você pode criar um apagamento de um clipe para outro. Outro exemplo é uma chave croma, na qual o plano de fundo de um clipe é inserido e substituído por uma faixa diferente. (O previsão do tempo na frente de uma imagem satelite é um exemplo de croma de chaveamento.)

O DES usa uma estrutura de árvore para representar uma edição:

-   Os clipes de áudio e vídeo formam os nós folha ou os objetos de *origem* .
-   Uma coleção de fontes com um tipo de mídia uniforme (áudio ou vídeo) é uma *faixa*.
-   Uma coleção de faixas é uma *composição*. Uma composição é renderizada como a composição de todas as faixas que ela contém. As composições podem conter outras composições, o que permite a organização de faixas complexas.
-   Uma coleção de alto nível de composições e faixas (todas representando o mesmo tipo de mídia) é um *grupo*.
-   Um conjunto de um ou mais grupos formam uma *linha do tempo*. A linha do tempo é o nó raiz na árvore.

Uma linha do tempo deve conter pelo menos um grupo. Cada grupo representa um único fluxo na produção final. Um projeto típico inclui um grupo de vídeos e um grupo de áudio. As composições são opcionais; elas existem para fornecer mais estrutura, se necessário.

A ilustração a seguir mostra as relações filho-pai que compõem uma linha do tempo:

![estrutura do nó](images/timeline1.png)

O seguinte mostra uma linha do tempo como uma sequência temporal:

![ilustração da linha do tempo](images/timeline2.png)

A seta na parte superior representa a direção da linha do tempo, começando do tempo zero. No grupo de vídeos, Track 1 tem uma prioridade mais alta do que a faixa 0. Os objetos de origem no Track 1 obscurecem aqueles no Track 0. Onde Track 1 está vazio, Track 0 "mostra". Como mencionado anteriormente, as faixas de áudio são simplesmente misturadas juntas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com os serviços de edição do DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Construindo uma linha do tempo](constructing-a-timeline.md)
</dt> </dl>

 

 



