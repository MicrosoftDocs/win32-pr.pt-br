---
description: Conectando e desconectando nós de topologia
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Conectando e desconectando nós de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772958"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>Conectando e desconectando nós de topologia

Para que uma topologia seja funcional, o nó de origem e o nó de saída devem estar conectados. Para conectar dois nós de topologia, arraste a saída do nó de um nó para a entrada de nó do outro nó. TopoEdit exibe a conexão do nó como uma linha preta. Isso é equivalente a conectar nós de topologia chamando o método [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .

A topologia só poderá ser resolvida se a conexão do nó for válida; ou seja, se os tipos de mídia dos dois nós forem compatíveis. Para obter informações sobre como resolver topologias, consulte [resolvendo uma topologia com TopoEdit](resolving-a-topology-with-topoedit.md).

Se você tentar fazer uma conexão de um nó que já está conectado, a nova conexão de nó substituirá a conexão de nó antiga.

Para excluir uma conexão, selecione a conexão do nó e pressione a tecla DELETE ou selecione **excluir** no menu **topologia** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando topologias usando TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



