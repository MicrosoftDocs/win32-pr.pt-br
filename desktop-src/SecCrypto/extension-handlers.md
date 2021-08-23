---
description: A partir do formato de certificado X.509 Versão 3, um certificado pode conter extensões de certificado.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Manipuladores de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba61c5896887471038325eba0dbed75f43061cff81452727933a3013c37f8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006924"
---
# <a name="extension-handlers"></a>Manipuladores de extensão

A partir do [*formato de certificado X.509*](../secgloss/x-gly.md) Versão 3, um certificado pode conter extensões de certificado. (Para ver o conteúdo de um Certificado X.509, consulte [Propriedades do Certificado](certificate-properties.md).) Essas extensões indicam informações adicionais. Por exemplo, uma extensão pode indicar informações adicionais de identificação de assunto ou pode indicar informações de uso de chave, que especifica as tarefas (como assinatura ou criptografia) para as quais uma chave pode ser usada. Um conjunto de extensões padrão é definido para uso do aplicativo e as extensões também podem ser personalizadas.

Cada extensão tem uma cadeia de caracteres de identificador de objeto associada que identifica o tipo de informações adicionais e uma estrutura de dados que contém essas informações. Por exemplo, o identificador de objeto de uso de chave é "2.5.29.15", que indica informações de uso de chave. Sua estrutura de dados associada é um [**\_ \_ BLOB DE BITS CRYPT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) (bitfield) que especifica como a chave pode ser usada.

Uma extensão pode ser adicionada a um certificado antes de ser emitida. Quando o certificado é emitido, todas as extensões habilitadas fazem parte do certificado. Se uma extensão for marcada como crítica, seu uso deverá ser conhecido pelo aplicativo usando e o aplicativo deverá aderir à intenção ou ao valor da extensão. Os Serviços de Certificados permitem que as extensões sejam definidas em um certificado não emitido por meio de métodos fornecidos por [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) e [**ICertServerPolicy.**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Para obter detalhes sobre extensões de certificado, consulte [**EXTENSÃO \_ DE CERTIFICADO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) na documentação do CryptoAPI. Para obter informações sobre estruturas de dados de extensão de certificado comuns, consulte Estruturas de extensão de certificado [X.509](cryptography-structures.md).

O manipulador de extensão é um objeto COM que fornece rotinas para codificar os tipos de dados e extensões mais complexos, mas comumente usados, como IA5String ou PrintableString.

Extensões que têm os tipos de **dados DATE,** **LONG** e **BSTR** não exigem um manipulador de extensão. O módulo de política simplesmente chama [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) com o parâmetro *Type* definido como um valor que representa o tipo de dados de extensão: PROPTYPE \_ DATE, PROPTYPE \_ LONG ou PROPTYPE \_ STRING. Em seguida, ele passa a extensão para o mecanismo de servidor. O mecanismo de servidor, por sua vez, executa a codificação ASN.1 (Abstract [*Syntax Notation One)*](../secgloss/a-gly.md) antes de armazenar a extensão no certificado.

No entanto, as extensões que têm tipos de dados diferentes desses tipos padrão devem ser codificadas como ASN.1 por um manipulador de extensões antes que o módulo de política os passe para o mecanismo de servidor. Quando o módulo de política chama [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) para passar uma extensão codificada em ASN.1 para o mecanismo de servidor, ele deve definir o parâmetro *Type* como PROPTYPE \_ BINARY. Em seguida, o mecanismo de servidor simplesmente armazena essa extensão codificada no certificado.

O manipulador de extensão padrão, Certenc.dll, exporta várias interfaces **ICertEncodeXXX** e pode ser chamado pelo módulo de política. As informações de tipo necessárias também estão contidas Certencl.dll que são fornecidas no SDK (Kit de Desenvolvimento de Software de Plataforma). Cada interface fornece um **método Encode** que retorna uma extensão de certificado codificado em ASN.1 para o módulo de política em um formato binário. O módulo de política pode definir a extensão em um certificado chamando o método [**ICertServerPolicy::SetCertificateExtension.**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension)

Para obter mais informações, consulte [Escrevendo manipuladores de extensão personalizados.](writing-custom-extension-handlers.md)

 

 
