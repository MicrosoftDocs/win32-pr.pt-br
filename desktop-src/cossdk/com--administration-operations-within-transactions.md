---
description: Operações de administração COM+ em transações
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Operações de administração COM+ em transações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21612ffec1b9f082dc6a91861882a71f18fb07be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646548"
---
# <a name="com-administration-operations-within-transactions"></a>Operações de administração COM+ em transações

O banco de dados de registro do COM+ (RegDB) é um Gerenciador de recursos transacionado que pode participar de transações COM+. Isso permite que você execute operações de administração em uma transação e que todas as alterações de configuração sejam confirmadas ou anuladas como uma operação atômica, mesmo em vários computadores. Em algumas circunstâncias, pode ser muito benéfico fazer isso, embora haja um comportamento de isolamento e bloqueio que você deve levar em conta, e executar tarefas de administração dentro de transações envolve pequenas alterações no modelo de programação de administração normal.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Benefícios da realização de operações de administração em transações

-   **Consistência dos dados —** As operações de administração executadas em uma transação são confirmadas ou anuladas como um todo, embora haja alguns recursos de catálogo COM+ não transacionais para os quais esse pode não ser o caso. (Consulte recursos de catálogo COM+ não transacionais abaixo.)
-   **Implantação consistente em vários computadores —** Se você estiver implantando aplicativos COM+ em vários servidores, poderá garantir que todos os servidores sejam mantidos com configurações idênticas.
-   **Dimensionamento e desempenho —** Quando você realiza várias operações em uma transação, todas as gravações em RegDB são executadas ao mesmo tempo. As gravações persistentes no RegDB são uma operação relativamente cara; Se você estiver fazendo muitas gravações no RegDB, poderá obter um grande benefício de desempenho para fazer todas elas de uma só vez, em vez de cada vez que chamar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).

## <a name="isolation-behavior-of-regdb"></a>Comportamento de isolamento de RegDB

Para garantir a consistência de dados adequada e as transações serializáveis, o RegDB impõe o comportamento específico de bloqueio e isolamento quando as operações de administração estão sendo executadas em transações.

Sempre que um componente que está trabalhando em uma transação chama qualquer método que fará uma gravação no catálogo COM+ — como [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)ou [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)— um bloqueio de gravador é obtido no código do servidor de catálogo com+ que bloqueará a entrada de qualquer outro gravador até que a transação atual seja confirmada ou anulada. Ou seja, os gravadores podem se originar apenas se tiverem a afinidade de transação correta e estiverem participando da transação atual.

Os leitores não estão bloqueados. No entanto, os dados que os leitores veem não refletem nenhuma alteração provisória feita dentro da transação até que a transação seja realmente confirmada. Todos os componentes que participam dessa transação veem os Estados de dados provisórios quando eles lêem dados, mas todos os componentes fora da transação veem essas alterações somente após a conclusão da transação.

## <a name="savechanges-behavior"></a>Comportamento de SaveChanges

Para obter o comportamento de isolamento descrito acima, o RegDB efetivamente fornece um cache que é acionado por componentes dentro da transação. Isso altera o comportamento do método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .

Normalmente, sem a presença de uma transação, todas as alterações pendentes são gravadas no catálogo quando você chama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), e **SaveChanges** não retorna até que todas as gravações sejam concluídas. Isso garante que, se uma chamada para **SaveChanges** retornar com êxito, você poderá chamar [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) e ele ativará o aplicativo com dados atualizados.

No entanto, em uma transação, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) afeta apenas o cache, não o próprio RegDB, e o **SaveChanges** retorna imediatamente se todas as alterações foram transacionalmente confirmadas em RegDB. Não há nenhuma garantia de que o [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) está usando dados atualizados subsequentemente para o retorno de **SaveChanges** . Se você precisar chamar **StartApplication** nesse contexto, é aconselhável aguardar um período de tempo antes de fazer isso.

## <a name="transaction-time-out-period"></a>Período de Time-Out da transação

Se você estiver fazendo várias operações de administração em uma transação, pode ser uma transação de longa execução. Nesse caso, o valor de tempo limite da transação pode ser um problema. Isso é determinado pelo valor de tempo limite da transação definido para o componente que inicia a transação ou pela configuração de tempo limite de todo o computador para o computador em que o componente está em execução. Se você estiver fazendo inúmeras operações em uma transação, é aconselhável definir o período de tempo limite da transação apropriado para um valor suficientemente longo e, se necessário, para restaurar a configuração original quando terminar.

## <a name="non-transactional-com-catalog-resources"></a>Recursos de catálogo COM+ não transacionais

O registro, o sistema de arquivos e o Windows Installer (MSI) são recursos de catálogo COM+ que não são transacionais.

> [!Note]  
> Se houver um erro que anule uma transação, as alterações nesses recursos não poderão ser revertidas.

 

Se houver um erro durante a instalação de um aplicativo COM+ existente a partir de um arquivo. msi, o aplicativo não aparecerá no snap-in Serviços de componentes, mas poderá aparecer em Adicionar ou remover programas, caso em que você precisa removê-lo manualmente.

## <a name="recovering-in-the-event-of-system-hangs"></a>Recuperando no caso de travamentos do sistema

Se um componente que está realizando operações de administração em uma transação fosse paralisado enquanto contém um bloqueio de gravador no código do servidor de catálogo, ele bloquearia qualquer outra coisa de fazer qualquer alteração no catálogo. Se isso acontecer, você poderá limpar o bloqueio no catálogo desligando e reiniciando o aplicativo do sistema.

## <a name="scripting-with-a-transactioncontext-object"></a>Criando scripts com um objeto TransactionContext

Uma maneira simples de realizar operações de administração em transações é usar um objeto [**TransactionContext**](transactioncontext.md) para controlar a transação. Por exemplo, o script de Visual Basic a seguir demonstra como adicionar transacionalmente dois novos aplicativos para que ambos os aplicativos ou nenhum dos aplicativos sejam criados:


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

[Manipulando erros de administração COM+](handling-com--administration-errors.md)
</dt> <dt>

[Exemplo introdutório usando o catálogo de administração do COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



