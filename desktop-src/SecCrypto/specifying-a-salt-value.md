---
description: O provedor de base e o provedor estendido podem especificar o valor e o comprimento do valor de Salt a ser usado. O provedor base define um valor salt usando o valor de parâmetro de Salt de KP \_ . O provedor base sempre define onze bytes de valor Salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Especificando um valor Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756673"
---
# <a name="specifying-a-salt-value"></a>Especificando um valor Salt

O provedor de base e o provedor estendido podem especificar o valor e o comprimento do [*valor de Salt*](../secgloss/s-gly.md) a ser usado. O provedor base define um valor salt usando o valor de parâmetro de Salt de KP \_ . O provedor base sempre define onze bytes de valor Salt.

O provedor avançado define o valor de Salt chamando [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) com o \_ valor do parâmetro KP Salt \_ ex especificado e com o parâmetro *pbData* apontando para uma estrutura de [**\_ \_ blobs de inteiros cript**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) que contém o Salt.

> [!Note]  
> O comprimento total de uma [*chave simétrica*](../secgloss/s-gly.md) do provedor avançado e seu valor de Salt não podem ser maiores que 128 bits.

 

\_O Salt de KP continua a ser fornecido para compatibilidade com versões anteriores com o provedor base. Aplicativos mais recentes devem usar o \_ valor do parâmetro KP Salt \_ ex.

O exemplo a seguir define um valor Salt.


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
