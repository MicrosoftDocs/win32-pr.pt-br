---
description: A instalação da nova funcionalidade na memória pode melhorar o desempenho. As funções de CryptoAPI procuram a memória para a funcionalidade antes de Pesquisar o registro para a DLL. A DLL deve ser carregada antes da instalação da funcionalidade.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Instalando a nova funcionalidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7147a1a70ffe57f4948d7db94aab0184d29e5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811056"
---
# <a name="installing-the-new-functionality"></a><span data-ttu-id="a9792-105">Instalando a nova funcionalidade</span><span class="sxs-lookup"><span data-stu-id="a9792-105">Installing the New Functionality</span></span>

<span data-ttu-id="a9792-106">A instalação da nova funcionalidade na memória pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a9792-106">Installing new functionality into memory can improve performance.</span></span> <span data-ttu-id="a9792-107">As funções de [*CryptoAPI*](../secgloss/c-gly.md) procuram a memória para a funcionalidade antes de Pesquisar o registro para a dll.</span><span class="sxs-lookup"><span data-stu-id="a9792-107">[*CryptoAPI*](../secgloss/c-gly.md) functions search memory for the functionality before searching the registry for the DLL.</span></span> <span data-ttu-id="a9792-108">A DLL deve ser carregada antes da instalação da funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="a9792-108">The DLL must be loaded before installing the functionality.</span></span>

<span data-ttu-id="a9792-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) instala o endereço da nova funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="a9792-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installs the address of the new functionality.</span></span> <span data-ttu-id="a9792-110">Ele deve ser colocado na função **DllMain** da dll.</span><span class="sxs-lookup"><span data-stu-id="a9792-110">It should be placed in the **DllMain** function of the DLL.</span></span>

<span data-ttu-id="a9792-111">Se *HMODULE* for passado para [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), uma vez instalado, a dll não será descarregada até que a Crypt32.dll seja descarregada.</span><span class="sxs-lookup"><span data-stu-id="a9792-111">If *hModule* is passed to [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), once installed, the DLL is not unloaded until the Crypt32.dll is unloaded.</span></span>

<span data-ttu-id="a9792-112">O exemplo a seguir chama a função [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) .</span><span class="sxs-lookup"><span data-stu-id="a9792-112">The following example calls the [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define X509_ENCODE_FUNC_COUNT (sizeof(X509EncodeFuncTable) / \
                                sizeof(X509EncodeFuncTable[0]))

static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD dwCertEncodingType,
        IN LPCSTR lpszStructType,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded
);

static const CRYPT_OID_FUNC_ENTRY X509EncodeFuncTable[] = {
    X509_ENHANCED_KEY_USAGE, OssX509CtlUsageEncode,
};

BOOL WINAPI DllMain(
    HMODULE hModule,
    ULONG  ulReason,
    LPVOID lpReserved)
{
    switch (ulReason)
    {
        case DLL_PROCESS_ATTACH:
            if (!CryptInstallOIDFunctionAddress(
                  hModule,
                  X509_ASN_ENCODING,
                  CRYPT_OID_ENCODE_OBJECT_FUNC,
                  X509_ENCODE_FUNC_COUNT,
                  X509EncodeFuncTable,
                  0))
            {
                printf("Install OID function address failed."); 
                return FALSE;
            }
            break;
         default:
            break;
    }
    return TRUE;
}

//-------------------------------------------------------------------
//  CTL Usage (Enhanced Key Usage) Encode (OSS X509)
//-------------------------------------------------------------------
static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD /*dwCertEncodingType*/,
        IN LPCSTR /*lpszStructType*/,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded)
{
    //Encoding logic goes here.
}
```



 

 
