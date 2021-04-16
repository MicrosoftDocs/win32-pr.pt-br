---
description: Alguns aplicativos são criados de forma a impedir que várias instâncias do aplicativo sejam instaladas em um computador.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restrições de design de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768811"
---
# <a name="application-design-restrictions"></a>Restrições de design de aplicativo

Alguns aplicativos são criados de forma a impedir que várias instâncias do aplicativo sejam instaladas em um computador. Com essa limitação, um aplicativo não pode usar o recurso de partições. Os seguintes recursos de design de aplicativo podem precisar ser modificados antes que as partições possam ser usadas para esse aplicativo.

## <a name="tables-and-arrays"></a>Tabelas e matrizes

Alguns aplicativos criam tabelas de banco de dados, tabelas na memória ou matrizes que usam um CLSID como uma chave de registro exclusiva. Em um computador sem partições, essa chave do registro normalmente é Computer/CLSID (um CLSID por computador).

Por outro lado, em um computador com partições, essa chave do registro é ID de computador/partição/ID do aplicativo/CLSID (várias instâncias de um CLSID por computador). Como o recurso de partições permite que várias instâncias de um CLSID existam em um computador, os aplicativos que contêm elementos de design que exigem um CLSID exclusivo por computador podem ser afetados negativamente.

## <a name="global-resources"></a>Recursos Globais

Alguns aplicativos usam recursos globais, como memória compartilhada, arquivos de dados e entradas do registro. Isso pode causar problemas se várias instâncias desse aplicativo estiverem sendo executadas simultaneamente.

Por exemplo, se um componente usa memória compartilhada para interagir com outros componentes, o componente precisará ser modificado para que cada instância do componente aloque sua própria memória compartilhada.

## <a name="type-libraries"></a>Bibliotecas de tipos

As bibliotecas de tipos fornecem informações sobre interfaces e métodos de um componente. Essas informações são usadas para várias finalidades, incluindo as seguintes:

-   Marshaling de dados entre componentes quando são feitas chamadas de função
-   Ajudando os componentes em fila COM+ e os serviços de eventos COM+
-   Fornecendo as informações corretas em um editor de Visual Basic da Microsoft

As referências a uma biblioteca de tipos são instaladas no registro de um computador. Ao desenvolver aplicativos que serão invocados em partições, é importante que a versão mais recente de uma biblioteca de tipos seja instalada no registro. Isso garante que o editor de Visual Basic que está sendo usado receberá informações precisas sobre os métodos disponíveis para esse componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes e partições em fila COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementação de partição](partition-implementation.md)
</dt> <dt>

[Registrando e ativando componentes em partições](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[O que são partições COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



