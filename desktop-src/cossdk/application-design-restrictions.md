---
description: Alguns aplicativos são projetados de uma maneira que impede que várias instâncias do aplicativo sejam instaladas em um computador.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restrições de design do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b98e7b7d8dddf1cd74224573d355e1f42d75c8ae6122d20977bbc1b38ffb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917540"
---
# <a name="application-design-restrictions"></a>Restrições de design do aplicativo

Alguns aplicativos são projetados de uma maneira que impede que várias instâncias do aplicativo sejam instaladas em um computador. Com essa limitação, um aplicativo não pode usar o recurso de partições. Os seguintes recursos de design de aplicativo podem precisar ser modificados antes que as partições possam ser usadas para esse aplicativo.

## <a name="tables-and-arrays"></a>Tabelas e matrizes

Alguns aplicativos criam tabelas de banco de dados, tabelas na memória ou matrizes que usam um CLSID como uma chave exclusiva do Registro. Em um computador sem partições, essa chave do Registro normalmente é computer/CLSID (uma CLSID por computador).

Por outro lado, em um computador com partições, essa chave do Registro é id do computador/partição/ID do aplicativo/CLSID (várias instâncias de um CLSID por computador). Como o recurso de partições permite que várias instâncias de um CLSID existam em um computador, os aplicativos que contêm elementos de design que exigem um CLSID exclusivo por computador podem ser afetados negativamente.

## <a name="global-resources"></a>Recursos Globais

Alguns aplicativos usam recursos globais, como memória compartilhada, arquivos de dados e entradas do Registro. Isso poderá causar problemas se várias instâncias desse aplicativo estão sendo executadas simultaneamente.

Por exemplo, se um componente usar memória compartilhada para interagir com outros componentes, o componente precisará ser modificado para que cada instância do componente aloce sua própria memória compartilhada.

## <a name="type-libraries"></a>Bibliotecas de tipos

As bibliotecas de tipos fornecem informações sobre as interfaces e os métodos de um componente. Essas informações são usadas para várias finalidades, incluindo as seguintes:

-   Marshaling de dados entre componentes quando chamadas de função são feitas
-   Ajudando os componentes em fila COM+ e os serviços de eventos COM+
-   Fornecendo as informações corretas em um editor do Microsoft Visual Basic

As referências a uma biblioteca de tipos são instaladas no Registro de um computador. Ao desenvolver aplicativos que serão invocados de dentro de partições, é importante que a versão mais recente de uma biblioteca de tipos seja instalada no Registro. Isso garante que o editor Visual Basic que está sendo usado obterá informações precisas sobre os métodos disponíveis para esse componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Partições e componentes em fila COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementação de partição](partition-implementation.md)
</dt> <dt>

[Registrando e ativando componentes em partições](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[O que são partições COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



