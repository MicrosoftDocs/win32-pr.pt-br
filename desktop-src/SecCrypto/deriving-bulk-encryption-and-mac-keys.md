---
description: A criptografia em massa e as chaves MAC são derivadas de uma chave mestra, mas podem incluir outras fontes, dependendo do protocolo e do conjunto de codificação usado.
ms.assetid: f78acb54-c32a-46a8-b465-855251069a57
title: Derivando criptografia em massa e chaves MAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602419be7cdddea27c190806f0d03e087b8aac63eeeee2d80e96e2b3bcfae561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767700"
---
# <a name="deriving-bulk-encryption-and-mac-keys"></a>Derivando criptografia em massa e chaves MAC

A [*criptografia em massa*](../secgloss/b-gly.md) e [*as chaves Mac*](../secgloss/m-gly.md) são derivadas de uma [*chave mestra*](../secgloss/m-gly.md) , mas podem incluir outras fontes, dependendo do protocolo e do conjunto de codificação usado.

O processo de derivar a criptografia em massa e as chaves MAC é o mesmo para o cliente e o servidor:

1.  O mecanismo de protocolo chama [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) na chave mestra uma ou mais vezes para fornecer ao CSP as informações necessárias para criar as chaves.
2.  Como as chaves de [*CryptoAPI*](../secgloss/c-gly.md) não podem ser derivadas diretamente de outras chaves, um objeto de hash é criado a partir da chave mestra usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Esse [*hash*](../secgloss/h-gly.md) é usado para criar as novas chaves.
3.  As duas chaves de criptografia em massa e as duas chaves MAC são criadas a partir do objeto de "hash mestre" usando quatro chamadas para [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).

> [!Note]
> Ao executar reconexões SSL, um mecanismo de protocolo pode executar o procedimento acima várias vezes usando a mesma chave mestra. Isso permite que o cliente e o servidor tenham várias conexões simultâneas, cada uma usando [*criptografia em massa*](../secgloss/b-gly.md) e chaves Mac diferentes sem operações adicionais de RSA ou Diffie-Hellman.
> 
> Todos os CSPs devem usar boas práticas seguras para thread. As contagens de threads de várias dúzias não são incomuns.

 

Este é o código-fonte típico para o mecanismo de protocolo:


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

BOOL fClient = <TRUE if this is code for the client?>;
CRYPT_DATA_BLOB Data;
HCRYPTHASH hMasterHash;

//--------------------------------------------------------------------
// Finish creating the master_secret.

switch(<protocol being used>)
{
    case <PCT 1.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_CLEAR_KEY, 
                   (PBYTE)&Data, 
                   0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CLIENT_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_SERVER_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CERTIFICATE_DATA.
        Data.pbData = pbServerCertificate;
        Data.cbData = cbServerCertificate;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CERTIFICATE, 
                    (PBYTE)&Data, 
                    0);
        break;

    case <SSL 2.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLEAR_KEY, 
                 (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLIENT_RANDOM,
                 (BYTE*)&Data, 
                 0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_SERVER_RANDOM,
                   (BYTE*)&Data, 
                   0);
        break;

case <SSL 3.0>:
case <TLS 1.0>:


//------------------------------------------------------------
// Specify client_random.

        Data.pbData = pClientRandom;
        Data.cbData = cbClientRandom;
        CryptSetKeyParam(
                hMasterKey, 
                KP_CLIENT_RANDOM, 
                (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify server_random.

        Data.pbData = pServerRandom;
        Data.cbData = cbServerRandom;
        CryptSetKeyParam(
                  hMasterKey, 
                  KP_SERVER_RANDOM, 
                  (PBYTE)&Data, 
                  0);
}

//------------------------------------------------------------
// Create the master hash object from the master key.

CryptCreateHash(
            hProv, 
            CALG_SCHANNEL_MASTER_HASH,
            hMasterKey, 
            0, 
            &hMasterHash);

//------------------------------------------------------------
// Derive read key from the master hash object.

CryptDeriveKey(hProv, 
               CALG_SCHANNEL_ENC_KEY, 
               hMasterHash,
               fClient ? CRYPT_SERVER : 0,
               &hReadKey);

//------------------------------------------------------------
// Derive write key from the master hash object.

CryptDeriveKey(
           hProv,
           CALG_SCHANNEL_ENC_KEY,
           hMasterHash,
           fClient ? 0 : CRYPT_SERVER,
           &hWriteKey);

if(<protocol being used> != <SSL 2.0>)   // for SSL 2.0, the master 
                                         // key is also the MAC.
{
//------------------------------------------------------------
// Derive read MAC from the master hash object.

    CryptDeriveKey(
              hProv,
              CALG_SCHANNEL_MAC_KEY,
              hMasterHash,
              fClient ? CRYPT_SERVER : 0,
              &hReadMAC);

//------------------------------------------------------------
// Derive write MAC from the master hash object.

    CryptDeriveKey(
             hProv,
             CALG_SCHANNEL_MAC_KEY,
             hMasterHash,
             fClient ? 0 : CRYPT_SERVER,
             &hWriteMAC);
}

CryptDestroyHash(hMasterHash);
```



 

 
