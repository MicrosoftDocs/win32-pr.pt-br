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
# <a name="specifying-a-salt-value"></a><span data-ttu-id="4a6fa-105">Especificando um valor Salt</span><span class="sxs-lookup"><span data-stu-id="4a6fa-105">Specifying a Salt Value</span></span>

<span data-ttu-id="4a6fa-106">O provedor de base e o provedor estendido podem especificar o valor e o comprimento do [*valor de Salt*](../secgloss/s-gly.md) a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-106">Both the Base Provider and the Extended Provider can specify the value and length of the [*salt value*](../secgloss/s-gly.md) to be used.</span></span> <span data-ttu-id="4a6fa-107">O provedor base define um valor salt usando o valor de parâmetro de Salt de KP \_ .</span><span class="sxs-lookup"><span data-stu-id="4a6fa-107">The Base Provider sets a salt value using the KP\_SALT parameter value.</span></span> <span data-ttu-id="4a6fa-108">O provedor base sempre define onze bytes de valor Salt.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-108">The Base Provider always sets eleven bytes of salt value.</span></span>

<span data-ttu-id="4a6fa-109">O provedor avançado define o valor de Salt chamando [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) com o \_ valor do parâmetro KP Salt \_ ex especificado e com o parâmetro *pbData* apontando para uma estrutura de [**\_ \_ blobs de inteiros cript**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) que contém o Salt.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-109">The Enhanced Provider sets the salt value by calling [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) with the KP\_SALT\_EX parameter value specified and with the *pbData* parameter pointing to a [**CRYPT\_INTEGER\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the salt.</span></span>

> [!Note]  
> <span data-ttu-id="4a6fa-110">O comprimento total de uma [*chave simétrica*](../secgloss/s-gly.md) do provedor avançado e seu valor de Salt não podem ser maiores que 128 bits.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-110">The total length of an Enhanced Provider [*symmetric key*](../secgloss/s-gly.md) and its salt value cannot be greater than 128 bits.</span></span>

 

<span data-ttu-id="4a6fa-111">\_O Salt de KP continua a ser fornecido para compatibilidade com versões anteriores com o provedor base.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-111">KP\_SALT continues to be provided for backward compatibility with the Base Provider.</span></span> <span data-ttu-id="4a6fa-112">Aplicativos mais recentes devem usar o \_ valor do parâmetro KP Salt \_ ex.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-112">Newer applications should use the KP\_SALT\_EX parameter value.</span></span>

<span data-ttu-id="4a6fa-113">O exemplo a seguir define um valor Salt.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-113">The following example sets a salt value.</span></span>


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



 

 
