---
description: Muitas das funções exigem tipos de codificação de certificado ou mensagem.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipos de codificação de certificado e mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185be8d3cc781786c93ac809c042c86d3601a45d86eaa39452f0bcbf44203a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771972"
---
# <a name="certificate-and-message-encoding-types"></a>Tipos de codificação de certificado e mensagem

Muitas das funções exigem tipos de codificação de certificado [*ou mensagem*](../secgloss/m-gly.md). Esse tipo de codificação é um **DWORD**, possivelmente contendo os tipos de codificação de certificado e mensagem. O tipo de codificação de certificado é armazenado na palavra de ordem baixa. O tipo de codificação de mensagem é armazenado na palavra de ordem alta. Algumas funções ou campos de estrutura exigem apenas um dos tipos de codificação, mas é sempre aceitável especificar ambos os tipos de codificação. Para ver um exemplo que especifica os dois tipos de codificação, consulte [ \# inclui e \# define](-includes-and--defines.md).

A convenção de nomen por parâmetro a seguir é usada para indicar os tipos de codificação necessários.



| Nome                       | Comentários                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Ambos os tipos de codificação são necessários.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | Somente o tipo de codificação de mensagem é necessário.                                                                                                                                                                                                                                                                             |
| *Dwcertencodingtype*       | Somente o tipo de codificação de certificado é necessário.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | Uma mensagem ou um tipo de codificação de certificado é necessário. Se a palavra de ordem baixa que contém o tipo de codificação de certificado for diferente de zero, ela será usada. Caso contrário, a palavra de ordem alta que contém o tipo de codificação de mensagem será usada. Se ambos são especificados, o tipo de codificação de certificado na palavra de ordem baixa é usado. |



 

Os tipos de codificação atualmente definidos são mostrados na tabela a seguir.



| Tipo de codificação          | Valor      |
|------------------------|------------|
| CODIFICAÇÃO \_ CRYPT ASN \_   | 0x00000001 |
| CODIFICAÇÃO ASN X509 \_ \_    | 0x00000001 |
| CODIFICAÇÃO ASN PKCS \_ 7 \_ \_ | 0x00010000 |



 

 

 
