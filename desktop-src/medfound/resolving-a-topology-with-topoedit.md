---
description: Resolvendo uma topologia com TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Resolvendo uma topologia com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511ceef8ea333ece43ebdb8adab555178f1976a20b60b354b017159011635e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058241"
---
# <a name="resolving-a-topology-with-topoedit"></a>Resolvendo uma topologia com TopoEdit

Há dois tipos de topologias:

-   Topologia parcial. O nó de origem está conectado diretamente ao nó de saída. Em alguns casos, uma topologia parcial pode ter alguns nós de transformação intermediários, como efeitos, mas não todos. Os nós de transformação que são omitidos normalmente são decodificadores ou MFTs de conversão de formato, como conversores de cor e reamostragens de áudio.

-   Topologia completa. O nó de origem está conectado ao nó de saída por meio de um nó de transformação. Esse tipo de topologia deve ter cada nó para processar dados.

TopoEdit só pode reproduzir topologias completas. O TopoEdit usa o objeto de carregador de topologia, fornecido pelo Media Foundation, para converter uma topologia parcial em uma topologia completa, inserindo as transformações necessárias. O processo de criação de uma topologia completa é chamado de resolução de uma topologia.

Para obter informações sobre tipos de topologia, consulte a seção topologias parciais em [sobre topologias](about-topologies.md).

Antes de resolver uma topologia, verifique se:

-   A topologia contém um nó de origem e um nó de saída.

-   Os nós de origem e saída estão conectados por uma conexão de nó válida. Durante a resolução da topologia, o carregador de topologia verifica o tipo de mídia dos nós quanto à compatibilidade. Se houver uma conexão de nó inválida, o processo falhará e uma mensagem de erro será exibida.

Para resolver uma topologia, no menu **topologia** , clique em **resolver topologia**.

A barra de ferramentas indica o status da topologia: **\[ resolvido \]** ou **\[ não resolvido \]**.

Se TopoEdit resolver uma topologia com êxito, o **status da topologia** será definido como **\[ resolvido \]** e os controles de reprodução serão habilitados.

Cada vez que você faz alterações na topologia, o **status da topologia** é definido como **\[ não resolvido \]** , o que indica que ela deve ser resolvida novamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando topologias usando TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



