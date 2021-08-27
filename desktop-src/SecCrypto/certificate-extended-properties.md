---
description: Os dados em um certificado, CRL (lista de certificados revogados) ou contexto de lista de certificados confiáveis (CTL), incluindo todas as extensões, são somente leitura e não podem ser alterados.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Propriedades estendidas do certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37eaf192d4c236a4f12898ece2bded86d467404c5eceedd98f1deb976b8857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127086"
---
# <a name="certificate-extended-properties"></a>Propriedades estendidas do certificado

Os dados em um [*certificado*](../secgloss/c-gly.md), CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ) ou [*contexto*](../secgloss/c-gly.md)de [*lista de certificados confiáveis*](../secgloss/c-gly.md) (CTL), incluindo todas as extensões, são somente leitura e não podem ser alterados. No entanto, em plataformas Microsoft, os certificados CryptoAPI também têm propriedades estendidas dinâmicas que podem ser adicionadas e alteradas.

> [!Note]  
> As propriedades estendidas são associadas a um certificado e não fazem parte de um certificado, conforme emitido por uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA). As propriedades estendidas não estão disponíveis em um certificado quando ele é usado em uma plataforma que não seja da Microsoft.

 

Essas propriedades incluem dados que:

-   Pertence à chave privada a ser usada com o certificado.
-   Indica o tipo de hashes a ser executado no certificado.
-   Fornece informações definidas pelo usuário associadas ao certificado.

Em plataformas Microsoft, os valores para essas propriedades são anexados e movidos com o certificado. As propriedades predefinidas atualmente identificadas com as IDs de propriedade incluem as seguintes propriedades:

-   Essas propriedades vinculam um certificado a um CSP específico e, dentro desse CSP, a uma chave privada específica:
    -   \_ID de \_ \_ prop do \_ identificador \_ da chave de certificado Prov
    -   \_ID de \_ \_ prop. \_ informações \_ da chave de certificado Prov
    -   \_ID de \_ prop de contexto de chave de certificado \_ \_
-   Essas propriedades indicam o algoritmo de hash a ser usado quando uma operação de hash é executada:
    -   \_ID de \_ \_ prop hash SHA1 de \_ certificado
    -   \_ID de \_ \_ prop hash MD5 de \_ certificado

Para obter listas completas das propriedades de certificado estendido definidas no momento e descrições do significado e uso de cada propriedade, consulte [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
