---
description: 'Antes de se registrar para receber um evento, você deve determinar os tipos de eventos a serem recebidos: intrínseco ou extrínsecos.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Determinando o tipo de evento a ser recebido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9172e3246a31cb42ada3b9f5099bc3b0575959c125dedd44d7c6ed745134a4a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374646"
---
# <a name="determining-the-type-of-event-to-receive"></a>Determinando o tipo de evento a ser recebido

Antes de se registrar para receber um evento, você deve determinar os tipos de eventos a serem recebidos: [intrínseco](#intrinsic-events) ou [extrínsecos](#extrinsic-events). Para obter mais informações sobre como receber eventos, consulte [recebendo um evento WMI](receiving-a-wmi-event.md). Para obter mais informações sobre como fornecer eventos, consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md) e [gravando um provedor de eventos](writing-an-event-provider.md). Para obter mais informações sobre as preocupações de segurança para receber e fornecer eventos, consulte [SECURING WMI Events.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Eventos intrínsecos

Um evento intrínseco é um evento que ocorre em resposta a uma alteração no modelo de dados padrão do WMI. Cada classe de evento intrínseca representa um tipo específico de alteração e ocorre quando o WMI ou um provedor cria, exclui ou modifica um namespace, classe ou instância de classe. Por exemplo, a criação de uma instância do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) resultaria em uma instância de [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) .

O WMI cria eventos intrínsecos para objetos armazenados no repositório WMI. Um provedor gera eventos intrínsecos para classes dinâmicas, mas o WMI pode criar uma instância para uma classe dinâmica se nenhum provedor estiver disponível. O WMI usa a sondagem para detectar as alterações. A tabela a seguir lista as classes de sistema que o WMI usa para relatar eventos intrínsecos.



| Classe do sistema                                                           | Descrição                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | Notifica um consumidor quando uma classe é criada.                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | Notifica um consumidor quando uma classe é excluída.                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | Notifica um consumidor quando uma classe é modificada.                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | Notifica um consumidor quando uma instância de classe é criada.                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | Notifica um consumidor quando ocorre um evento de instância, como criação, exclusão ou modificação da instância. Você pode usar essa classe em consultas para obter todos os eventos de tipos associados a uma instância. |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | Notifica um consumidor quando uma instância é excluída.                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | Notifica um consumidor quando uma instância é modificada.                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | Notifica um consumidor quando um namespace é criado.                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | Notifica um consumidor quando um namespace é excluído.                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | Notifica um consumidor quando um namespace é modificado.                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | Notifica um consumidor quando algum outro evento é Descartado devido a uma falha na parte de um consumidor de evento.                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | Notifica um consumidor quando algum outro evento é Descartado em vez de ser entregue ao consumidor de evento solicitante.                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | Notifica um consumidor quando um evento é Descartado como resultado de um estouro de fila de entrega.                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | Notifica um consumidor quando ocorre um evento de chamada de método.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Eventos extrínsecos

Um evento extrínsecos é uma ocorrência predefinida que não pode ser vinculada diretamente a alterações no modelo de dados do WMI. Portanto, o WMI permite que um provedor de eventos defina uma classe de evento que descreve o evento. Por exemplo, um evento que descreve uma troca de computador para o modo de espera é um evento extrínsecos. Um provedor deriva um evento extrínsecos da classe de sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) , que é uma subclasse da classe de sistema de [**\_ \_ eventos**](--event.md) . O [registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e os provedores [SNMP](snmp-provider.md) definem classes de evento extrínsecos, como **RegistryKeyChangeEvent**, que notificam um consumidor quando uma chave do registro é alterada. Para obter mais informações, consulte [registrando para eventos de registro do sistema](registering-for-system-registry-events.md) e [gravando um provedor de eventos](writing-an-event-provider.md).

No exemplo a seguir, um provedor de eventos está relatando violações de segurança para um ou mais edifícios. A classe a seguir pode ser definida para o evento extrínsecos que representa uma violação de segurança.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Para receber as notificações de violação de segurança, um consumidor se registra para o tipo de evento SecurityViolationEvent. A menos que especificado de outra forma, um consumidor recebe a notificação de todas as violações de segurança durante todos os períodos de tempo e em todos os prédios. A classe de evento também contém informações que os consumidores podem usar para solicitar eventos mais específicos.

No exemplo a seguir, a consulta registra o consumidor para eventos de violação de segurança no Build 24 somente.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 
