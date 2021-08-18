---
description: O pool de objetos é um serviço automático fornecido pelo COM+ que permite que você configure um componente para que as instâncias dele sejam mantidas ativas em um pool, prontas para serem usadas por qualquer cliente que solicite o componente.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Conceitos de pool de objetos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836dd6f29c2f0bd120843a1a93763d46cb51224966f255251f7e3bfb4c7fa66a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129138"
---
# <a name="com-object-pooling-concepts"></a>Conceitos de pool de objetos COM+

O pool de objetos é um serviço automático fornecido pelo COM+ que permite que você configure um componente para que as instâncias dele sejam mantidas ativas em um pool, prontas para serem usadas por qualquer cliente que solicite o componente. Você pode configurar administrativamente e monitorar o pool mantido para um determinado componente, especificando características como tamanho do pool e valores de tempo limite da solicitação de criação. Quando o aplicativo está em execução, o COM+ gerencia o pool para você, tratando os detalhes da ativação e reutilização de objetos de acordo com os critérios especificados.

Você pode obter benefícios de desempenho e dimensionamento muito significativos reutilizando objetos dessa maneira, especialmente quando eles são escritos para tirar total proveito da reutilização. Com o pooling de objetos, você obterá os seguintes benefícios:

-   Você pode acelerar o tempo de uso do objeto para cada cliente, Fatorando a inicialização demorada e a aquisição de recursos do trabalho real que o objeto executa para os clientes.
-   Você pode compartilhar o custo de aquisição de recursos caros em todos os clientes.
-   É possível alocar objetos previamente quando o aplicativo é iniciado, antes de qualquer solicitação de cliente chegar.
-   Você pode controlar o uso de recursos com o gerenciamento de pool administrativo, por exemplo, ao definir um nível máximo apropriado de pool, você pode continuar a abrir apenas as conexões de banco de dados das quais você tem uma licença para o.
-   Você pode configurar o pooling de forma administrativa para tirar a melhor vantagem dos recursos de hardware disponíveis, você pode ajustar facilmente a configuração do pool conforme os recursos de hardware disponíveis mudam.
-   Você pode acelerar o tempo de reativação para objetos que usam a [ativação JIT (just-in-time)](com--just-in-time-activation.md), enquanto controla deliberadamente como os recursos são dedicados aos clientes.

## <a name="writing-poolable-objects"></a>Gravando objetos com pools

Os objetos pooling devem atender a certos requisitos para permitir que uma única instância de objeto seja usada por vários clientes. Por exemplo, eles não podem manter o estado do cliente nem ter nenhuma afinidade de thread. Os objetos transacionais também têm requisitos específicos, pois os recursos gerenciados mantidos por um objeto em pool devem ser inscritos manualmente em uma transação.

Os objetos em pool podem implementar [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) para controlar como eles são reutilizados. Isso permite que eles executem a inicialização quando ativados em um determinado contexto, para limpar qualquer estado do cliente na desativação e para indicar quando eles estão em um estado não reutilizável.

Muitas vezes, é útil escrever objetos com pools de maneira um tanto genérica para que possam ser administrados administrativamente com uma cadeia de caracteres de construtor. Por exemplo, um objeto pode ser escrito para conter uma conexão ODBC genérica, com um DSN específico, de forma administrativa, especificado em uma cadeia de caracteres de construtor.

Os tópicos nesta seção, descritos na tabela a seguir, fornecem informações sobre como o pool de objetos funciona no COM+, bem como informações sobre como escrever, configurar e implementar objetos pooling.



| Tópico                                                                                                 | Descrição                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Como o pool de objetos funciona](how-object-pooling-works.md)<br/>                                   | Apresenta conceitos básicos.<br/>                                                                      |
| [Melhorando o desempenho com o pooling de objetos](improving-performance-with-object-pooling.md)<br/> | Fornece detalhes específicos sobre como você pode usar o pool de objetos com mais eficiência.<br/>                 |
| [Requisitos para objetos pooling](requirements-for-poolable-objects.md)<br/>                 | Fornece detalhes sobre como gravar um objeto que será colocado em pool.<br/>                              |
| [Pooling de objetos transacionais](pooling-transactional-objects.md)<br/>                         | Fornece detalhes sobre os requisitos especiais que se aplicam a objetos transacionais em pool.<br/> |
| [Controlando o tempo de vida e o estado do objeto](controlling-object-lifetime-and-state.md)<br/>         | Descreve como os objetos em pool podem ser implementados para controlar como eles são reutilizados.<br/>               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de pooling de objetos COM+](com--object-pooling-tasks.md)
</dt> </dl>

 

 




