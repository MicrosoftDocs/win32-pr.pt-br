---
description: Para os componentes configurados em execução nos aplicativos COM+, os contextos são a base na qual os serviços COM+ são fornecidos.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: Contextos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0ae1228f89797f9124e817db07f11a23dbec12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370481"
---
# <a name="com-contexts"></a>Contextos COM+

Para os componentes configurados em execução nos aplicativos COM+, os *contextos* são a base na qual os serviços com+ são fornecidos. No COM+, um contexto é definido como um conjunto de propriedades de tempo de execução associadas a um ou mais objetos COM que são usados para fornecer serviços para esses objetos.

No COM+, cada objeto COM é associado a um contexto precisamente à medida que é executado (ou seja, entre sua ativação e desativação), e cada contexto reside em um apartamento COM precisamente. Vários objetos podem ser executados dentro do mesmo contexto e vários contextos podem residir no mesmo apartamento. Inicializado quando um objeto é ativado, as propriedades de contexto, como propriedades de contexto de segurança, representam as necessidades de tempo de execução de um objeto.

> [!Note]  
> Para componentes não configurados que não usam serviços COM+, o contexto é, na maior parte, ignorado.

 

O COM+ usa propriedades de contexto como a base para fornecer serviços em tempo de execução. Essas propriedades mantêm o estado que determina como o ambiente de execução executa serviços para objetos dentro do contexto. Em alguns casos, você pode interagir diretamente com as propriedades de contexto de um objeto para indicar algum estado relevante para um serviço que está sendo fornecido para o objeto. Por exemplo, você faria isso quando um objeto que está participando de um voto automático de transações no resultado da transação.

Para obter uma discussão detalhada da base COM desses conceitos, consulte [processos, threads e Apartments](/windows/desktop/com/processes--threads--and-apartments).

## <a name="programmatic-interaction-with-context-properties"></a>Interação programática com propriedades de contexto

Cada contexto tem um objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) associado que controla suas propriedades. Você pode acessar o **ObjectContext** chamando a função [**getObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) . Depois de ter acessado **ObjectContext**, você pode chamar métodos na interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) que ele expõe para manipular propriedades de contexto.

Por exemplo, chamar [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) tem o efeito de definir o bit de consistência da transação como "consistente" e o bit de [ativação JIT](com--just-in-time-activation.md) realizado para "Done" no contexto associado ao objeto. Sinais "consistentes" para COM+ que você votou para confirmar a transação e "concluído" indicam que o objeto está pronto para ser desativado quando o método retorna.

Além de [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext), outras interfaces especializadas que fornecem acesso às propriedades de contexto são [**IObjectContextInfo**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo), [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)e [**IObjectContextActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity). Para uma determinada extensão, o [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) também acessa as propriedades de contexto. Você pode usar [**IGetSecurityCallContext:: GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) para obter **ISecurityCallContext**.

## <a name="understanding-activation-and-interception"></a>Entendendo a ativação e a interceptação

Em geral, você precisa pensar no contexto somente na medida em que ele representa uma série de propriedades, algumas das quais você pode definir ou obter, que são usadas para fornecer serviços COM+ para seus componentes. Em algumas circunstâncias, no entanto, talvez seja necessário considerar as duas facetas inter-relacionadas de contextos com mais detalhes:

-   [Ativação de contexto](context-activation.md)ou a inicialização de um objeto em um contexto apropriado.
-   [Interceptação](interception-of-cross-context-calls.md)ou o que o com+ faz em chamadas por um limite de contexto.

## <a name="relation-to-mts-context-wrappers"></a>Relação com os wrappers de contexto MTS

Os contextos substituem efetivamente os wrappers de contexto MTS. A finalidade que eles serviam — fornecendo serviços automáticos ao interceptar solicitações de criação — agora é um recurso integrado do COM+. Como resultado, você não precisa mais usar a função [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) . No MTS, o **SafeRef** foi usado para obter uma referência ao seu objeto que poderia ser passado fora do seu wrapper de contexto. No COM+, isso é desnecessário; referências de objetos normais (**esses** ponteiros) funcionam.

 

 
