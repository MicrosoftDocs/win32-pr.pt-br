---
description: A biblioteca de Xenroll.dll foi removida do sistema operacional e substituída por CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Mapeando Xenroll.dll para CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662675"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Mapeando Xenroll.dll para CertEnroll.dll

Antes do Windows Vista, o controle de registro de certificado foi implementado em Xenroll.dll. A biblioteca de Xenroll.dll foi removida do sistema operacional e substituída por CertEnroll.dll.

O XEnroll tentou implementar dois conjuntos paralelos de interfaces. [**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)e [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) estavam em conformidade com a automação e são compatíveis com linguagens de script. As interfaces correspondentes,[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)e [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4), não podiam ser inseridas no script, mas eram mais convenientes para programadores de C++. À medida que evoluíram, os dois conjuntos de interfaces não permaneceram sincronizados. Em particular, o conjunto de interfaces duplas representadas mais recentemente por **ICEnroll4** define apenas um subconjunto da funcionalidade definida por **IEnroll4**.

CertEnroll.dll implementa um conjunto maior e mais estruturado de interfaces COM em conformidade com a automação. Os tópicos a seguir discutem como o Xenroll.dll é mapeado para CertEnroll.dll para diferentes tipos de funcionalidade.

-   [Funções de solicitação de certificado](certificate-request-functions.md)
-   [Funções de resposta de certificado](certificate-response-functions.md)
-   [Funções de atributo](attribute-functions.md)
-   [Funções de extensão](extension-functions.md)
-   [Funções de propriedade externa](external-property-functions.md)
-   [Funções de chave pública e privada](private-and-public-key-functions.md)
-   [Funções do provedor de serviços de criptografia](cryptographic-service-provider-functions.md)
-   [Funções de repositório de certificados](certificate-store-functions.md)
-   [Funções de troca de informações pessoais](personal-information-exchange-functions.md)
-   [Funções auxiliares](helper-functions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a API de registro de certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
