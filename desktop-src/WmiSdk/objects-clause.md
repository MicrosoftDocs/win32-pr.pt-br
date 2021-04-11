---
description: A cláusula OBJECTs da macro do tipo notificação enumera o conjunto de objetos associados ao objeto de notificação.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: Cláusula OBJECTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e25848e0fc98ca79ef96e25423ba7872296e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164242"
---
# <a name="objects-clause"></a>Cláusula OBJECTs

A cláusula OBJECTs da macro do [tipo notificação](notification-type-macro.md) enumera o conjunto de objetos associados ao objeto de notificação.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

As regras a seguir se aplicam ao mapear para classes CIM:

-   Cada membro da cláusula OBJECTs é mapeado para uma propriedade da definição da classe CIM. O descritor de objeto do membro mapeia literalmente para o nome da propriedade CIM. Por exemplo, **ifIndex** é convertido em **ifIndex**.
-   Cada propriedade CIM gerada pelo processo de mapeamento contém o qualificador **VarBindIndex** .

    **VarBindIndex** é um qualificador obrigatório **UInt32** que descreve a posição do objeto como ele aparece na cláusula objetos do tipo de [interceptação](trap-type-macro.md) ou na macro do [tipo de notificação](notification-type-macro.md) . O inteiro também especifica a posição da propriedade como ela aparece na lista de associações de variáveis da PDU de INTERCEPTAção SNMPv1 ou SNMPv2C (unidade de dados de protocolo), respectivamente. (Como as duas primeiras associações de variáveis sempre são carimbo de data/hora e identificação, todas as variáveis adicionais são numeradas após o valor 2.)

    Quando a classe de evento CIM é gerada a partir de uma macro do [tipo de interceptação](trap-type-macro.md) SNMPv1, o qualificador **VarBindIndex** tem um valor inicial de 1 para a primeira variável na lista de associações de variáveis.

    Quando a classe de evento CIM é gerada a partir de uma macro do [tipo de notificação](notification-type-macro.md) do SNMPv2c, o qualificador **VarBindIndex** tem um valor inicial de 3 para a primeira variável na lista de associações de variáveis.

Ao mapear uma classe CIM encapsulada, cada membro da cláusula OBJECTs é mapeado para uma propriedade CIM que reflete o nome, o tipo e o valor do objeto MIB correspondente. Os procedimentos de mapeamento usados são especificados nos seguintes tópicos:

-   [Cláusula de sintaxe](syntax-clause.md)
-   [Macro de Convenção TEXTUAL](textual-convention-macro.md)
-   [Cláusulas ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)

Ao usar uma classe CIM Referent, cada membro da cláusula OBJECTs é mapeado da seguinte maneira:

-   Cada membro da cláusula OBJECTs é mapeado para uma única propriedade da classe CIM. A propriedade é fortemente tipada como um objeto inserido.
-   A classe do objeto inserido é gerada por meio do procedimento de mapeamento de objeto padrão. Para obter mais informações, consulte [macro de tipo de objeto](object-type-macro.md). Por exemplo, **iftable** é mapeado para uma classe inserida denominada **SNMP \_ RFC1213 \_ MIB \_ iftable**.
-   Os valores associados às associações de variável de uma PDU de INTERCEPTAção são instanciados como objetos incorporados de um objeto da classe Referent. Cada objeto inserido contém valores para cada uma das propriedades com chave do objeto e o valor da propriedade na associação de variável que está sendo mapeada.

 

 



