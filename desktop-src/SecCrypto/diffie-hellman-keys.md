---
description: Explica como gerar, trocar, importar e exportar chaves de Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Chaves de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4082650b030ab1643b83cb154718176d445c98788b15a7bcadd1db97c30bab7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875496"
---
# <a name="diffie-hellman-keys"></a>Chaves de Diffie-Hellman

-   [Gerando chaves de Diffie-Hellman](#generating-diffie-hellman-keys)
-   [Trocando chaves de Diffie-Hellman](#exchanging-diffie-hellman-keys)
-   [Exportando uma chave privada de Diffie-Hellman](#exporting-a-diffie-hellman-private-key)
-   [Código de exemplo](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Gerando chaves de Diffie-Hellman

Para gerar uma chave de Diffie-Hellman, execute as seguintes etapas:

1.  Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.
2.  Gere a nova chave. Há duas maneiras de fazer isso – com o CryptoAPI, gere todos os novos valores para G, P e X ou usando valores existentes para G e P e gerando um novo valor para X.

    **Para gerar a chave gerando todos os novos valores**

    1.  Chame a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , passando **CALG \_ DH \_ it** (Store e Forward) ou **CALG \_ DH \_ EPHEM** (efêmero) no parâmetro *algid* . A chave será gerada usando valores novos e aleatórios para G e P, um valor calculado recentemente para X e seu identificador será retornado no parâmetro *phKey* .
    2.  A nova chave agora está pronta para uso. Os valores de G e P devem ser enviados ao destinatário junto com a chave (ou enviados por algum outro método) ao fazer uma [*troca de chaves*](../secgloss/e-gly.md).

    **Para gerar a chave usando valores predefinidos para G e P**

    1.  Chame [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passando **CALG \_ DH \_ it** (Store e Forward) ou **CALG \_ DH \_ EPHEM** (efêmero) no parâmetro *algid* e **criptografado \_ PREGEN** para o parâmetro *dwFlags* . Um identificador de chave será gerado e retornado no parâmetro *phKey* .
    2.  Inicialize uma estrutura de [**\_ \_ blob de dados criptografados**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) com o membro **PbData** definido como o valor P. O [*blob*](../secgloss/b-gly.md) não contém informações de cabeçalho e o membro **pbData** está no formato [*little-endian*](../secgloss/l-gly.md) .
    3.  O valor de P é definido chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando o identificador de chave recuperado na etapa a no parâmetro *HKEY* , o sinalizador **KP \_ P** no parâmetro *dwParam* e um ponteiro para a estrutura que contém o valor de P no parâmetro *pbData* .
    4.  Inicialize uma estrutura de [**\_ \_ blob de dados criptografados**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) com o membro **PbData** definido como o valor G. O BLOB não contém informações de cabeçalho e o membro **pbData** está no formato little-endian.
    5.  O valor de G é definido chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando o identificador de chave recuperado na etapa a no parâmetro *HKEY* , o sinalizador **KP \_ G** no parâmetro *dwParam* e um ponteiro para a estrutura que contém o valor de G no parâmetro *pbData* .
    6.  O valor de X é gerado chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando o identificador de chave recuperado na etapa a no parâmetro *HKEY* , o sinalizador **KP \_ X** no parâmetro *dwParam* e **nulo** no parâmetro *pbData* .
    7.  Se todas as chamadas de função forem bem-sucedidas, a chave pública Diffie-Hellman estará pronta para uso.

3.  Quando a chave não for mais necessária, destrua-a passando o identificador de chave para a função [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

Se o **CALG \_ DH \_ it** tiver sido especificado nos procedimentos anteriores, os valores de chave serão persistidos no armazenamento com cada chamada para [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). Os valores G e P podem então ser recuperados usando a função [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) . Alguns CSPs podem ter valores G e P embutidos em código. Nesse caso, um erro de **\_ FIXEDPARAMETER de nte** será retornado **se CryptSetKeyParam** for chamado com **KP \_ G** ou **KP \_ P** especificado no parâmetro *dwParam* . Se **CryptDestroyKey** for chamado, o identificador para a chave será destruído, mas os valores de chave serão mantidos no CSP. No entanto, se **CALG \_ DH \_ EPHEM** tiver sido especificado, o identificador para a chave será destruído e todos os valores serão removidos do CSP.

## <a name="exchanging-diffie-hellman-keys"></a>Trocando chaves de Diffie-Hellman

A finalidade do algoritmo de Diffie-Hellman é possibilitar que duas ou mais partes criem e compartilhem uma chave de sessão secreta idêntica compartilhando informações em uma rede que não seja segura. As informações que são compartilhadas pela rede estão na forma de alguns valores constantes e uma Diffie-Hellman chave pública. O processo usado por duas partes de troca de chaves é o seguinte:

-   Ambas as partes concordam com os Diffie-Hellman parâmetros que são um número primo (P) e um número de gerador (G).
-   A parte 1 envia sua Diffie-Hellman chave pública para a parte 2.
-   A parte 2 computa a chave de sessão secreta usando as informações contidas em sua chave privada e a chave pública de 1 parte.
-   A parte 2 envia sua Diffie-Hellman chave pública para a parte 1.
-   A parte 1 computa a chave de sessão secreta usando as informações contidas em sua chave privada e a chave pública de 2 partes.
-   Ambas as partes agora têm a mesma chave de sessão, que pode ser usada para criptografar e descriptografar dados. As etapas necessárias para isso são mostradas no procedimento a seguir.

**Para preparar uma chave pública Diffie-Hellman para transmissão**

1.  Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.
2.  Crie uma chave de Diffie-Hellman chamando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para criar uma nova chave ou chamando a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar uma chave existente.
3.  Obtenha o tamanho necessário para manter o BLOB de chave de Diffie-Hellman chamando o [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passando **NULL** para o parâmetro *pbData* . O tamanho necessário será retornado em *pdwDataLen*.
4.  Aloque memória para o BLOB de chave.
5.  Crie um [*blob de chave pública*](../secgloss/p-gly.md) Diffie-Hellman chamando a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PublicKeyBlob** no parâmetro *dwBlobType* e o identificador para a chave Diffie-Hellman no parâmetro *HKEY* . Essa chamada de função causa o cálculo do valor da chave pública, (G ^ X) mod P.
6.  Se todas as chamadas de função anteriores forem bem-sucedidas, o Diffie-Hellman BLOB de chave pública agora estará pronto para ser codificado e transmitido.

**Para importar uma chave pública Diffie-Hellman e calcular a chave de sessão secreta**

1.  Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.
2.  Crie uma chave de Diffie-Hellman chamando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para criar uma nova chave ou chamando a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar uma chave existente.
3.  Para importar a chave pública Diffie-Hellman para o CSP, chame a função [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , passando um ponteiro para o blob de chave pública no parâmetro *pbData* , o comprimento do blob no parâmetro *dwDataLen* e o identificador para a chave Diffie-Hellman no parâmetro *hPubKey* . Isso faz com que o cálculo, (Y ^ X) mod P, seja executado, criando assim a chave secreta compartilhada e concluindo a [*troca de chaves*](../secgloss/e-gly.md). Essa chamada de função retorna um identificador para a nova chave de sessão secreta, no parâmetro *HKEY* .
4.  Neste ponto, o Diffie-Hellman importado é do tipo **CALG \_ AGREEDKEY \_ any**. Antes que a chave possa ser usada, ela deve ser convertida em um tipo de chave de sessão. Isso é feito chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) com *DwParam* definido como **KP \_ ALGID** e com *pbData* definido como um ponteiro para um valor [**de \_ ID alg**](alg-id.md) que representa uma chave de sessão, como **CALG \_ RC4**. A chave deve ser convertida antes de usar a chave compartilhada na função [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) ou [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) . As chamadas feitas para uma dessas funções antes da conversão do tipo de chave falharão.
5.  A chave de sessão secreta agora está pronta para ser usada para criptografia ou descriptografia.
6.  Quando a chave não for mais necessária, destrua o identificador de chave chamando a função [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

## <a name="exporting-a-diffie-hellman-private-key"></a>Exportando uma chave privada de Diffie-Hellman

Para exportar uma chave privada Diffie-Hellman, execute as seguintes etapas:

1.  Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.
2.  Crie uma chave de Diffie-Hellman chamando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para criar uma nova chave ou chamando a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar uma chave existente.
3.  Crie um Diffie-Hellman [*blob de chave privada*](../secgloss/p-gly.md) chamando a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PRIVATEKEYBLOB** no parâmetro *dwBlobType* e o identificador para a chave Diffie-Hellman no parâmetro *HKEY* .
4.  Quando o identificador de chave não for mais necessário, chame a função [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) para destruir o identificador de chave.

## <a name="example-code"></a>Código de exemplo

O exemplo a seguir mostra como criar, exportar, importar e usar uma chave de Diffie-Hellman para executar uma troca de chaves.


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
