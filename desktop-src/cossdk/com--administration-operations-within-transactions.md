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
# <a name="com-administration-operations-within-transactions"></a><span data-ttu-id="6d42b-103">Operações de administração COM+ em transações</span><span class="sxs-lookup"><span data-stu-id="6d42b-103">COM+ Administration Operations Within Transactions</span></span>

<span data-ttu-id="6d42b-104">O banco de dados de registro do COM+ (RegDB) é um Gerenciador de recursos transacionado que pode participar de transações COM+.</span><span class="sxs-lookup"><span data-stu-id="6d42b-104">The COM+ registration database (RegDB) is a transacted resource manager that can participate in COM+ transactions.</span></span> <span data-ttu-id="6d42b-105">Isso permite que você execute operações de administração em uma transação e que todas as alterações de configuração sejam confirmadas ou anuladas como uma operação atômica, mesmo em vários computadores.</span><span class="sxs-lookup"><span data-stu-id="6d42b-105">This enables you to perform administration operations within a transaction and have all configuration changes committed or aborted as an atomic operation, even across multiple computers.</span></span> <span data-ttu-id="6d42b-106">Em algumas circunstâncias, pode ser muito benéfico fazer isso, embora haja um comportamento de isolamento e bloqueio que você deve levar em conta, e executar tarefas de administração dentro de transações envolve pequenas alterações no modelo de programação de administração normal.</span><span class="sxs-lookup"><span data-stu-id="6d42b-106">In some circumstances, it can be very beneficial to do this, although there is isolation and blocking behavior that you should take into account, and performing administration tasks within transactions does involve slight changes to the normal administration programming model.</span></span>

## <a name="benefits-of-doing-administration-operations-within-transactions"></a><span data-ttu-id="6d42b-107">Benefícios da realização de operações de administração em transações</span><span class="sxs-lookup"><span data-stu-id="6d42b-107">Benefits of Doing Administration Operations Within Transactions</span></span>

-   <span data-ttu-id="6d42b-108">**Consistência dos dados —** As operações de administração executadas em uma transação são confirmadas ou anuladas como um todo, embora haja alguns recursos de catálogo COM+ não transacionais para os quais esse pode não ser o caso.</span><span class="sxs-lookup"><span data-stu-id="6d42b-108">**Consistency of data—** Administration operations performed within a transaction are committed or aborted as a whole, although there are some non-transactional COM+ catalog resources for which this may not be the case.</span></span> <span data-ttu-id="6d42b-109">(Consulte recursos de catálogo COM+ não transacionais abaixo.)</span><span class="sxs-lookup"><span data-stu-id="6d42b-109">(See Non-Transactional COM+ Catalog Resources below.)</span></span>
-   <span data-ttu-id="6d42b-110">**Implantação consistente em vários computadores —** Se você estiver implantando aplicativos COM+ em vários servidores, poderá garantir que todos os servidores sejam mantidos com configurações idênticas.</span><span class="sxs-lookup"><span data-stu-id="6d42b-110">**Consistent deployment across multiple machines—** If you are deploying COM+ applications across multiple servers, you can guarantee that all servers are left with identical configurations.</span></span>
-   <span data-ttu-id="6d42b-111">**Dimensionamento e desempenho —** Quando você realiza várias operações em uma transação, todas as gravações em RegDB são executadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6d42b-111">**Scaling and performance—** When you do multiple operations within a transaction, all writes to RegDB are performed at once.</span></span> <span data-ttu-id="6d42b-112">As gravações persistentes no RegDB são uma operação relativamente cara; Se você estiver fazendo muitas gravações no RegDB, poderá obter um grande benefício de desempenho para fazer todas elas de uma só vez, em vez de cada vez que chamar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span><span class="sxs-lookup"><span data-stu-id="6d42b-112">Persisted writes to RegDB are a relatively expensive operation; if you are making many writes to RegDB, you can get a big performance benefit from doing them all at once instead of every time you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span></span>

## <a name="isolation-behavior-of-regdb"></a><span data-ttu-id="6d42b-113">Comportamento de isolamento de RegDB</span><span class="sxs-lookup"><span data-stu-id="6d42b-113">Isolation Behavior of RegDB</span></span>

<span data-ttu-id="6d42b-114">Para garantir a consistência de dados adequada e as transações serializáveis, o RegDB impõe o comportamento específico de bloqueio e isolamento quando as operações de administração estão sendo executadas em transações.</span><span class="sxs-lookup"><span data-stu-id="6d42b-114">To ensure proper data consistency and serializable transactions, RegDB enforces particular blocking and isolation behavior when administration operations are being performed within transactions.</span></span>

