---
description: O formato de certificado X. 509 versão 3 identifica várias extensões que podem ser adicionadas a um certificado.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensões (API de registro de certificado)
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
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752536"
---
# <a name="extensions-certificate-enrollment-api"></a>Extensões (API de registro de certificado)

O formato de certificado X. 509 versão 3 identifica várias extensões que podem ser adicionadas a um certificado. As extensões fornecem informações aprimoradas sobre o uso da chave, políticas de certificado e restrições, formulários de nome alternativo e muito mais. Você pode usar a interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir um valor de extensão. Muitas das extensões comuns podem ser criadas usando interfaces predefinidas derivadas de **IX509Extension**. Uma coleção de extensões é adicionada a uma solicitação de certificado, incluindo a coleção nos atributos de solicitação. Para mais informações, consulte os seguintes tópicos:

-   [Extensões com suporte](supported-extensions.md)
-   [\#Extensões PKCS 10](pkcs--10-extensions.md)
-   [Extensões CMC](cmc-extensions.md)

 

 



