---
description: A macro do tipo de notificação contém os elementos a seguir.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Macro do tipo de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751763"
---
# <a name="notification-type-macro"></a>Macro do tipo de notificação

A macro do tipo de notificação contém os elementos a seguir.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Componentes

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descritor de objeto
</dt> <dd>

Anexa um nome a um evento SNMP em uma macro do tipo notificação. A lista a seguir lista as regras para mapear o descritor de objeto.



| Tipo                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome da classe CIM encapsulada | "SNMP \_ "<br/> Nome de identidade do módulo MIB<br/> sublinhado ( \_ )<br/> descritor de objeto<br/> " \_ Notificação"<br/> Exemplo: a notificação de **vtpServerDisabled** do **Cisco-VTP-MIB** é mapeada **para \_ \_ notificação de \_ \_ vtpServerDisabled de \_ MIB do Cisco VTP SNMP**.<br/>                 |
| Nome da classe CIM Referent     | "SNMP \_ "<br/> Nome de identidade do módulo MIB<br/> sublinhado ( \_ )<br/> descritor de objeto<br/> " \_ ExtendedNotification"<br/> Exemplo: a notificação de **vtpServerDisabled** do **Cisco-VTP-MIB** é mapeada para **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Cláusula OBJECTs
</dt> <dd>

Enumera o conjunto de objetos associados ao objeto de notificação.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Cláusula de referência
</dt> <dd>

Refere-se a outro documento que contém mais informações sobre o objeto. Ele é mapeado para a **referência** de qualificador de classe CIM, que é do tipo cadeia de caracteres.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Cláusula de descrição
</dt> <dd>

Descreve o objeto em questão. Ele é mapeado para a **Descrição** do qualificador de classe CIM, que é do tipo cadeia de caracteres

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Cláusula de STATUS
</dt> <dd>

Indica se o objeto deve ter suporte. Quando o status é **obsoleto** ou **preterido**, a notificação é descartada do mapeamento. Caso contrário, essa cláusula é mapeada para o **status** do qualificador de classe CIM, que é do tipo **cadeia de caracteres**.

Para SNMPv1, o valor preferencial do **status** é **obrigatório** ou **opcional**, mas o qualificador pode conter algum outro valor. Para o SNMPv2C, o valor preferencial do **status** é **atual** ou **preterido**, mas o qualificador pode conter algum outro valor.

</dd> </dl>

## <a name="remarks"></a>Comentários

O provedor SNMP mapeia a macro do **tipo de notificação** para uma definição de classe encapsulada ou Referent.

Uma definição de classe encapsulada não expõe as informações de instância associadas ao objeto MIB. Em vez disso, a definição de classe codifica a cláusula OBJECTs como uma série de propriedades da classe de evento CIM. Cada propriedade CIM reflete o nome, o tipo e o valor do objeto MIB correspondente na cláusula OBJECTs. Se você precisar de informações de instância, será necessário mapear para uma classe Referent. Uma definição de classe encapsulada é mapeada para a classe [SnmpNotification](snmpnotification.md) .

Uma classe Referent define um objeto MIB e as informações de instância usadas para obter o objeto. A definição de classe codifica a cláusula OBJECTs como uma série de propriedades da classe de evento CIM. Cada propriedade CIM reflete o nome do objeto MIB correspondente na cláusula OBJECTs e o tipo como um objeto incorporado que reflete uma instância da classe associada a esse objeto MIB. Em seguida, o provedor gera uma classe associada ao objeto MIB. Por exemplo, **ifIndex** mapeia para uma classe incorporada chamada **SNMP \_ RFC1213 \_ MIB \_ ifIndex**. Para obter mais informações sobre esse tipo de classe, consulte [macro de tipo de objeto](object-type-macro.md).

 

 




