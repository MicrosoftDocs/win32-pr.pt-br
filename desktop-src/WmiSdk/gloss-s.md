---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 223cfe51-8b1d-4965-b7b1-acc3cd5619f0
ms.tgt_platform: multiple
title: S (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7089d3b4e7714b84dc02f6491da1c0a8d21d1b83c1729ac9fe04824c83a6789e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993186"
---
# <a name="s-wmi"></a>S (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) S [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_schema"></span><span id="WMI.GLOSS_SCHEMA"></span>**esquema**
</dt> <dd>

Uma coleção de definições de classe que descrevem [*objetos gerenciados*](gloss-m.md) em um ambiente específico.

</dd> <dt>

<span id="wmi.gloss_security_descriptor"></span><span id="WMI.GLOSS_SECURITY_DESCRIPTOR"></span>**descritor de segurança**
</dt> <dd>

Uma estrutura de dados que contém as informações de segurança para um objeto protegível, como um compartilhamento, arquivo, coletor ou filtro de eventos.

</dd> <dt>

<span id="wmi.gloss_security_identifier"></span><span id="WMI.GLOSS_SECURITY_IDENTIFIER"></span>**identificador de segurança (SID)**
</dt> <dd>

Uma estrutura de dados que identifica contas de usuário, grupo e computador.

</dd> <dt>

<span id="wmi.gloss_semi_synchronous"></span><span id="WMI.GLOSS_SEMI_SYNCHRONOUS"></span>**semi-síncrono**
</dt> <dd>

Consulte o *método semisynchronous*.

</dd> <dt>

<span id="wmi.gloss_semi__synchronous"></span><span id="WMI.GLOSS_SEMI__SYNCHRONOUS"></span>**semi-síncrono**
</dt> <dd>

Consulte o *método semisynchronous*.

</dd> <dt>

<span id="wmi.gloss_semisynchronous"></span><span id="WMI.GLOSS_SEMISYNCHRONOUS"></span>**método semisynchronous**
</dt> <dd>

Uma chamada de método que retorna imediatamente e permite que o aplicativo ou script enumere os objetos retornados como uma coleção.

</dd> <dt>

<span id="gloss_servicesid"></span><span id="GLOSS_SERVICESID"></span>**SID de serviço**
</dt> <dd>

Um *Sid* exclusivo que é criado para cada contexto de segurança; ou seja, um para "LocalService" e outro para "NetworkService". Somente o *SID do serviço* tem permissões para recursos, como threads e eventos, que são criados pelo processo de host do provedor WMI (wmiprvse.exe).

</dd> <dt>

<span id="wmi.gloss_sid"></span><span id="WMI.GLOSS_SID"></span>**SIDs**
</dt> <dd>

Consulte *identificador de segurança*.

</dd> <dt>

<span id="wmi.gloss_singleton_class"></span><span id="WMI.GLOSS_SINGLETON_CLASS"></span>**classe singleton**
</dt> <dd>

Uma classe WMI que dá suporte a uma única instância.

</dd> <dt>

<span id="wmi.gloss_sink"></span><span id="WMI.GLOSS_SINK"></span>**coletar**
</dt> <dd>

Um objeto COM que atua como o destino de entrega física para os resultados de uma operação assíncrona ou de uma notificação de evento. Um coletor implementado por um [*consumidor permanente*](gloss-p.md) dá suporte à interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Um coletor implementado por um [*consumidor temporário*](gloss-t.md) ou aplicativos que fazem chamadas assíncronas dá suporte à interface [**IWbemObjectSink**](iwbemobjectsink.md) .

Os clientes de script podem usar o objeto [**SWbemSink**](swbemsink.md) e os eventos, como [**OnObjectReady**](swbemsink-onobjectready.md), para receber retornos de chamada resultantes de chamadas assíncronas.

</dd> <dt>

<span id="wmi.gloss_standard_consumer"></span><span id="WMI.GLOSS_STANDARD_CONSUMER"></span>**consumidor padrão**
</dt> <dd>

Um [*consumidor permanente*](gloss-p.md) pré-instalado que executa uma ação, como enviar uma mensagem de email ou gravar em um log quando configurado por um arquivo [*formato MOF (MOF)*](gloss-m.md) ou um script.

</dd> <dt>

<span id="wmi.gloss_standard_provider"></span><span id="WMI.GLOSS_STANDARD_PROVIDER"></span>**provedor padrão**
</dt> <dd>

Um [*provedor*](gloss-p.md) interno do WMI, que é diferente de um provedor personalizado ou de terceiros.

</dd> <dt>

<span id="wmi.gloss_standard_qualifier"></span><span id="WMI.GLOSS_STANDARD_QUALIFIER"></span>**qualificador padrão**
</dt> <dd>

Um [*qualificador*](gloss-q.md) que o [*Gerenciador de objetos CIM*](gloss-c.md) anexa automaticamente a uma classe, instância, propriedade, método ou parâmetro de um método.

</dd> <dt>

<span id="wmi.gloss_standard_schema"></span><span id="WMI.GLOSS_STANDARD_SCHEMA"></span>**esquema padrão**
</dt> <dd>

Uma estrutura conceitual comum que organiza e relaciona as classes que representam o estado operacional atual de um sistema, rede ou aplicativo. A [*DMTF (Distributed Management Task Force)*](gloss-d.md) define o esquema padrão no [*modelo CIM (CIM)*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_static_class"></span><span id="WMI.GLOSS_STATIC_CLASS"></span>**classe estática**
</dt> <dd>

Uma definição de classe CIM que raramente muda e é armazenada no [*repositório CIM*](gloss-c.md) até que seja explicitamente excluída. O [*Gerenciador de objetos CIM*](gloss-c.md) pode fornecer uma definição de uma classe estática sem um [*provedor*](gloss-p.md). Uma classe estática pode dar suporte a instâncias *estáticas* ou [*dinâmicas*](gloss-d.md).

</dd> <dt>

<span id="wmi.gloss_static_instance"></span><span id="WMI.GLOSS_STATIC_INSTANCE"></span>**instância estática**
</dt> <dd>

Uma instância de uma classe CIM que é armazenada de forma persistente no [*repositório CIM*](gloss-c.md) e permanece válida até que seja explicitamente excluída, mesmo entre as reinicializações do sistema.

</dd> <dt>

<span id="wmi.gloss_static_method"></span><span id="WMI.GLOSS_STATIC_METHOD"></span>**método estático**
</dt> <dd>

Um método definido em uma classe CIM que é executado pela recuperação da definição de classe em vez de recuperar uma instância da classe.

</dd> <dt>

<span id="wmi.gloss_subschema"></span><span id="WMI.GLOSS_SUBSCHEMA"></span>**subesquema**
</dt> <dd>

Uma parte de um *esquema* que pertence a uma organização específica. O [*Win32schema*](gloss-w.md) é um exemplo de um subesquema.

</dd> <dt>

<span id="wmi.gloss_system_class"></span><span id="WMI.GLOSS_SYSTEM_CLASS"></span>**classe do sistema**
</dt> <dd>

Uma classe que o [*Gerenciador de objetos CIM*](gloss-c.md) define para oferecer suporte a recursos principais, como notificação de eventos, segurança e localização. Uma classe de sistema é definida automaticamente em cada [*namespace*](gloss-n.md). Uma classe de sistema deriva da classe base abstrata [**\_ \_ SystemClass**](--systemclass.md).

</dd> <dt>

<span id="wmi.gloss_system_monitor"></span><span id="WMI.GLOSS_SYSTEM_MONITOR"></span>**Monitor do sistema**
</dt> <dd>

Um utilitário (CIM) que é a GUI para monitoramento de desempenho.

</dd> <dt>

<span id="wmi.gloss_system_property"></span><span id="WMI.GLOSS_SYSTEM_PROPERTY"></span>**Propriedade do sistema**
</dt> <dd>

Uma propriedade que o [*Gerenciador de objetos CIM*](gloss-c.md) define para fornecer informações que se aplicam a cada classe, por exemplo, nome, derivação e [*namespace*](gloss-n.md).

</dd> </dl>

 

 



