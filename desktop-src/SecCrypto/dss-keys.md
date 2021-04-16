---
description: Explica como gerar, recuperar, verificar e exportar chaves e assinaturas do DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Chaves DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6ab8adcc4d551c4196e99ce48f5afdd380dc3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747845"
---
# <a name="dss-keys"></a>Chaves DSS

-   [Gerando e recuperando chaves DSS](#generating-and-retrieving-dss-keys)
-   [Gerando assinaturas DSS](#generating-dss-signatures)
-   [Verificando uma assinatura DSS](#verifying-a-dss-signature)
-   [Exportando chaves DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Gerando e recuperando chaves DSS

As chaves DSS podem ser geradas por uma chamada para a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . A chamada para **CryptGenKey** exige que a \_ assinatura ou \_ \_ o sinal CALG DSS seja passado no argumento *algid* . Essa chamada gerará os valores P (primo de módulo), Q (primo), G (gerador), X (expoente secreto) e Y (chave pública) do zero e os manterá em um [*blob de chave*](../secgloss/k-gly.md) para o armazenamento local.

**Para gerar um par de chaves de assinatura DSS**

1.  Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para gerar as chaves. A \_ assinatura ou \_ \_ o sinal DSS CALG deve ser passado para o argumento *algid* e os 16 bits superiores do argumento *dwFlags* devem ser definidos para o tamanho de chave desejado. Se os 16 bits superiores forem zero, o tamanho de chave padrão de 1.024 bits será usado. Um identificador [**HCRYPTKEY**](hcryptkey.md) é retornado no argumento *HKEY* .

**Para recuperar um ponteiro para chaves de assinatura geradas anteriormente**

1.  Chame [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft DSS.
2.  Chame a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) com o argumento *dwKeySpec* definido como a \_ assinatura ou o \_ sinal DSS de CALG \_ .

**Para recuperar os valores de P, Q e G**

1.  Chame [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) com o argumento *dwKeySpec* definido como a \_ assinatura ou o \_ sinal DSS de CALG \_ .
3.  Chame [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) com o argumento *HKEY* definido como o ponteiro recuperado na etapa anterior. O argumento *dwParam* deve ser definido como o sinalizador desejado; KP \_ P, KP \_ Q ou KP \_ G. O valor é retornado no argumento *pbData* e o comprimento dos dados é retornado no argumento *pdwDataLen* . O valor é retornado sem informações de cabeçalho e no formato [*little-endian*](../secgloss/l-gly.md) .

## <a name="generating-dss-signatures"></a>Gerando assinaturas DSS

Os dados a serem assinados devem primeiro ser [*codificados*](../secgloss/h-gly.md) usando o algoritmo [*Sha*](../secgloss/s-gly.md) . Depois que os dados são codificados em hash, uma assinatura [*DSS*](../secgloss/d-gly.md) é gerada chamando a função [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) .

**Para gerar uma assinatura DSS**

1.  Chame [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) com o argumento *ALGID* definido como CALG \_ SHA para obter um identificador para um objeto de hash SHA.
3.  Chame [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) com o argumento *hHash* definido como o identificador recuperado na etapa anterior. Isso cria um hash dos dados e retorna um identificador para o hash no argumento *phHash* da chamada de função [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
4.  Chame [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) com o argumento *hHash* definido como o identificador recuperado na etapa anterior. A \_ assinatura ou \_ \_ o sinal DSS CALG pode ser passado no parâmetro *dwKeySpec* . A assinatura é retornada para o endereço fornecido no argumento *pbSignature* e o comprimento da assinatura é retornado para o endereço fornecido no argumento *pdwSigLen* . Um ponteiro **nulo** pode ser passado no argumento *pbSignature* e, nesse caso, a assinatura não é gerada, mas o comprimento da assinatura é retornado para o endereço fornecido no parâmetro *pdwSigLen* .

## <a name="verifying-a-dss-signature"></a>Verificando uma assinatura DSS

Para verificar uma assinatura DSS, a chave pública DSS do signatário deve ser importada, os [*dados assinados*](../secgloss/s-gly.md) devem ser codificados em hash e a assinatura pode ser verificada.

**Para verificar uma assinatura DSS**

1.  Chame [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) para importar a chave pública DSS do signatário.
3.  Chame [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) com o argumento *ALGID* definido como CALG \_ SHA para obter um identificador para um objeto de hash SHA.
4.  Chame [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) com o argumento *hHash* definido como o identificador recuperado na etapa anterior e com *pbData* apontando para os dados assinados. Isso cria um hash dos dados e retorna um identificador para o hash no argumento *phHash* da chamada de função [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
5.  Chame [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) com as seguintes configurações:

    *hHash* é definido como o identificador para o hash executado na etapa anterior.

    *pbSignature* aponta para a assinatura a ser verificada.

    *dwSigLen* é definido como o comprimento da assinatura.

    *hPubKey* é definido como o identificador da chave pública importada na etapa 2.

    *dwFlags* está definido como zero.

## <a name="exporting-dss-keys"></a>Exportando chaves DSS

Quando você envia [*dados assinados*](../secgloss/s-gly.md) para alguém onde a assinatura precisará ser verificada pelo destinatário, a chave pública do signatário deve ser fornecida ao destinatário e geralmente é enviada junto com os dados assinados. Portanto, é necessário ser capaz de exportar as chaves [*DSS*](../secgloss/d-gly.md) em um formato de [*blob de chave*](../secgloss/k-gly.md) .

**Para exportar a chave pública do DSS**

1.  Chame [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft DSS.
2.  Chame [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) com o argumento *dwKeySpec* definido como a \_ assinatura ou o \_ sinal DSS de CALG \_ .
3.  Chame [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) com *HKEY* definido como o identificador recuperado na etapa anterior, *DwBlobType* definido como PublicKeyBlob e *dwFlags* definido como zero. O [*blob de chave pública*](../secgloss/p-gly.md) DSS é retornado em *pbData* e o comprimento do [*blob de chave*](../secgloss/k-gly.md) é retornado em *pdwDataLen*. Um ponteiro **nulo** pode ser passado em *pbData* e, nesse caso, apenas o comprimento do blob de chave DSS será retornado. O BLOB retornado ao fazer a chamada para **CryptExportKey** está no formato descrito em [blobs de chave do provedor DSS](dss-provider-key-blobs.md).

**Para exportar a chave privada DSS**

-   Siga o mesmo procedimento usado para exportar uma chave pública DSS, exceto que, ao fazer a chamada para [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), *dwBlobType* será definido como PRIVATEKEYBLOB. O BLOB retornado ao fazer a chamada para **CryptExportKey** está no formato descrito em [blobs de chave do provedor DSS](dss-provider-key-blobs.md).

 

 