<span data-ttu-id="6d42b-115">Sempre que um componente que está trabalhando em uma transação chama qualquer método que fará uma gravação no catálogo COM+ — como [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)ou [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)— um bloqueio de gravador é obtido no código do servidor de catálogo com+ que bloqueará a entrada de qualquer outro gravador até que a transação atual seja confirmada ou anulada.</span><span class="sxs-lookup"><span data-stu-id="6d42b-115">Whenever a component that is doing work within a transaction calls any method that will cause a write to the COM+ catalog—such as [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication), or [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)—a writer lock is taken on COM+ catalog server code that will block any other writers from coming in until the current transaction commits or aborts.</span></span> <span data-ttu-id="6d42b-116">Ou seja, os gravadores podem se originar apenas se tiverem a afinidade de transação correta e estiverem participando da transação atual.</span><span class="sxs-lookup"><span data-stu-id="6d42b-116">That is, writers can come in only if they have the correct transaction affinity and are participating in the current transaction.</span></span>

<span data-ttu-id="6d42b-117">Os leitores não estão bloqueados.</span><span class="sxs-lookup"><span data-stu-id="6d42b-117">Readers are not blocked.</span></span> <span data-ttu-id="6d42b-118">No entanto, os dados que os leitores veem não refletem nenhuma alteração provisória feita dentro da transação até que a transação seja realmente confirmada.</span><span class="sxs-lookup"><span data-stu-id="6d42b-118">However, the data that readers see does not reflect any interim changes made within the transaction until that transaction actually commits.</span></span> <span data-ttu-id="6d42b-119">Todos os componentes que participam dessa transação veem os Estados de dados provisórios quando eles lêem dados, mas todos os componentes fora da transação veem essas alterações somente após a conclusão da transação.</span><span class="sxs-lookup"><span data-stu-id="6d42b-119">Any components participating in that transaction sees interim data states when they read data, but all components outside the transaction see those changes only after the transaction has completed.</span></span>

## <a name="savechanges-behavior"></a><span data-ttu-id="6d42b-120">Comportamento de SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6d42b-120">SaveChanges Behavior</span></span>

<span data-ttu-id="6d42b-121">Para obter o comportamento de isolamento descrito acima, o RegDB efetivamente fornece um cache que é acionado por componentes dentro da transação.</span><span class="sxs-lookup"><span data-stu-id="6d42b-121">To achieve the isolation behavior described above, RegDB effectively provides a cache that is acted on by components within the transaction.</span></span> <span data-ttu-id="6d42b-122">Isso altera o comportamento do método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="6d42b-122">This changes the behavior of the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method.</span></span>

<span data-ttu-id="6d42b-123">Normalmente, sem a presença de uma transação, todas as alterações pendentes são gravadas no catálogo quando você chama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), e **SaveChanges** não retorna até que todas as gravações sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="6d42b-123">Normally, without the presence of a transaction, any pending changes are written to the catalog when you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), and **SaveChanges** doesn't return until all writes are completed.</span></span> <span data-ttu-id="6d42b-124">Isso garante que, se uma chamada para **SaveChanges** retornar com êxito, você poderá chamar [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) e ele ativará o aplicativo com dados atualizados.</span><span class="sxs-lookup"><span data-stu-id="6d42b-124">This guarantees that if a call to **SaveChanges** returns successfully, you can call [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) and it will activate the application with fresh data.</span></span>

<span data-ttu-id="6d42b-125">No entanto, em uma transação, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) afeta apenas o cache, não o próprio RegDB, e o **SaveChanges** retorna imediatamente se todas as alterações foram transacionalmente confirmadas em RegDB.</span><span class="sxs-lookup"><span data-stu-id="6d42b-125">However, within a transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affects only the cache, not the RegDB itself, and **SaveChanges** returns immediately whether all changes have been transactionally committed to RegDB.</span></span> <span data-ttu-id="6d42b-126">Não há nenhuma garantia de que o [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) está usando dados atualizados subsequentemente para o retorno de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="6d42b-126">There is no guarantee that [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) is using fresh data subsequent to **SaveChanges** returning.</span></span> <span data-ttu-id="6d42b-127">Se você precisar chamar **StartApplication** nesse contexto, é aconselhável aguardar um período de tempo antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6d42b-127">If you need to call **StartApplication** in this context, it is advisable to wait for some period of time before doing so.</span></span>

## <a name="transaction-time-out-period"></a><span data-ttu-id="6d42b-128">Período de Time-Out da transação</span><span class="sxs-lookup"><span data-stu-id="6d42b-128">Transaction Time-Out Period</span></span>

