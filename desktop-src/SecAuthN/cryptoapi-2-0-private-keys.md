---
description: As credenciais Schannel são representadas internamente como estruturas de contexto de certificado \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 chaves privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ca6356849894ac5d15c07a0116bee7c2a2ba84df8c79de360d96f1e147fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008684"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 chaves privadas

As credenciais Schannel são representadas internamente como estruturas de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . O Schannel localiza a [*chave privada*](/windows/desktop/SecGloss/p-gly) associada a um contexto de certificado específico usando a propriedade de \_ \_ ID de \_ prop info da chave de certificado Prov do certificado \_ \_ . Usando essa propriedade, o Schannel acessa a *chave privada* chamando a função [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) . Para obter detalhes adicionais, consulte [pares de chaves pública/privada](/windows/desktop/SecCrypto/public-private-key-pairs).

Cada credencial Schannel contém uma referência a uma ou mais chaves privadas, cada uma associada a um certificado específico. As [*chaves privadas*](/windows/desktop/SecGloss/p-gly) são tratadas de forma muito diferente, dependendo se a credencial é para um cliente ou um servidor.

## <a name="client-private-keys"></a>Chaves privadas do cliente

[*As chaves privadas*](/windows/desktop/SecGloss/p-gly) do cliente são gerenciadas pelo CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ) em uso. As chaves privadas do cliente normalmente são armazenadas por CSPs do tipo [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) ou Prov \_ RSA \_ Signature.

Se o aplicativo cliente fizer a chamada de [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) manualmente antes de chamar [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), o cliente deverá associar o identificador do CSP ao contexto do certificado usando a \_ propriedade de ID de prop Handle chave de certificado \_ Prov \_ \_ \_ . Se o Schannel encontrar esse conjunto de propriedades, ele não usará \_ a \_ \_ propriedade de \_ ID prop de informações da chave de certificado Prov \_ .

## <a name="server-private-keys"></a>Chaves privadas do servidor

As chaves privadas do servidor são armazenadas por um dos seguintes CSPs:

-   PROV \_ RSA \_ Schannel
-   PROV \_ DH \_ Schannel
-   CSP do PROV \_ Fortezza

A escolha do CSP depende do algoritmo de [*troca de chaves*](/windows/desktop/SecGloss/k-gly)selecionado. As chaves privadas do servidor devem ser do tipo em troca de chave \_ .

 

 
