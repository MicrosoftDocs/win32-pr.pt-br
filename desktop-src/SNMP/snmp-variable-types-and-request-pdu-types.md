---
title: Tipos de variáveis SNMP e tipos de PDU de solicitação
description: As definições para alguns tipos de variáveis SNMP e tipos de PDU de solicitação foram alteradas. O arquivo SNMP. h mapeia os tipos antigos para os novos tipos correspondentes.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641513"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a>Tipos de variáveis SNMP e tipos de PDU de solicitação

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

As definições para alguns tipos de variáveis SNMP e tipos de PDU de solicitação foram alteradas. O arquivo SNMP. h mapeia os tipos antigos para os novos tipos correspondentes.

## <a name="modified-snmp-variable-types"></a>Tipos de variáveis SNMP modificados

Você deve usar os novos tipos de variáveis SNMP listados na tabela a seguir ao desenvolver aplicativos de Gerenciador que usam a API de gerenciamento SNMP da Microsoft. A tabela lista os tipos de variáveis SNMP antigos com os novos tipos de variáveis correspondentes.

| Tipo de variável antiga        | Novo tipo de variável |
|--------------------------|-------------------|
| \_IPAddress de RFC1155 ASN \_  | IPAddress do ASN \_    |
| \_Contador de RFC1155 ASN \_    | \_COUNTER32 ASN    |
| \_Medidor de RFC1155 ASN \_      | \_GAUGE32 ASN      |
| \_TIMEtiques de RFC1155 ASN \_  | \_TIMEtiques ASN    |
| ASN \_ RFC1155 \_ opaco     | ASN \_ opaco       |
| Disp. de \_ RFC1213 ASN \_ | \_octetstring ASN  |



 

## <a name="modified-snmp-pdu-request-types"></a>Tipos de solicitação de PDU do SNMP modificados

Você deve usar os novos tipos de PDU de SNMP listados na tabela a seguir ao desenvolver aplicativos de Gerenciador que usam a API de gerenciamento SNMP da Microsoft. A tabela lista os tipos de PDU do SNMP antigos com os novos tipos de PDU correspondentes.

| Tipo antigo de PDU                 | Novo tipo de PDU        |
|------------------------------|---------------------|
| RFC1157 ASN de \_ \_ solicitação     | \_Get SNMP PDU \_      |
| \_GETNEXTREQUEST RFC1157 \_ ASN | o SNMP \_ PDU \_ GetNext  |
| \_GETRESPONSE RFC1157 \_ ASN    | \_resposta de PDU de SNMP \_ |
| RFC1157 ASN de \_ \_ solicitação     | \_conjunto de PDU SNMP \_      |
| \_ \_ Interceptação ASN RFC1157           | \_V1TRAP de PDU SNMP \_   |



 

 

 