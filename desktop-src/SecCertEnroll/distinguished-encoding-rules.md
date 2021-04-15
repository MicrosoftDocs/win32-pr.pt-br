---
description: A predefinição de notação de sintaxe abstrata (ASN. 1) define os seguintes conjuntos de regras que regem como as estruturas de dados que estão sendo enviadas entre computadores são codificadas e decodificadas.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501972"
---
# <a name="distinguished-encoding-rules"></a>Distinguished Encoding Rules

A predefinição de notação de sintaxe abstrata (ASN. 1) define os seguintes conjuntos de regras que regem como as estruturas de dados que estão sendo enviadas entre computadores são codificadas e decodificadas.

-   Regras básicas de codificação (BER)
-   CER (regras de codificação canônica)
-   Distinguished Encoding Rules (DER)
-   Regras de codificação empacotadas (por)

O conjunto de regras original foi definido pela especificação BER. CER e DER foram desenvolvidos posteriormente como subconjuntos especializados do BER. POR foi desenvolvido em resposta a críticas sobre a quantidade de largura de banda necessária para transmitir dados usando o BER ou suas variantes. POR fornece uma economia significativa.

O DER foi criado para atender aos requisitos da especificação X. 509 para transferência segura de dados. A API de registro de certificado usa DER exclusivamente. Para obter mais informações, consulte os tópicos a seguir.

-   [Sintaxe de transferência de DER](about-der-transfer-syntax.md)
-   [Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação de solicitação de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Introdução à sintaxe e codificação ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