<span data-ttu-id="6d42b-129">Se você estiver fazendo várias operações de administração em uma transação, pode ser uma transação de longa execução.</span><span class="sxs-lookup"><span data-stu-id="6d42b-129">If you are doing numerous administration operations within a transaction, it may be a long running transaction.</span></span> <span data-ttu-id="6d42b-130">Nesse caso, o valor de tempo limite da transação pode ser um problema.</span><span class="sxs-lookup"><span data-stu-id="6d42b-130">In this case, the transaction time-out value can be an issue.</span></span> <span data-ttu-id="6d42b-131">Isso é determinado pelo valor de tempo limite da transação definido para o componente que inicia a transação ou pela configuração de tempo limite de todo o computador para o computador em que o componente está em execução.</span><span class="sxs-lookup"><span data-stu-id="6d42b-131">This is determined either by the transaction time-out value set for the component initiating the transaction or by the machine-wide time-out setting for the machine where that component is running.</span></span> <span data-ttu-id="6d42b-132">Se você estiver fazendo inúmeras operações em uma transação, é aconselhável definir o período de tempo limite da transação apropriado para um valor suficientemente longo e, se necessário, para restaurar a configuração original quando terminar.</span><span class="sxs-lookup"><span data-stu-id="6d42b-132">If you are doing numerous operations within a transaction, it is advisable to set the appropriate transaction time-out period to a sufficiently long value and, if necessary, to restore the original setting when you are finished.</span></span>

## <a name="non-transactional-com-catalog-resources"></a><span data-ttu-id="6d42b-133">Recursos de catálogo COM+ não transacionais</span><span class="sxs-lookup"><span data-stu-id="6d42b-133">Non-Transactional COM+ Catalog Resources</span></span>

<span data-ttu-id="6d42b-134">O registro, o sistema de arquivos e o Windows Installer (MSI) são recursos de catálogo COM+ que não são transacionais.</span><span class="sxs-lookup"><span data-stu-id="6d42b-134">The registry, the file system, and Windows Installer (MSI) are COM+ catalog resources that are not transactional.</span></span>

> [!Note]  
> <span data-ttu-id="6d42b-135">Se houver um erro que anule uma transação, as alterações nesses recursos não poderão ser revertidas.</span><span class="sxs-lookup"><span data-stu-id="6d42b-135">If there is an error that aborts a transaction, changes to these resources may not be rolled back.</span></span>

 

<span data-ttu-id="6d42b-136">Se houver um erro durante a instalação de um aplicativo COM+ existente a partir de um arquivo. msi, o aplicativo não aparecerá no snap-in Serviços de componentes, mas poderá aparecer em Adicionar ou remover programas, caso em que você precisa removê-lo manualmente.</span><span class="sxs-lookup"><span data-stu-id="6d42b-136">If there is an error while installing an existing COM+ application from an .msi file, the application doesn't appear in the Component Services snap-in but it might appear in Add/Remove programs, in which case you need to manually remove it.</span></span>

## <a name="recovering-in-the-event-of-system-hangs"></a><span data-ttu-id="6d42b-137">Recuperando no caso de travamentos do sistema</span><span class="sxs-lookup"><span data-stu-id="6d42b-137">Recovering in the Event of System Hangs</span></span>

<span data-ttu-id="6d42b-138">Se um componente que está realizando operações de administração em uma transação fosse paralisado enquanto contém um bloqueio de gravador no código do servidor de catálogo, ele bloquearia qualquer outra coisa de fazer qualquer alteração no catálogo.</span><span class="sxs-lookup"><span data-stu-id="6d42b-138">If a component doing administration operations within a transaction were to hang while it holds a writer lock on the catalog server code, it would block everyone else from making any changes to the catalog.</span></span> <span data-ttu-id="6d42b-139">Se isso acontecer, você poderá limpar o bloqueio no catálogo desligando e reiniciando o aplicativo do sistema.</span><span class="sxs-lookup"><span data-stu-id="6d42b-139">Should this happen, you can clear the lock on the catalog by shutting down and restarting the System application.</span></span>

## <a name="scripting-with-a-transactioncontext-object"></a><span data-ttu-id="6d42b-140">Criando scripts com um objeto TransactionContext</span><span class="sxs-lookup"><span data-stu-id="6d42b-140">Scripting with a TransactionContext Object</span></span>

<span data-ttu-id="6d42b-141">Uma maneira simples de realizar operações de administração em transações é usar um objeto [**TransactionContext**](transactioncontext.md) para controlar a transação.</span><span class="sxs-lookup"><span data-stu-id="6d42b-141">A simple way to do administration operations within transactions is to use a [**TransactionContext**](transactioncontext.md) object to control the transaction.</span></span> <span data-ttu-id="6d42b-142">Por exemplo, o script de Visual Basic a seguir demonstra como adicionar transacionalmente dois novos aplicativos para que ambos os aplicativos ou nenhum dos aplicativos sejam criados:</span><span class="sxs-lookup"><span data-stu-id="6d42b-142">For example, the following Visual Basic script demonstrates how to transactionally add two new applications so that either both applications or neither application is created:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6d42b-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d42b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d42b-144">Manipulando erros de administração COM+</span><span class="sxs-lookup"><span data-stu-id="6d42b-144">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="6d42b-145">Exemplo introdutório usando o catálogo de administração do COM+</span><span class="sxs-lookup"><span data-stu-id="6d42b-145">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="6d42b-146">Visão geral dos objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="6d42b-146">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="6d42b-147">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="6d42b-147">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="6d42b-148">Definindo propriedades e salvando alterações no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="6d42b-148">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



