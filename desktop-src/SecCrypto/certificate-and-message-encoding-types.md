---
description: Muitas das funções exigem tipos de codificação de certificado ou mensagem.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipos de codificação de certificado e mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461053"
---
# <a name="certificate-and-message-encoding-types"></a>Tipos de codificação de certificado e mensagem

Muitas das funções exigem [*tipos de codificação*](../secgloss/m-gly.md)de certificado ou mensagem. Esse tipo de codificação é um **DWORD**, possivelmente contendo os tipos de codificação de certificado e de mensagem. O tipo de codificação de certificado é armazenado na palavra de ordem inferior. O tipo de codificação de mensagem é armazenado na palavra de ordem superior. Alguns campos de funções ou de estrutura exigem apenas um dos tipos de codificação, mas é sempre aceitável especificar os dois tipos de codificação. Para obter um exemplo que especifica os dois tipos de codificação, consulte [ \# inclusões e \# define](-includes-and--defines.md).

A seguinte convenção de nomenclatura de parâmetro é usada para indicar os tipos de codificação necessários.



| Nome                       | Comentários                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Ambos os tipos de codificação são necessários.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | Somente o tipo de codificação de mensagem é necessário.                                                                                                                                                                                                                                                                             |
| *dwCertEncodingType*       | Somente o tipo de codificação de certificado é necessário.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | Um tipo de codificação de mensagem ou de certificado é necessário. Se a palavra de ordem inferior que contém o tipo de codificação de certificado for diferente de zero, ela será usada. Caso contrário, a palavra de ordem superior que contém o tipo de codificação de mensagem será usada. Se ambos forem especificados, o tipo de codificação de certificado na palavra de ordem inferior será usado. |



 

Os tipos de codificação atualmente definidos são mostrados na tabela a seguir.



| Tipo de codificação          | Valor      |
|------------------------|------------|
| \_codificação ASN \_ cript   | 0x00000001 |
| \_Codificação ASN \_ X509    | 0x00000001 |
| \_ \_ Codificação ASN do PKCS 7 \_ | 0x00010000 |



 

 

 
