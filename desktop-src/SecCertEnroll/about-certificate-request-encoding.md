---
description: Em uma PKI da Microsoft, as solicitações de certificado são enviadas de computadores cliente para CAs (autoridades de certificação) como uma cadeia de caracteres binária que contém uma sequência de estruturas de dados codificados.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codificação de solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662170"
---
# <a name="certificate-request-encoding"></a>Codificação de solicitação de certificado

Em uma PKI da Microsoft, as solicitações de certificado são enviadas de computadores cliente para CAs (autoridades de certificação) como uma cadeia de caracteres binária que contém uma sequência de estruturas de dados codificados. A API de registro de certificado usa a notação de sintaxe abstrata um (ASN. 1) para descrever e codificar essas estruturas. Para os fins desta documentação, o ASN. 1 pode ser dividido conceitualmente nas regras de sintaxe (ISO 8824) que descrevem as estruturas de dados e as regras de codificação (ISO 8825) que especificam como os dados serão codificados para transmissão de rede. Para mais informações, consulte os seguintes tópicos:

-   [Introdução à sintaxe e codificação ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [Sistema de tipo ASN. 1](about-asn-1-type-system.md)
-   [Distinguished Encoding Rules](distinguished-encoding-rules.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API de registro de certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



