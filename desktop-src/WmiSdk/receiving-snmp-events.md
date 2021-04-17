---
description: Os provedores de eventos SNMP dão suporte a interceptações de SNMPv1 e notificações de SNMPv2.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Recebendo eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f718d2bcea85d0ee942050108f337f8ecb78e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752736"
---
# <a name="receiving-snmp-events"></a>Recebendo eventos SNMP

Os provedores de eventos SNMP dão suporte a interceptações de SNMPv1 e notificações de SNMPv2.

Há suporte para os três tipos de notificações SNMPv1 e de SNMPv2 a seguir:

-   Genérico

    As armadilhas e notificações genéricas correspondem a eventos nomeados, como link para cima e início frio. As armadilhas e as notificações genéricas são representadas por classes, como **SnmpLinkUpNotification** e **SnmpWarmStartExtendedNotification**, que contêm o nome da interceptação no nome da classe. Essas classes são subclasses de [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md).

-   Específico da empresa

    As notificações e armadilhas específicas da empresa correspondem aos eventos representados por uma classe WMI que não é uma subclasse de [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md). Para dar suporte a interceptações e notificações específicas da empresa, um consumidor deve definir classes compilando definições de MIB usando o compilador de MIB SNMP.

-   Corporativo-não específico

    Interceptações e notificações não específicas da empresa não correspondem a nenhum dos tipos de eventos genéricos ou tipos de eventos específicos da empresa. Interceptações e notificações não específicas da empresa não tiveram suas definições de MIB compiladas no SMIR. Elas são representadas pelas classes [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** e **SnmpV2ExtendedNotification** derivadas de SnmpNotification e [SnmpExtendedNotification](snmpextendednotification.md).

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

As seções a seguir são discutidas neste tópico:

-   [Recebendo eventos SNMP genéricos](#receiving-generic-snmp-events)
-   [Recebendo eventos de Enterprise-Specific](#receiving-enterprise-specific-events)
-   [Recebendo eventos de Enterprise-Nonspecific](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Recebendo eventos SNMP genéricos

O SEEP e o SREP dão suporte a todos os tipos de interceptações de SNMPv1 genéricas e notificações de SNMPv2. Os eventos SNMP genéricos são representados por subclasses das classes [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md) .

Cada tipo de evento é representado por uma classe SEEP e uma classe SREP. As classes SEEP derivam de [SnmpNotification](snmpnotification.md); as classes SREP derivam de [SnmpExtendedNotification](snmpextendednotification.md). Os provedores de eventos exigem classes diferentes porque usam mecanismos diferentes na apresentação dos dados de evento SNMP.

O SEEP converte os dados de evento SNMP diretamente nas propriedades da classe WMI, enquanto o SREP não. O SREP adiciona um nível de indireção à interpretação necessária para usar as propriedades do WMI. As propriedades das subclasses SREP [SnmpExtendedNotification](snmpextendednotification.md) são instâncias de classes SNMP; as propriedades das subclasses SEEP [SnmpNotification](snmpnotification.md) são inteiros e cadeias de caracteres.

A tabela a seguir lista os tipos de eventos SNMP genéricos e as classes de evento associadas.



| Evento SNMP                                    | Classe SEEP                                | Classe SREP                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Falha na autenticação                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Perda de vizinho do protocolo de gateway exterior (EGP) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Início frio                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Início quente                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Vincular                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Link para baixo                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Por exemplo, as classes **SnmpLinkUpNotification** e **SnmpLinkUpExtendedNotification** descrevem o evento link-up. Ambas as classes incluem as propriedades **ifIndex**, **ifAdminStatus** e **ifOperStatus** , mas têm tipos muito diferentes. As propriedades na classe **SnmpLinkUpNotification** são do tipo sint32 e String. As propriedades na classe **SnmpLinkUpExtendedNotification** são o tipo de objeto inserido IETF \_ SNMP \_ RFC1213 \_ MIB \_ iftable.

## <a name="receiving-enterprise-specific-events"></a>Recebendo eventos de Enterprise-Specific

O SEEP e o SREP oferecem suporte a interceptações e notificações específicas da empresa que você compilou no SMIR.

O procedimento a seguir descreve como receber eventos específicos da empresa.

**Para receber eventos específicos da empresa**

1.  Compile as definições de MIB do dispositivo responsável para gerar o evento.

    Você pode compilar as definições de MIB usando o compilador de MIB SNMP. Para obter mais informações, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

2.  Determine quais tipos de classes você deseja mapear para os eventos.

    Ao compilar a definição de MIB para um evento específico da empresa, você pode determinar o tipo de classe que o compilador gera. Especificamente, você pode instruir o compilador para criar uma das seguintes opções:

    -   [SnmpNotification](snmpnotification.md) subclasses das definições.
    -   [SnmpExtendedNotification](snmpextendednotification.md) subclasses das definições.
    -   Subclasses [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md) das definições.

    Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

Se os provedores de eventos SNMP receberem uma interceptação ou notificação específica para a qual não há nenhuma classe, os provedores geram um evento não empresarial específico. Para obter mais informações, consulte [recebendo eventos não específicos da empresa](#receiving-enterprise-nonspecific-events).

## <a name="receiving-enterprise-nonspecific-events"></a>Recebendo eventos de Enterprise-Nonspecific

Um evento corporativo não específico é um evento que não é mapeado de uma notificação de SNMPv1 ou de um erro de SNMPv2 para qualquer uma das subclasses de [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification](snmpextendednotification.md) ou qualquer classe que represente um evento corporativo.

SEEP usa as classes **SNMPV1Notification** ou **SNMPV2Notification** para eventos não específicos, enquanto SREP usa as classes **SNMPv1ExtendedNotification** e **SNMPV2ExtendedNotification** .

Todas as quatro classes não específicas da empresa derivam das classes [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification](snmpextendednotification.md) e têm o mesmo formato. Ambas as classes têm a única propriedade **VarBindList**. **VarBindList** é uma matriz de instâncias da classe **SnmpVarBind** . **SnmpVarBind** é uma classe base suportada pelos provedores de eventos SNMP para representar uma instância de uma associação de variável SNMP. A tabela a seguir lista as propriedades de **SnmpVarBind**.



| Propriedade         | Descrição                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Codificação         | Cadeia de caracteres que indica o tipo da variável de notação de sintaxe abstrata (ASN. 1) na propriedade **Value** . |
| ObjectIdentifier | Cadeia de caracteres que identifica a variável na propriedade **Value** .                                                 |
| Valor            | Dados brutos em octetos.                                                                                            |



 

Nas classes **SnmpV1Notification** e **SnmpV2Notification** , a ordem de associação da variável do evento SNMP foi preservada, exceto pelas duas primeiras associações de variáveis, timestamp e SnmpTrapOID. Essas associações foram removidas e armazenadas nas propriedades **timestamp** e **Identification** da classe pai [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification](snmpextendednotification.md) .

 

 



