---
description: Explica como gerar, recuperar, verificar e exportar assinaturas e chaves DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Chaves DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5497a2a02ac5614c056f819a3999ee3cca6c5da78229f92e57002ae6a9e401ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875306"
---
# <a name="dss-keys"></a>Chaves DSS

-   [Gerando e recuperando chaves DSS](#generating-and-retrieving-dss-keys)
-   [Gerando assinaturas DSS](#generating-dss-signatures)
-   [Verificando uma assinatura DSS](#verifying-a-dss-signature)
-   [Exportando chaves DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Gerando e recuperando chaves DSS

As chaves DSS podem ser geradas por uma chamada para a [**função CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) A chamada para **CryptGenKey** requer que AT SIGNATURE ou \_ CALG \_ DSS SIGN sejam \_ passados no *argumento Algid.* Essa chamada gerará os valores P (módulo principal), Q (prime), G (gerador), X (expoente secreto) e Y (chave pública) do zero e os manterá em um [*BLOB*](../secgloss/k-gly.md) de chave para o armazenamento local.

**Para gerar um par de chaves de assinatura DSS**

1.  Chame a [**função CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um handle para o Provedor Criptográfico do Microsoft DSS.
2.  Chame [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para gerar as chaves. AT SIGNATURE ou CALG DSS SIGN devem ser passados para o argumento Algid e os 16 bits superiores do argumento \_ \_ \_ *dwFlags*  devem ser definidos para o tamanho da chave desejado. Se os 16 bits superiores são zero, o tamanho padrão da chave de 1.024 bits será usado. Um [**alça HCRYPTKEY**](hcryptkey.md) é retornado no *argumento hKey.*

**Para recuperar um ponteiro para chaves de assinatura geradas anteriormente**

1.  Chame [**CryptAcquireContext para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) obter um handle para o Provedor criptográfico do Microsoft DSS.
2.  Chame a [**função CryptGetUserKey com**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) o *argumento dwKeySpec* definido como AT \_ SIGNATURE ou CALG \_ DSS \_ SIGN.

**Para recuperar os valores P, Q e G**

1.  Chame [**CryptAcquireContext para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) obter um handle para o Provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptGetUserKey com**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) o *argumento dwKeySpec* definido como AT \_ SIGNATURE ou CALG \_ DSS \_ SIGN.
3.  Chame [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) com o *argumento hKey* definido como o ponteiro recuperado na etapa anterior. O *argumento dwParam* deve ser definido como o sinalizador desejado; KP \_ P, KP \_ Q ou KP \_ G. O valor é retornado no *argumento pbData* e o comprimento dos dados é retornado no *argumento pdwDataLen.* O valor é retornado sem nenhuma informação de header e no [*formato little-endian.*](../secgloss/l-gly.md)

## <a name="generating-dss-signatures"></a>Gerando assinaturas DSS

Os dados a serem assinados devem primeiro [*ser com hashed*](../secgloss/h-gly.md) usando o [*algoritmo SHA.*](../secgloss/s-gly.md) Depois que os dados são com hashed, uma [*assinatura DSS*](../secgloss/d-gly.md) é gerada chamando a [**função CryptSignHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha)

**Para gerar uma assinatura DSS**

1.  Chame [**CryptAcquireContext para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) obter um handle para o Provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptCreateHash com**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) o argumento *Algid* definido como CALG SHA para obter um \_ identificador para um objeto de hash SHA.
3.  Chame [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) com o *argumento hHash* definido como o handle recuperado na etapa anterior. Isso cria um hash dos dados e retorna um handle para o hash no argumento *phHash* da chamada de [**função CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
4.  Chame [**CryptSignHash com**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) o *argumento hHash* definido como o handle recuperado na etapa anterior. AT \_ SIGNATURE ou CALG \_ DSS \_ SIGN podem ser passados no parâmetro *dwKeySpec.* A assinatura é retornada para o endereço fornecido no argumento *pbSignature* e o comprimento da assinatura é retornado para o endereço fornecido no *argumento pdwSigLen.* Um **ponteiro NULL** pode ser passado no argumento *pbSignature* e, nesse caso, a assinatura não é gerada, mas o comprimento da assinatura é retornado para o endereço fornecido no parâmetro *pdwSigLen.*

## <a name="verifying-a-dss-signature"></a>Verificando uma assinatura DSS

Para verificar uma assinatura de DSS, a chave pública do [](../secgloss/s-gly.md) DSS do signante deve ser importada, os dados assinados devem ser com hashed e, em seguida, a assinatura pode ser verificada.

**Para verificar uma assinatura DSS**

1.  Chame [**CryptAcquireContext para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) obter um handle para o Provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) para importar a chave pública DSS do signante.
3.  Chame [**CryptCreateHash com**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) o argumento *Algid* definido como CALG SHA para obter um \_ identificador para um objeto de hash SHA.
4.  Chame [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) com o argumento *hHash* definido como o handle recuperado na etapa anterior e com *pbData* apontando para os dados assinados. Isso cria um hash dos dados e retorna um handle para o hash no argumento *phHash* da chamada de [**função CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
5.  Chame [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) com as seguintes configurações:

    *hHash* é definido como o handle para o hash executado na etapa anterior.

    *pbSignature* aponta para a assinatura a ser verificada.

    *dwSigLen* é definido como o comprimento da assinatura.

    *hPubKey* é definido como o handle da chave pública importada na etapa 2.

    *dwFlags* é definido como zero.

## <a name="exporting-dss-keys"></a>Exportando chaves DSS

Quando você [](../secgloss/s-gly.md) envia dados assinados para alguém em que a assinatura precisará ser verificada pelo destinatário, a chave pública do signante deve ser fornecida ao destinatário e geralmente é enviada junto com os dados assinados. Portanto, é necessário ser capaz de exportar as chaves [*DSS*](../secgloss/d-gly.md) em um formato [*blob de*](../secgloss/k-gly.md) chaves.

**Para exportar a chave pública do DSS**

1.  Chame [**CryptAcquireContext para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) obter um handle para o Provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptGetUserKey com**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) o *argumento dwKeySpec* definido como AT \_ SIGNATURE ou CALG \_ DSS \_ SIGN.
3.  Chame [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) com *hKey* definido como o handle recuperado na etapa anterior, *dwBlobType* definido como PUBLICKEYBLOB e *dwFlags* definido como zero. O [*BLOB*](../secgloss/p-gly.md) de chave pública do DSS é retornado em *pbData* e o comprimento da chave [*BLOB*](../secgloss/k-gly.md) é retornado *em pdwDataLen.* Um **ponteiro NULL** pode ser passado em *pbData* e, nesse caso, apenas o comprimento do BLOB de chave DSS será retornado. O BLOB retornado ao fazer a chamada para **CryptExportKey** está no formato descrito em BLOBs de Chaves do Provedor [de DSS.](dss-provider-key-blobs.md)

**Para exportar a chave privada do DSS**

-   Siga o mesmo procedimento que para exportar uma chave pública DSS, exceto que, ao fazer a chamada para [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), *dwBlobType* está definido como PRIVATEKEYBLOB. O BLOB retornado ao fazer a chamada para **CryptExportKey** está no formato descrito em BLOBs de Chaves do Provedor [de DSS.](dss-provider-key-blobs.md)

 

 
