---
description: O formato de certificado X.509 versão 3 identifica várias extensões que podem ser adicionadas a um certificado.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensões (API de Registro de Certificado)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 534c3cf9268f21c36d982a627de2e1b293ffdca1e1fd4ffc2acd0db9f7d6059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867936"
---
# <a name="extensions-certificate-enrollment-api"></a>Extensões (API de Registro de Certificado)

O formato de certificado X.509 versão 3 identifica várias extensões que podem ser adicionadas a um certificado. As extensões fornecem informações aprimoradas sobre o uso de chaves, políticas e restrições de certificado, formulários de nomes alternativos e muito mais. Você pode usar a interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir um valor de extensão. Muitas das extensões comuns podem ser criadas usando interfaces predefinida derivadas de **IX509Extension**. Uma coleção de extensões é adicionada a uma solicitação de certificado incluindo a coleção nos atributos de solicitação. Para obter mais informações, consulte estes tópicos:

-   [Extensões com suporte](supported-extensions.md)
-   [Extensões PKCS \# 10](pkcs--10-extensions.md)
-   [Extensões do CMC](cmc-extensions.md)

 

 



