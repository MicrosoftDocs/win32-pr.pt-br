---
description: Em uma PKI da Microsoft, as solicitações de certificado são enviadas de computadores cliente para CAs (autoridades de certificação) como uma cadeia de caracteres binária que contém uma sequência de estruturas de dados codificadas.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codificação de solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6bb65b496264fcd1f9667416c78d5d8cf246f1c9aa4cf736990a1f61669f19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904845"
---
# <a name="certificate-request-encoding"></a>Codificação de solicitação de certificado

Em uma PKI da Microsoft, as solicitações de certificado são enviadas de computadores cliente para CAs (autoridades de certificação) como uma cadeia de caracteres binária que contém uma sequência de estruturas de dados codificadas. A API de Registro de Certificado usa ASN.1 (Abstract Syntax Notation One) para descrever e codificar essas estruturas. Para os fins desta documentação, o ASN.1 pode ser dividido conceitualmente nas regras de sintaxe (ISO 8824) que descrevem as estruturas de dados e as regras de codificação (ISO 8825) que especificam como os dados devem ser codificados para transmissão de rede. Para obter mais informações, consulte estes tópicos:

-   [Introdução à sintaxe e à codificação ASN.1](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [Sistema de tipos ASN.1](about-asn-1-type-system.md)
-   [Distinguished Encoding Rules](distinguished-encoding-rules.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API de Registro de Certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



