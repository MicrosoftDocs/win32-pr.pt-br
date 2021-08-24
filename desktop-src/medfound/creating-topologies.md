---
description: Criando topologias
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Criando topologias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4048200055066a601f9044ff109f173cb00fc4449a71ea1331b29c8be1a59b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777616"
---
# <a name="creating-topologies"></a>Criando topologias

Esta seção descreve alguns dos procedimentos gerais para a criação de uma topologia.

As etapas gerais para criar uma topologia são as seguintes:

1.  Crie um novo objeto de topologia chamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Essa função retorna um ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia.

2.  Inicialmente, a topologia não contém nenhum nó. Para criar nós para a topologia, chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode). Essa função retorna um ponteiro para a interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) do nó. Você deve especificar o tipo de nó ao criar o nó:

    -   Nó de origem.

    -   Nó de transformação.

    -   Nó de saída.

    -   Nó de t.

3.  Inicialize cada nó. O processo de inicialização depende do tipo de nó, conforme descrito nos tópicos a seguir.

4.  Adicione cada nó à topologia chamando [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).

5.  Conexão os nós. Para conectar um nó, chame [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) no nó upstream e passe um ponteiro para o nó downstream.

Os tópicos a seguir fornecem as etapas específicas para cada tipo de nó.



| Tópico                                                    | Descrição                     |
|----------------------------------------------------------|---------------------------------|
| [Criando nós de origem](creating-source-nodes.md)       | Como criar um nó de origem.    |
| [Criando nós de transformação](creating-transform-nodes.md) | Como criar um nó de transformação. |
| [Criando nós de saída](creating-output-nodes.md)       | Como criar um nó de saída.   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Topologias](topologies.md)
</dt> </dl>

 

 



