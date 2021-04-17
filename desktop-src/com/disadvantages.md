---
title: Desvantagens
description: Desvantagens
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498783"
---
# <a name="disadvantages"></a>Desvantagens

Os servidores em processo fornecem a velocidade e a vantagem do tamanho de um manipulador de objetos com a capacidade de edição de um servidor local. Então, por que você iria optar por implementar seu aplicativo OLE como um servidor local em vez de um servidor em processo? Há vários motivos:

-   Segurança. Somente um servidor local tem seu espaço de endereço isolado do cliente. Um servidor em processo compartilha o espaço de endereço e o contexto do processo do cliente e, portanto, pode ser menos robusto diante de falhas ou programação mal-intencionada.
-   Granularidade. Um servidor local pode hospedar várias instâncias de seu objeto em vários clientes diferentes, compartilhando o estado do servidor entre objetos em vários clientes de maneiras que seriam difíceis ou impossíveis se implementadas como um servidor em processo, que é simplesmente uma DLL carregada em cada cliente.
-   Compatibilidade. Se você optar por implementar um servidor em processo, você cederá a compatibilidade com o OLE 1, que não oferece suporte a esses servidores. Isso não será uma consideração para muitos desenvolvedores, mas, se for, será uma preocupação importante.
-   Incapacidade de dar suporte a links. Um servidor em processo não pode servir como uma fonte de link. Como uma DLL não pode ser executada por si só, não é possível criar um objeto de arquivo a ser vinculado.

Apesar dessas desvantagens, um servidor em processo pode ser uma opção excelente para sua velocidade e tamanho — se atender a todos os seus requisitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vantagens](advantages.md)
</dt> <dt>

[Servidores em processo](in-process-servers.md)
</dt> </dl>

 

 




