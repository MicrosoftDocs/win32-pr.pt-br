---
description: Sobre topologias
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: Sobre topologias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35008d839e8054554370039dd13297ae7a1f0b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557310"
---
# <a name="about-topologies"></a>Sobre topologias

Uma topologia é um objeto que representa como os dados fluem no pipeline. Um aplicativo cria uma topologia para descrever o caminho que cada fluxo pega da origem de mídia para um coletor de mídia. O aplicativo passa a topologia para a sessão de mídia e a sessão de mídia usa a topologia para controlar o fluxo de dados.

Os componentes de processamento de dados no pipeline (fontes de mídia, transformações e coletores de mídia) são representados na topologia como *nós*. O fluxo de dados de um componente para outro é representado por uma conexão entre os nós. Os seguintes tipos de nó são definidos:

-   Nó de origem: representa um fluxo de mídia em uma origem de mídia.
-   Nó de transformação: representa uma Media Foundation de transformação (MFT).
-   Nó de saída: representa um coletor de fluxo em um coletor de mídia.
-   Nó de "t": representa uma bifurcação no fluxo. Os nós de "t" são uma exceção à regra que um nó representa um objeto de pipeline. Ao contrário de outros tipos de nó, o nó de "t" simplesmente direciona o fluxo de dados.

Uma topologia funcional deve conter pelo menos um nó de origem conectado a um nó de saída, possivelmente por meio de um ou mais nós de transformação. Por exemplo, o diagrama a seguir mostra uma topologia simples com um fluxo.

![um diagrama que mostra uma topologia com um fluxo.](images/topology01.png)

Para a reprodução de arquivos, o nó de transformação pode representar um decodificador e o nó de saída representaria o processador de áudio ou vídeo. Para codificação de arquivo, o nó de transformação representaria um codificador e o nó de saída representaria um coletor de arquivo morto, como o coletor de arquivos ASF.

Se dois nós estiverem conectados, o nó que produz dados é chamado de nó *upstream* e o nó que recebe dados é chamado de nó *downstream* . Por exemplo, no diagrama anterior, o nó de origem é upstream a partir do nó de transformação.

Em um par de nós conectados, o ponto de conexão no nó upstream é chamado de *saída*. O ponto de conexão no nó downstream é chamado de *entrada*. O diagrama a seguir mostra um par de nós com seus pontos de conexão e o fluxo de dados entre eles. Os pontos de conexão não são representados como objetos separados na topologia. Eles são especificados pelo valor de índice no objeto node.

![um diagrama que mostra dois nós conectados.](images/topology04.png)

Um nó de origem não pode ter nenhuma entrada. Portanto, não pode haver nenhum nó upstream a partir de uma origem. Da mesma forma, um nó de saída não pode ter saídas e não pode haver nós downstream de um nó de saída. Uma cadeia de nós de um nó de origem para um nó de saída é chamada de *ramificação* da topologia. O primeiro diagrama neste tópico mostra uma topologia com uma única ramificação. Geralmente, há uma ramificação por fluxo. Para reproduzir um arquivo com um fluxo de áudio e um fluxo de vídeo, por exemplo, requer uma topologia com duas ramificações.

## <a name="partial-topologies"></a>Topologias parciais

Uma topologia completa ou *completa* contém um nó para cada objeto de pipeline necessário. No entanto, o aplicativo nem sempre precisa criar uma topologia completa. Em vez disso, ele cria uma topologia *parcial* que omite um ou mais nós de transformação.

A sessão de mídia conclui a topologia usando um objeto chamado carregador de *topologia*. O carregador de topologia converte topologias parciais em topologias completas, inserindo as transformações necessárias. O processo de conversão é chamado de *resolução* da topologia.

Por exemplo, para reproduzir um fluxo de áudio codificado, a topologia deve ter um decodificador entre os nós de origem e de saída. O aplicativo cria uma topologia parcial que conecta o nó de origem diretamente ao nó de saída, sem o decodificador. O carregador de topologia examina os formatos de fluxo, localiza o decodificador correto e insere um nó de transformação na topologia.

O diagrama a seguir mostra a topologia parcial criada pelo aplicativo.

![um diagrama que mostra um parcial com um nó de origem e um nó de saída.](images/topology02.png)

O próximo diagrama mostra a topologia completa depois que o carregador de topologia a resolve. Neste exemplo, o carregador de topologia inseriu um nó de transformação para o decodificador.

![um diagrama que mostra uma topologia completa.](images/topology03.png)

Na versão atual do Media Foundation, o carregador de topologia dá suporte a topologias para reprodução. Para codificação de arquivo e outros cenários, o aplicativo deve construir uma topologia completa.

Os aplicativos também podem criar o carregador de topologia e usá-lo diretamente. Por exemplo, você pode usar o carregador de topologia para resolver uma topologia parcial e, em seguida, modificar a topologia completa antes de fornecê-la à sessão de mídia. Para criar o carregador de topologia, chame [**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Topologias](topologies.md)
</dt> </dl>

 

 



