---
description: Os provedores de eventos SNMP suportam interceptações SNMPv1 e notificações SNMPv2.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Recebendo eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf09e32ec05d42adcc60891cd369cde1f3f078541416ce1a492484de024744bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996015"
---
# <a name="receiving-snmp-events"></a>Recebendo eventos SNMP

Os provedores de eventos SNMP suportam interceptações SNMPv1 e notificações SNMPv2.

Há suporte para os três tipos de interceptações SNMPv1 e notificações SNMPv2:

-   Genérico

    As interceptações genéricas e as notificações correspondem a eventos nomeados, como link para cima e início frio. Interceptações e notificações genéricas são representadas por classes, como **SnmpLinkUpNotification** e **SnmpWarmStartExtendedNotification**, que contêm o nome da interceptação no nome da classe. Essas classes são subclasses [de SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md).

-   Enterprise específico do Enterprise

    Enterprise notificações e interceptações específicas correspondem a eventos representados por uma classe WMI que não é uma subclasse de [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md). Para dar suporte a interceptações e notificações específicas da empresa, um consumidor deve definir classes compilando definições MIB usando o compilador MIB SNMP.

-   Enterprise não específico

    As interceptações e notificações específicas de Nonenterprise não correspondem a nenhum dos tipos de evento genéricos ou tipos de eventos específicos da empresa. As interceptações e notificações específicas de Nonenterprise não tiveram suas definições MIB compiladas no SMIR. Eles são representados pelas classes [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** e **SnmpV2ExtendedNotification** derivadas de SnmpNotification e [SnmpExtendedNotification](snmpextendednotification.md).

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

As seções a seguir são discutidas neste tópico:

-   [Recebendo eventos SNMP genéricos](#receiving-generic-snmp-events)
-   [Recebendo Enterprise-Specific eventos](#receiving-enterprise-specific-events)
-   [Recebendo Enterprise-Nonspecific eventos](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Recebendo eventos SNMP genéricos

O SEEP e o SREP suportam todos os tipos de interceptações SNMPv1 genéricas e notificações SNMPv2. Eventos SNMP genéricos são representados por subclasses das classes [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification.](snmpextendednotification.md)

Cada tipo de evento é representado por uma classe SEEP e uma classe SREP. As classes SEEP derivam [de SnmpNotification](snmpnotification.md); as classes SREP derivam [de SnmpExtendedNotification](snmpextendednotification.md). Os provedores de eventos exigem classes diferentes porque usam mecanismos diferentes na apresentação dos dados de evento SNMP.

O SEEP converte os dados de evento SNMP diretamente em propriedades da classe WMI, enquanto o SREP não. O SREP adiciona um nível de inderção à interpretação necessária para usar as propriedades WMI. As propriedades das subclasses [SREP SnmpExtendedNotification](snmpextendednotification.md) são instâncias de classes SNMP; as propriedades das subclasses [SEEP SnmpNotification](snmpnotification.md) são inteiros e cadeias de caracteres.

A tabela a seguir lista os tipos de eventos SNMP genéricos e as classes de evento associadas.



| Evento SNMP                                    | Classe SEEP                                | Classe SREP                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Falha de autenticação                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Perda de vizinho do EGP (Exterior Gateway Protocol) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Início frio                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Início quente                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Vincular                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Link para baixo                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Por exemplo, as classes **SnmpLinkUpNotification** e **SnmpLinkUpExtendedNotification** descrevem o evento de vinculação. Ambas as classes **incluem as propriedades ifIndex**, **ifAdminStatus** e **ifOperStatus,** mas têm tipos muito diferentes. As propriedades na **classe SnmpLinkUpNotification** são do tipo SINT32 e STRING. As propriedades na **classe SnmpLinkUpExtendedNotification** são o tipo de objeto inserido IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable.

## <a name="receiving-enterprise-specific-events"></a>Recebendo Enterprise-Specific eventos

O SEEP e o SREP são suportados por interceptações e notificações específicas da empresa que você compilou no SMIR.

O procedimento a seguir descreve como receber eventos específicos da empresa.

**Para receber eventos específicos da empresa**

1.  Compile as definições do MIB do dispositivo responsável por gerar o evento.

    Você pode compilar as definições do MIB usando o compilador MIB SNMP. Para obter mais informações, [consulte Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

2.  Determine quais tipos de classes você deseja mapear para os eventos.

    Ao compilar a definição do MIB para um evento específico da empresa, você pode determinar qual tipo de classe o compilador gera. Especificamente, você pode instruir o compilador a criar uma das seguintes opções:

    -   [Subclasses SnmpNotification](snmpnotification.md) das definições.
    -   [Subclasses SnmpExtendedNotification](snmpextendednotification.md) das definições.
    -   [Subclasses SnmpNotification](snmpnotification.md) [e SnmpExtendedNotification](snmpextendednotification.md) das definições.

    Para obter mais informações, consulte [Compilando arquivos MOF](compiling-mof-files.md).

Se os provedores de eventos SNMP receberem uma interceptação ou notificação específica para a qual não há nenhuma classe, os provedores gerarão um evento específico nonenterprise. Para obter mais informações, [consulte Recebendo Enterprise eventos não específicos.](#receiving-enterprise-nonspecific-events)

## <a name="receiving-enterprise-nonspecific-events"></a>Recebendo Enterprise-Nonspecific eventos

Um evento corporativo não específico é um evento que não é mapeado de uma interceptação SNMPv1 ou notificação SNMPv2 para qualquer uma das subclasses [de SnmpNotification,](snmpnotification.md) [SnmpExtendedNotification](snmpextendednotification.md) ou qualquer classe que represente um evento corporativo.

SEEP usa as classes **SNMPV1Notification** ou **SNMPV2Notification** para eventos não específicos, enquanto SREP usa as classes **SNMPv1ExtendedNotification** e **SNMPV2ExtendedNotification.**

Todas as quatro classes empresariais não específicas derivam das classes [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification](snmpextendednotification.md) e têm o mesmo formato. Ambas as classes têm a única **propriedade VarBindList**. **VarBindList** é uma matriz de instâncias da **classe SnmpVarBind.** **SnmpVarBind** é uma classe base com suporte pelos provedores de eventos SNMP para representar uma instância de uma associação de variável SNMP. A tabela a seguir lista as propriedades **de SnmpVarBind**.



| Propriedade         | Descrição                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Codificação         | Cadeia de caracteres que indica o tipo ASN.1 (Abstract Syntax Notation One) da variável na **propriedade** Value. |
| ObjectIdentifier | Cadeia de caracteres que identifica a variável na **propriedade** Value.                                                 |
| Valor            | Dados brutos em octetos.                                                                                            |



 

Nas classes **SnmpV1Notification** e **SnmpV2Notification,** a ordem de associação variável do evento SNMP foi preservada, exceto para as duas primeiras vinculações variáveis, TimeStamp e SnmpTrapOID. Essas vinculações foram removidas e são armazenadas nas propriedades **TimeStamp** e **Identification** da classe pai [SnmpNotification](snmpnotification.md) ou [SnmpExtendedNotification.](snmpextendednotification.md)

 

 



