---
description: A partir do formato de certificado X. 509 versão 3, um certificado pode conter extensões de certificado.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Manipuladores de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfcf1b47fcc97b87f5956f4584aee07acce04222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770453"
---
# <a name="extension-handlers"></a>Manipuladores de extensão

A partir do formato de certificado [*X. 509*](../secgloss/x-gly.md) versão 3, um certificado pode conter extensões de certificado. (Para o conteúdo de um certificado X. 509, consulte [Propriedades do certificado](certificate-properties.md).) Essas extensões indicam informações adicionais. Por exemplo, uma extensão pode indicar informações adicionais de identificação da entidade ou pode indicar informações de uso da chave, que especificam as tarefas (como assinatura ou criptografia) para as quais uma chave pode ser usada. Um conjunto de extensões padrão é definido para uso do aplicativo, e as extensões também podem ser personalizadas.

Cada extensão tem uma cadeia de caracteres de identificador de objeto associada que identifica o tipo de informações adicionais e uma estrutura de dados que contém essas informações. Por exemplo, o identificador de objeto de uso de chave é "2.5.29.15", que indica informações de uso de chave. Sua estrutura de dados associada é um campo de [**\_ \_ blob de bit cript (bits**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) ) que especifica como a chave pode ser usada.

Uma extensão pode ser adicionada a um certificado antes de ser emitida. Quando o certificado é emitido, todas as extensões habilitadas fazem parte do certificado. Se uma extensão estiver marcada como crítica, seu uso deverá ser conhecido pelo aplicativo usando, e o aplicativo deverá aderir à intenção ou ao valor da extensão. Os serviços de certificados permitem que as extensões sejam definidas em um certificado não emitido por meio de métodos fornecidos por [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) e [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy). Para obter detalhes sobre as extensões de certificado, consulte [**\_ extensão CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) na documentação do CryptoAPI. Para obter informações sobre estruturas de dados de extensão de certificado comuns, consulte [estruturas de extensão de certificado X. 509](cryptography-structures.md).

O manipulador de extensão é um objeto COM que fornece rotinas para codificar as extensões mais complexas, mas geralmente usadas e os tipos de dados, como IA5String ou imenablestring.

As extensões que têm os tipos de dados **Date**, **Long** e **BSTR** não exigem um manipulador de extensão. O módulo de política simplesmente chama [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) com o parâmetro de *tipo* definido como um valor que representa o tipo de dados de extensão: PROPtype \_ Date, propproperty \_ Long ou a cadeia de proptype \_ . Em seguida, ele passa a extensão para o mecanismo do servidor. O mecanismo de servidor, por sua vez, executa a codificação de uma (ASN. 1) de [*sintaxe abstrata*](../secgloss/a-gly.md) antes de armazenar a extensão no certificado.

No entanto, as extensões que têm tipos de dados diferentes desses tipos padrão devem ser ASN. 1 codificada por um manipulador de extensão antes que o módulo de política as passe para o mecanismo do servidor. Quando o módulo de política chama [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) para passar uma extensão ASN. 1 codificada para o mecanismo do servidor, ele deve definir o parâmetro de *tipo* como proptype \_ binário. O mecanismo de servidor simplesmente armazena essa extensão codificada no certificado.

O manipulador de extensão padrão, Certenc.dll, exporta várias interfaces **ICertEncodeXXX** e pode ser chamado pelo módulo de política. As informações de tipo necessárias também estão contidas no Certencl.dll que é fornecido no SDK (Software Development Kit) da plataforma. Cada interface fornece um método de **codificação** que retorna uma extensão de certificado com codificação ASN. 1 para o módulo de política em um formato binário. O módulo de política pode então definir a extensão em um certificado chamando o método [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) .

Para obter mais informações, consulte [escrevendo manipuladores de extensão personalizados](writing-custom-extension-handlers.md).

 

 
