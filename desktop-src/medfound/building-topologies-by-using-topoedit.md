---
description: Criando topologias usando TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Criando topologias usando TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089796"
---
# <a name="building-topologies-by-using-topoedit"></a>Criando topologias usando TopoEdit

Uma topologia deve ter os três nós a seguir:

-   Nó de origem: os fluxos de um arquivo de mídia, que são usados como uma fonte para a topologia.
-   Nó de transformação: uma Media Foundation transformação (MFT). Esses nós geralmente são codificadores, decodificadores e efeitos para a topologia.
-   Nó de saída: o coletor de fluxo que passa os dados de mídia, quadros de vídeo ou fluxos de áudio para a sessão de mídia para reprodução.

Para obter informações sobre a estrutura de topologia, consulte [sobre topologias](about-topologies.md).

Para criar uma topologia, você deve adicionar os nós, conectar os nós e resolver a topologia para que ela possa ser reproduzida.

Os nós de topologia são exibidos como caixas, com texto mostrando o nome do nó. As caixas verdes representam os nós que são adicionados pelo usuário. Quando uma topologia é resolvida, o TopoEdit pode adicionar nós de transformação automaticamente à topologia. Eles aparecem como caixas azuis no **painel topologia**.

As entradas e saídas de topologia são representadas por como quadrados pretos ao longo da borda do nó. A *entrada de nó* é mostrada no lado esquerdo do nó e a *saída do nó* está no lado direito do nó.

Os nós de topologia são conectados por meio de uma *conexão de nó* que aparece como uma linha preta conectando a entrada de nó de um nó à saída do nó de outro nó.

A ilustração a seguir mostra uma topologia conectada para uma fonte de áudio.

![ilustração mostrando conexões do nó de origem, para dois nós de transformação e, em seguida, para o nó de saída](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Esta seção contém os seguintes tópicos:



| Tópico                                                                                          | Descrição                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Adicionando nós de origem com TopoEdit](adding-source-nodes-with-topoedit.md)                     | Descreve o processo de adicionar nós de origem a uma topologia.    |
| [Adicionando nós de transformação com TopoEdit](adding-transform-nodes-with-topoedit.md)               | Descreve o processo de adicionar nós de transformação a uma topologia. |
| [Adicionando nós de saída com TopoEdit](adding-output-nodes-with-topoedit.md)                     | Descreve o processo de adicionar nós de saída a uma topologia.    |
| [Conectando e desconectando nós de topologia](connecting-and-disconnecting-topology-nodes.md) | Descreve o processo de conexão de dois nós.                 |
| [Resolvendo uma topologia com TopoEdit](resolving-a-topology-with-topoedit.md)                   | Descreve o processo de resolução de topologia.                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



