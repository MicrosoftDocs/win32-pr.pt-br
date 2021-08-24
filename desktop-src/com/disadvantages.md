---
title: Desvantagens
description: Desvantagens
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b9d41a632c202a25c3383ffb2d1069505c0dc988651e9fc886cfeecca5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501106"
---
# <a name="disadvantages"></a>Desvantagens

Os servidores em processo fornecem a vantagem de velocidade e tamanho de um manipulador de objetos com a capacidade de edição de um servidor local. Então, por que você optaria por implementar seu aplicativo OLE como um servidor local em vez de um servidor em processo? Há vários motivos:

-   Segurança. Somente um servidor local tem seu espaço de endereço isolado do do cliente. Um servidor em processo compartilha o espaço de endereço e o contexto de processo do cliente e, portanto, pode ser menos robusto em caso de falhas ou programação mal-intencionada.
-   Granularidade. Um servidor local pode hospedar várias instâncias de seu objeto em vários clientes diferentes, compartilhando o estado do servidor entre objetos em vários clientes de maneiras difíceis ou impossíveis se implementadas como um servidor em processo, que é simplesmente uma DLL carregada em cada cliente.
-   Compatibilidade. Se optar por implementar um servidor em processo, você abandonará a compatibilidade com o OLE 1, que não dá suporte a esses servidores. Isso não será uma consideração para muitos desenvolvedores, mas, se for, será uma preocupação crítica.
-   Incapacidade de dar suporte a links. Um servidor em processo não pode servir como uma fonte de link. Como uma DLL não pode ser executado por si só, ela não pode criar um objeto de arquivo a ser vinculado.

Apesar dessas desvantagens, um servidor em processo pode ser uma excelente opção para sua velocidade e tamanho – se ele atende a todos os seus outros requisitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vantagens](advantages.md)
</dt> <dt>

[Servidores em processo](in-process-servers.md)
</dt> </dl>

 

 




