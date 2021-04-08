---
description: Usado com o provedor DSS (padrão de assinatura digital) para exportar chaves e importar chaves para o CSP (provedor de serviços de criptografia).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: BLOBs de chave do provedor DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920819"
---
# <a name="dss-provider-key-blobs"></a>BLOBs de chave do provedor DSS

Os [*BLOBs*](../secgloss/b-gly.md) são usados com o provedor DSS ( [*padrão de assinatura digital*](../secgloss/d-gly.md) ) para exportar chaves e importar chaves para o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).

-   [BLOBs de chave pública](#public-key-blobs)
-   [BLOBs de chave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOBs de chave pública

Uma [*chave pública*](../secgloss/p-gly.md) DSS é exportada e importada como um blob, uma sequência de bytes estruturados da seguinte maneira.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

A tabela a seguir descreve esses componentes. Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .



| Campo          | Descrição                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Uma estrutura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . O membro **mágico** deve ter um valor de 0x31535344. Esse número hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DSS1. |
| g              | Uma sequência de **bytes** . O gerador, g. Deve ter o mesmo comprimento que p. Se não tiver o mesmo comprimento que p, ele deverá ser preenchido com 0x00 bytes.                                                                      |
| p              | Uma sequência de **bytes** . O principal módulo, p. O bit mais significativo do byte mais significativo deve ser definido como um.                                                                                                 |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                |
| q              | Uma sequência de **bytes** . A Prime, q, 20 bytes de comprimento. O bit mais significativo do byte mais significativo deve ser definido como um.                                                                                     |
| seedstruct     | Uma estrutura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valores de semente e Counter para verificar as Primes.                                                                                                                                |
| a              | Uma sequência de **bytes** . A chave pública, y. Deve ter o mesmo comprimento que p. Se não tiver o mesmo comprimento que p, ele deverá ser preenchido com 0x00 bytes.                                                                         |



 

> [!Note]  
> Os [*blobs de chave pública*](../secgloss/p-gly.md) não são criptografados. Elas contêm chaves públicas em formato de [*texto sem formatação*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>BLOBs de chave privada

Uma [*chave privada*](../secgloss/p-gly.md) DSS é exportada e importada como uma sequência de bytes estruturados da seguinte maneira.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

A tabela a seguir descreve cada componente. Todos os valores estão no formato [*little-endian*](../secgloss/l-gly.md) .



| Campo          | Descrição                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Uma estrutura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . O membro **mágico** deve ser definido como 0x32535344. Esse número hexadecimal é a codificação [*ASCII*](../secgloss/a-gly.md) de DSS2. |
| g              | Uma sequência de **bytes** . O gerador, g. Deve ter o mesmo comprimento que p. Se não tiver o mesmo comprimento que p, ele deverá ser preenchido com 0x00 bytes.                                                                |
| publickeystruc | Uma estrutura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                          |
| p              | Uma sequência de **bytes** . O principal módulo, p. O bit mais significativo do byte mais significativo deve ser definido como um.                                                                                           |
| q              | Uma sequência de **bytes** . O primo, q. q tem 20 bytes de comprimento. O bit mais significativo do byte mais significativo deve ser definido como um.                                                                          |
| seedstruct     | Uma estrutura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valores de semente e Counter para verificar as Primes.                                                                                                                          |
| x              | Uma sequência de **bytes** . O expoente secreto, x. Deve ter sempre 20 bytes de comprimento. Se x tiver um comprimento menor que 20 bytes, ele deverá ser preenchido com 0x00.                                                     |



 

Ao chamar [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), o desenvolvedor pode escolher se deseja criptografar a chave. O **PRIVATEKEYBLOB** será criptografado se o parâmetro *hExpKey* contiver um identificador válido para uma chave de sessão. Tudo menos a parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) do blob é criptografada.

> [!Note]  
> Os parâmetros de algoritmo de criptografia e chave de criptografia não são armazenados junto com o BLOB de chave privada. O aplicativo deve gerenciar e armazenar essas informações. Se zero for passado para *hExpKey*, a chave privada será exportada sem criptografia.

 

> [!Caution]  
> É perigoso exportar chaves privadas sem criptografia porque elas são então vulneráveis à interceptação e ao uso por entidades não autorizadas.

 

 

 
