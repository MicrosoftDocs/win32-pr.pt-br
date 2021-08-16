---
description: Operações de administração COM+ em transações
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Operações de administração COM+ em transações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4182b143de38d838aea7c5aabd2d91bdb84f94480b2bed4c4441e204412ac834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308245"
---
# <a name="com-administration-operations-within-transactions"></a>Operações de administração COM+ em transações

O RegDB (banco de dados de registro COM+) é um gerenciador de recursos transacionado que pode participar de transações COM+. Isso permite executar operações de administração em uma transação e ter todas as alterações de configuração confirmados ou anulados como uma operação atômica, mesmo em vários computadores. Em algumas circunstâncias, pode ser muito útil fazer isso, embora haja um comportamento de isolamento e bloqueio que você deve levar em conta e a execução de tarefas de administração em transações envolva pequenas alterações no modelo de programação de administração normal.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Benefícios de fazer operações de administração em transações

-   **Consistência de dados—** As operações de administração executadas em uma transação são comprometidas ou anuladas como um todo, embora haja alguns recursos de catálogo COM+ não transacionais para os quais isso pode não ser o caso. (Consulte Recursos de catálogo COM+ não transacionais abaixo.)
-   **Implantação consistente em vários máquinas—** Se você estiver implantando aplicativos COM+ em vários servidores, poderá garantir que todos os servidores sejam deixados com configurações idênticas.
-   **Dimensionamento e desempenho—** Quando você faz várias operações em uma transação, todas as gravações no RegDB são executadas ao mesmo tempo. As gravações persistentes no RegDB são uma operação relativamente cara; Se você estiver fazendo muitas gravações no RegDB, poderá obter um grande benefício de desempenho ao fazer todas de uma vez, em vez de sempre que chamar [**SaveChanges.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)

## <a name="isolation-behavior-of-regdb"></a>Comportamento de isolamento do RegDB

Para garantir a consistência de dados adequada e transações serializáveis, o RegDB impõe um comportamento específico de bloqueio e isolamento quando as operações de administração estão sendo executadas em transações.

Sempre que um componente que está fazendo trabalho em uma transação chama qualquer método que causará uma gravação no catálogo COM+, como [**SaveChanges,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)ou [**InstallComponent,**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)um bloqueio de gravação é feito no código do servidor do catálogo COM+, que impedirá que qualquer outro autor entre até que a transação atual seja confirmada ou anulada. Ou seja, os autores poderão entrar somente se eles têm a afinidade de transação correta e estão participando da transação atual.

Os leitores não estão bloqueados. No entanto, os dados que os leitores veem não refletem nenhuma alteração provisória feita dentro da transação até que essa transação seja realmente confirmada. Todos os componentes que participam dessa transação veem estados de dados provisórios quando leem dados, mas todos os componentes fora da transação veem essas alterações somente após a conclusão da transação.

## <a name="savechanges-behavior"></a>Comportamento de SaveChanges

Para obter o comportamento de isolamento descrito acima, o RegDB fornece efetivamente um cache que é agido pelos componentes dentro da transação. Isso altera o comportamento do [**método SaveChanges.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)

Normalmente, sem a presença de uma transação, todas as alterações pendentes são escritas no catálogo quando você chama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)e **SaveChanges** não retorna até que todas as gravações sejam concluídas. Isso garante que, se uma chamada para **SaveChanges** for retornada com êxito, você poderá chamar [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) e ela ativará o aplicativo com dados atualizados.

No entanto, em uma transação, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) afeta apenas o cache, não o RegDB em si, e **SaveChanges** retorna imediatamente se todas as alterações foram transaticamente comprometidas com RegDB. Não há nenhuma garantia de [**que StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) está usando dados atualizados subsequentes **ao retorno de SaveChanges.** Se você precisar chamar **StartApplication** nesse contexto, é aconselhável aguardar algum período antes de fazer isso.

## <a name="transaction-time-out-period"></a>Período de Time-Out transação

Se você estiver fazendo várias operações de administração dentro de uma transação, pode ser uma transação de execução longa. Nesse caso, o valor de tempo-máximo da transação pode ser um problema. Isso é determinado pelo valor de tempo-de-execução da transação definido para o componente que inicia a transação ou pela configuração de tempo-out em todo o computador para o computador em que o componente está sendo executado. Se você estiver fazendo várias operações dentro de uma transação, é aconselhável definir o período de tempo de tempo de transação apropriado para um valor suficientemente longo e, se necessário, restaurar a configuração original quando terminar.

## <a name="non-transactional-com-catalog-resources"></a>Recursos de catálogo COM+ não transacionais

O registro, o sistema de arquivos e Windows instalador (MSI) são recursos de catálogo COM+ que não são transacionais.

> [!Note]  
> Se houver um erro que anula uma transação, as alterações nesses recursos poderão não ser re roleadas.

 

Se houver um erro durante a instalação de um aplicativo COM+ existente de um arquivo .msi, o aplicativo não aparecerá no snap-in serviços de componentes, mas poderá aparecer nos programas Adicionar/Remover, caso em que você precisará removê-lo manualmente.

## <a name="recovering-in-the-event-of-system-hangs"></a>Recuperação no evento de travas do sistema

Se um componente que realiza operações de administração dentro de uma transação travasse enquanto mantém um bloqueio de autor no código do servidor do catálogo, ele impediria que todos os outros realizasse alterações no catálogo. Se isso acontecer, você poderá limpar o bloqueio no catálogo desligando e reiniciando o aplicativo System.

## <a name="scripting-with-a-transactioncontext-object"></a>Script com um objeto TransactionContext

Uma maneira simples de fazer operações de administração em transações é usar um [**objeto TransactionContext**](transactioncontext.md) para controlar a transação. Por exemplo, o script Visual Basic a seguir demonstra como adicionar transaticamente dois novos aplicativos para que ambos os aplicativos ou nenhum aplicativo seja criado:


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratando erros de administração COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemplo introdutório usando o catálogo de administração COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



