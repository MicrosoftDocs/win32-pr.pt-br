---
description: Cada propriedade de controle de registro de certificado é de leitura/gravação e tem um padrão inicializado, bem como um conjunto de valores aceitáveis.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Usando as propriedades do controle de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647633"
---
# <a name="using-the-certificate-enrollment-control-properties"></a>Usando as propriedades do controle de registro de certificado

Cada propriedade de controle de registro de certificado é de leitura/gravação e tem um padrão inicializado, bem como um conjunto de valores aceitáveis. Você pode definir uma propriedade para qualquer valor nesse conjunto a fim de modificar o comportamento dos métodos que usam a propriedade. Para obter um comportamento desejado, defina a propriedade antes de chamar o método que usa o valor dessa propriedade.

Observe, no entanto, que depois de chamar os métodos a seguir

-   [**acceptPKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [**acceptFilePKCS7**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [**createPKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [**createFilePKCS10**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

as propriedades a seguir estão impedidas de serem redefinidas

-   [**ProviderType**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [**KeySpec**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [**ProviderFlags**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [**ContainerName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [**ProviderName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

a menos que o método [**ICEnroll4:: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) seja chamado.

Para obter informações sobre propriedades e métodos individuais, consulte os tópicos de referência para essas propriedades e métodos na [referência de criptografia](cryptography-reference.md).

As seções a seguir contêm informações específicas do idioma para definir e recuperar as propriedades do controle de registro de certificado:

-   [Propriedades de controle de registro de certificado em C++](certificate-enrollment-control-properties-in-c-.md)

 

 
