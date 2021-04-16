---
description: Depois que uma chave mestra é criada ou importada, o RSA/Schannel e o Diffie-Hellman/Schannel informam o CSP do tipo de chaves de criptografia em massa e as chaves MAC que serão derivadas da chave mestra.
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: Especificando os algoritmos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5d329486c655fbc347d35870cfe81335678cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751103"
---
# <a name="specifying-the-algorithms"></a>Especificando os algoritmos

Depois que uma [*chave mestra*](../secgloss/m-gly.md) é criada ou importada, o [*RSA*](../secgloss/r-gly.md)/Schannel e o [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel informam o [*CSP*](../secgloss/c-gly.md) do tipo de [*chaves de criptografia em massa*](../secgloss/b-gly.md) e [*as chaves Mac*](../secgloss/m-gly.md) que serão derivadas da chave mestra. O exemplo a seguir especifica esses algoritmos. O mesmo código é usado tanto para o cliente quanto para o servidor.


```C++
#include <windows.h>
#include <stdio.h>

typedef struct _SCHANNEL_ALG 
{
    DWORD  dwUse;
    ALG_ID Algid;
    DWORD  cBits;
    DWORD  dwFlags;
    DWORD  dwReserved;
} SCHANNEL_ALG, *PSCHANNEL_ALG;

SCHANNEL_ALG Algorithm;

//--------------------------------------------------------------------
// Algorithms for the SCHANNEL_ALG structure

#define SCHANNEL_MAC_KEY   0x00000000
#define SCHANNEL_ENC_KEY   0x00000001

//--------------------------------------------------------------------
// dwFlags for the SCHANNEL_ALG structure
// This flag will be set when the SSL cipher suite is exportable 
// outside the United States and Canada. The use of this flag notifies
// the CSP that it must perform the extra export steps when deriving 
// the key.

#define INTERNATIONAL USAGE   0x00000001

void main()
{
//--------------------------------------------------------------------
// Specify the bulk encryption algorithm.

Algorithm.dwUse = SCHANNEL_ENC_KEY;
Algorithm.Algid = CALG_RC4;    // or CALG_RC2, CALG_DES, and so on
Algorithm.cBits = 40;          // or 64, 128, 192, and so on
if (!CryptSetKeyParam(
         hMasterKey, 
         KP_SCHANNEL_ALG, 
         (PBYTE)&Algorithm, 
         0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};

//--------------------------------------------------------------------
// Specify hash algorithm.
Algorithm.dwUse = SCHANNEL_MAC_KEY;
Algorithm.Algid = CALG_MD5;    // or CALG_SHA, and so on
Algorithm.cBits = 128;         // or 160...
if (!CryptSetKeyParam(
          hMasterKey, 
          KP_SCHANNEL_ALG, 
          (PBYTE)&Algorithm, 
          0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};
```



> [!Note]  
> Um mecanismo de protocolo [*Schannel*](../secgloss/s-gly.md) não deve especificar algoritmos e tamanhos de chave não suportados pelo CSP. Para obter mais informações, consulte [enumerando protocolos com suporte](enumerating-supported-protocols.md). Se forem especificados algoritmos ou tamanhos de chave sem suporte, a função CSP deverá falhar e retornar o \_ código de erro de dados inválidos do nte \_ .

 

 

 
