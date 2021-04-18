---
title: Estado de objeto persistente
description: Estado de objeto persistente
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291934"
---
# <a name="persistent-object-state"></a>Estado de objeto persistente

Alguns objetos COM podem salvar seu estado interno quando solicitados a fazer isso por um cliente.

COM define padrões por meio dos quais os clientes podem solicitar que os objetos sejam inicializados, carregados e salvos em e de um armazenamento de dados (por exemplo, arquivo simples, armazenamento estruturado ou memória). É responsabilidade do cliente gerenciar o local onde os dados persistentes do objeto são armazenados, mas não o formato dos dados. Objetos COM que aderem a esses padrões são chamados de *objetos persistentes*.

Para mais informações, consulte os seguintes tópicos:

-   [Interfaces de objeto persistentes](persistent-object-interfaces.md)
-   [Inicializando objetos persistentes](initializing-persistent-objects.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




