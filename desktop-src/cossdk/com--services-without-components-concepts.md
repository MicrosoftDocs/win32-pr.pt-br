---
description: O COM+ 1,5 apresenta a capacidade de usar serviços COM+ sem componentes.
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: Conceitos dos serviços COM+ sem componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826607"
---
# <a name="com-services-without-components-concepts"></a>Conceitos dos serviços COM+ sem componentes

O COM+ 1,5 apresenta a capacidade de usar serviços COM+ sem componentes. Isso reduz significativamente os custos de desempenho ao usar os serviços COM+ de um ambiente que não usa componentes e também elimina a complexidade de usar esses serviços. A partir do IIS 6,0, o IIS e o ASP aproveitam o uso de serviços COM+ sem componentes.

Os serviços COM+ foram projetados originalmente para serem usados com componentes COM+. No entanto, alguns ambientes de programação não são baseados em componentes e, portanto, exigiam sobrecarga substancial para usar os serviços COM+. Por exemplo, antes do lançamento do COM+ 1,5, o IIS tinha que criar objetos Shim unicamente para poder usar os serviços de transação COM+ em páginas ASP. Os custos de desempenho que vêm da criação desses objetos incluem o armazenamento dos dados de configuração na metabase do IIS e no banco de dados de registro do COM+ (RegDB), bem como a comunicação extra entre a metabase do IIS e o RegDB do COM+ que é necessário para gerenciar efetivamente os dados de configuração.

Se o IIS precisasse usar um segundo serviço COM+, como a sincronização, ele tinha que criar um objeto de Shim completamente diferente para fazer isso. Para usar as transações COM+ e a sincronização, um terceiro tipo de objeto Shim seria necessário. A complexidade dessa abordagem é dimensionada como O (N2), tornando a implementação de novos serviços extremamente difícil.

Com a introdução dos serviços COM+ sem componentes, os serviços que são necessários são configurados por meio de um objeto instanciado da classe. A classe [**CServiceConfig**](cserviceconfig.md) implementa as interfaces necessárias para configurar os diferentes serviços, fornecendo a flexibilidade para dar suporte a vários serviços ao mesmo tempo e a capacidade de dar suporte a novos serviços no futuro.

Os serviços configurados podem ser usados por meio de dois mecanismos diferentes: eles podem ser usados por meio da função [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) , que aplica os serviços a todo o trabalho enviado por meio da atividade criada pela função e também podem ser usados pela inserção do trabalho que usa os serviços entre chamadas para as funções [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) . Nenhuma dessas funções requer a criação de novos componentes para poder usar os serviços COM+; somente o objeto [**CServiceConfig**](cserviceconfig.md) é necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços COM+ sem tarefas de componentes](com--services-without-components-tasks.md)
</dt> </dl>

 

 



