---
description: É recomendável que todas as assinaturas permanentes sejam compiladas no \\ \\ namespace da assinatura raiz.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implementando assinaturas de eventos permanentes de namespace cruzado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52771e40d4dfb036354c3b37b562b32edd3034ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762150"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>Implementando assinaturas de eventos permanentes de namespace cruzado

É recomendável que todas as assinaturas permanentes sejam compiladas no \\ \\ namespace da assinatura raiz. Isso impede a necessidade de compilar o consumidor permanente em cada namespace que está sendo usado, o que significa que há apenas um namespace para procurar assinaturas permanentes. Use a propriedade **EventNamespace** de [**\_ \_ EventFilter**](--eventfilter.md) para implementar uma assinatura de namespace cruzado.

Ao usar o [**CommandLineEventConsumer**](commandlineeventconsumer.md), é importante proteger o executável que você está iniciando. Se o executável não estiver em um local seguro, ou protegido com uma ACL (lista de controle de acesso) forte, qualquer pessoa poderá substituir seu executável por um de seus próprios. Para obter mais informações sobre ACLs, consulte [criando um descritor de segurança para um novo objeto em C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

O exemplo de código de formato MOF (MOF) a seguir mostra uma assinatura de namespace cruzado.

``` syntax
#pragma namespace("\\root\\subscription")

instance of __EventFilter as $FLT
{
  Name = "Filter";
  Query = "SELECT * FROM __InstanceModificationEvent "
          "WHERE TargetInstance ISA \"Win32_LocalTime\" "
          "AND TargetInstance.Hour = 8 "
          "AND TargetInstance.Minute = 0 "
          "AND TargetInstance.Second = 0 "
          "AND TargetInstance.DayOfWeek = 6";
  QueryLanguage = "WQL";
  EventNamespace = "root\\cimv2";
};

instance of CommandLineEventConsumer as $CONS
{
  ExecutablePath = "cmd.exe";
  ShowWindowCommand = 7;
  RunInteractively = true;
};

instance of __FilterToConsumerBinding
{
  Consumer = $CONS;
  Filter = $FLT;
};
```

 

 
