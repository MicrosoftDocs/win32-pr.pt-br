---
description: Os componentes de aplicativo usam o dispensador de recursos COM+ para acessar e gerenciar informações de estado não duráveis, como conexões entre componentes e um Gerenciador de recursos específico.
ms.assetid: 252c7180-61b1-485d-883d-36bf77357a29
title: Conceitos do dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0fcf281d6d7b8ed0e087b6d77e4d686e28e1fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646291"
---
# <a name="com-resource-dispenser-concepts"></a>Conceitos do dispensador de recursos COM+

Os componentes de aplicativo usam o dispensador de recursos COM+ para acessar e gerenciar informações de estado não duráveis, como conexões entre componentes e um Gerenciador de recursos específico. Em tempo de execução, pools dinâmicos de recursos, como conexões de banco de dados, conexões de rede, conexões a filas, threads, objetos e blocos de memória, são disponibilizados para o dispensador de recurso. O processo do aplicativo alcança alto desempenho usando um número mínimo de recursos usados com frequência. O dispensador de recursos também pode automatizar transações e reclamações. (Consulte [recuperação automática de recursos](automatic-resource-reclamation.md) para obter mais informações sobre esse recurso.)

> [!Note]  
> Um *recurso* é qualquer coisa que um dispensador de recurso cria. Por exemplo, uma conexão com um Gerenciador de recursos é um recurso comum. Os recursos residem na memória do dispensador de recursos e nunca são copiados para o Gerenciador do dispensador. Um recurso é conhecido apenas por um identificador opaco (**Resid**) e pode ou não ser capaz de executar transações. Embora os recursos gerenciados possam muitas vezes ser conexões com um componente que gerencia um estado durável, as próprias conexões não são duráveis. Um dispensador de recursos geralmente usa um Gerenciador de recursos relacionado para manter o estado durável.

 

Em termos de arquitetura, o sistema do dispensador de recursos COM+ consiste em dispensadores de recursos e um Gerenciador de dispensadores. Os dispensadores de recursos são componentes fornecidos pelo usuário que fornecem aplicativos com interfaces simples para recursos compartilhados. O Gerenciador do dispensador é um componente fornecido pelo COM+ que coordena as atividades de vários dispensadores de recursos.

Um dispensador de recurso é um componente DLL (biblioteca de vínculo dinâmico) que fornece pelo menos duas interfaces. A primeira, [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver), fornece ao Gerenciador de dispensadores informações básicas sobre como criar, destruir e inscrever os recursos que ele gerencia. O segundo é exposto aos aplicativos e pode ser uma interface COM ou um conjunto de interfaces ou pode ser uma API (interface de programação de aplicativo) para a qual um componente está vinculado por meio de uma biblioteca de importação. Um aplicativo pode chamar qualquer dispensador de recursos que, por sua vez, pode oferecer qualquer API para o aplicativo. Se o dispensador de recursos for um componente de automação, ele poderá ser acessado do Microsoft Visual Basic. Um dispensador de recurso é instanciado quando um componente de aplicativo faz referência a ele.

O Gerenciador do dispensador fornecido pelo COM+ controla os dispensadores de recursos e as coordenadas entre eles. Ele implementa duas interfaces: [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) e [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder). os dispensadores de recursos se registram usando a interface **IDispenserManager** . Em seguida, o Gerenciador do dispensador dá a eles um ponteiro para um **IHolder** que eles usam para notificar o gerente do dispensador sobre suas atividades.

Um dispensador de recursos transacionais deve se inscrever em uma transação Coordenador de Transações Distribuídas (DTC). Isso implica o uso de um Gerenciador de recursos interno ou externo (para o dispensador de recursos) que é compatível com transações OLE.

> [!Note]  
> O modelo de programação COM+ inclui *Transações declarativas*, que ajudam a proteger o trabalho executado por um objeto de aplicativo durante seu tempo de vida. Quando um objeto de aplicativo usa um dispensador de recursos COM+, o trabalho que ele executa é transacional automaticamente; ou seja, o componente não precisa declarar explicitamente as transações. Essas transações são definidas na especificação de transações OLE, implementadas pelo DTC e iniciadas em nome do objeto de aplicativo por COM+. Consulte o guia de desenvolvimento do DTC para obter mais informações.

 

Os recursos não precisam ser transacionais. Um dispensador de recursos que agrupa recursos não transacionais ainda pode alcançar alto desempenho, permitindo que os objetos de aplicativo acessem um pool compartilhado desses recursos. Esse tipo de dispensador de recurso retorna S \_ false do método [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) , o que significa que o dispensador de recurso não inscreveu o recurso porque o recurso não é transacional.

O dispensador de recursos também pode funcionar independentemente do COM+, fornecendo apenas recursos de pool de recursos. Por exemplo, se um dispensador de recursos expõe uma API (como ODBC), o dispensador de recursos pode ser uma DLL que é acessada pelo aplicativo por meio de uma biblioteca de importação (ou usando as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ). Um dispensador de recurso também pode ser um componente COM que um aplicativo acessa chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Sem o COM+, um método [**EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) do dispensador de recursos nunca pode ser chamado porque o Gerenciador do dispensador não tem conhecimento da transação do componente atual.

Na inicialização, uma DLL de dispensador de recurso deve se registrar com o Gerenciador do dispensador. O Gerenciador do dispensador é o executivo de controle que gerencia o carregamento e o descarregamento de dispensadores de recursos, fornece o contexto COM+ e controla o Gerenciador de estatísticas de inventário. (Para obter mais informações, consulte [Gerenciador do dispensador do com+](com--dispenser-manager.md).) O dispensador de recurso primeiro chama a função [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) e, em seguida, chama o método [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser) , passando o ponteiro [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) que o dispensador de recurso implementa. Essa chamada retorna uma referência a [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder).

Para desligar, um dispensador de recurso chama [**IHolder:: Close**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-close). Para garantir um desligamento limpo do pacote, um dispensador de recursos deve ser capaz de lidar com a situação em que as chamadas continuam a chegar de objetos comerciais depois que o COM+ pediu para o desligamento do dispensador.

Os tópicos a seguir nesta seção fornecem informações mais detalhadas sobre o serviço do dispensador de recursos COM+:

-   [Gerenciador do dispensador COM+](com--dispenser-manager.md)
-   [Tipos de thread do dispensador de recursos COM+](com--resource-dispenser-thread-types.md)
-   [Estados de recursos em pool disponíveis para o dispensador de recursos COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
-   [Inlistando um recurso em uma transação](enlisting-a-resource-in-a-transaction.md)
-   [Processo de alocação de recursos do dispensador de recursos](resource-dispenser-resource-allocation-process.md)
-   [Controlando recursos não alocados](tracking-non-allocated-resources.md)
-   [Recuperação automática de recursos](automatic-resource-reclamation.md)
-   [Tipos usados em interfaces de dispensador de recursos COM+](types-used-in-com--resource-dispenser-interfaces.md)
-   [Interfaces do dispensador de recursos COM+](com--resource-dispenser-interfaces.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do dispensador de recursos COM+](com--resource-dispenser-tasks.md)
</dt> </dl>

 

 
