---
title: Entrando no estado de execução
description: Entrando no estado de execução
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916211"
---
# <a name="entering-the-running-state"></a>Entrando no estado de execução

Quando um objeto incorporado faz a transição para o estado de execução, o manipulador de objetos deve localizar e executar o aplicativo de servidor para utilizar os serviços que apenas o servidor fornece. Os objetos inseridos são colocados no estado de execução explicitamente por meio de uma solicitação pelo contêiner, como uma necessidade de desenhar um formato não armazenado em cache no momento ou implicitamente pelo OLE em resposta à invocação de alguma operação, como quando um usuário do contêiner clica duas vezes no objeto.

Quando um objeto vinculado faz a transição para o estado de execução, o processo é conhecido como *Associação*. No processo de associação, o manipulador de objeto solicita que seu moniker armazenado Localize os dados do link e, em seguida, executa o aplicativo do servidor.

À primeira vista, a associação de um objeto vinculado parece não ser mais complicada do que a execução de um objeto inserido. No entanto, os seguintes pontos complicam o processo:

-   Um link pode se referir a um objeto ou a uma parte dele, que é inserida em outro contêiner. Esse recurso implica um potencial para incorporações aninhadas. A resolução de referências a tal hierarquia requer a passagem recursiva de um *moniker composto*, começando com o membro mais à direita.
-   Quando a origem do link está em execução, o OLE é associado à instância em execução do objeto em vez de executar outra instância. No caso de objetos incorporados aninhados, um dos quais é a origem do link, o OLE deve ser capaz de se associar a um objeto já em execução em qualquer ponto.
-   A execução de um objeto requer o acesso à área de armazenamento para o objeto. Quando um objeto inserido é executado, o OLE recebe um ponteiro para o armazenamento durante o processo de carregamento, que passa para o aplicativo do servidor OLE. Para objetos vinculados, no entanto, não há nenhuma interface padrão para acessar o armazenamento. O aplicativo do servidor OLE pode usar a interface do sistema de arquivos ou algum outro mecanismo.

 

 




