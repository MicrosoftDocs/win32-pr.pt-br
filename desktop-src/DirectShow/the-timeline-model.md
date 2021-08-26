---
description: O modelo de linha do tempo
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: O modelo de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e5eeb60dce31fa466a518476bb3da341a3d2fda4fdeaa47ca58a89a904dded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903798"
---
# <a name="the-timeline-model"></a>O modelo de linha do tempo

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Uma *linha* do tempo é um objeto [DirectShow DES (Serviços](directshow-editing-services.md) de Edição) usa para representar um projeto de edição de vídeo. Um projeto de edição é iniciado como uma coleção de clipes de origem, retirados de arquivos de vídeo, arquivos de som ou ainda arquivos de imagem. Uma sequência linear de clipes forma uma *faixa*. No DirectShow DES (Serviços de Edição), áudio e vídeo são colocados em faixas separadas.

As faixas também podem ser em camadas. Várias faixas de áudio são misturadas e podem incluir efeitos de áudio, como esmaece ou reverb. Várias faixas de vídeo são usadas para criar transições. Por exemplo, você pode criar um apagando de um clipe para outro. Outro exemplo é uma chave de chroma, na qual a parte de fundo de um clipe é destacada e substituída por uma faixa diferente. (O previsão do tempo na frente de uma imagem satelite é um exemplo de chave de chroma.)

O DES usa uma estrutura de árvore para representar uma edição:

-   Clipes de áudio e vídeo formam os nós folha ou objetos *de origem.*
-   Uma coleção de fontes com um tipo de mídia uniforme (áudio ou vídeo) é uma *faixa*.
-   Uma coleção de faixas é uma *composição*. Uma composição é renderizada como a composição de todas as faixas que ela contém. As composições podem conter outras composições, o que permite a organização complexa de faixas.
-   Uma coleção de nível superior de composições e faixas (todas representando o mesmo tipo de mídia) é um *grupo*.
-   Um conjunto de um ou mais grupos forma uma linha do *tempo*. A linha do tempo é o nó raiz na árvore.

Uma linha do tempo deve conter pelo menos um grupo. Cada grupo representa um único fluxo na produção final. Um projeto típico inclui um grupo de vídeo e um grupo de áudio. As composições são opcionais; eles existem para fornecer mais estrutura, se necessário.

A ilustração a seguir mostra as relações pai-filho que compoem uma linha do tempo:

![estrutura de nó](images/timeline1.png)

O seguinte mostra uma linha do tempo como uma sequência temporal:

![ilustração da linha do tempo](images/timeline2.png)

A seta na parte superior representa a direção da linha do tempo, começando da hora zero. Dentro do grupo de vídeos, a faixa 1 tem uma prioridade mais alta do que a faixa 0. Os objetos de origem na faixa 1 obscurecem aqueles na faixa 0. Onde a faixa 1 está vazia, a faixa 0 "mostra". Conforme mencionado anteriormente, as faixas de áudio são simplesmente misturadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com DirectShow de Edição](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Construindo uma linha do tempo](constructing-a-timeline.md)
</dt> </dl>

 

 



