---
description: É usado como um identificador para um CSP (provedor de serviços de criptografia) do CryptoAPI ou CSP CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770338"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a><span data-ttu-id="98400-103">\_identificador de chave HCRYPTPROV ou \_ NCRYPT \_ \_</span><span class="sxs-lookup"><span data-stu-id="98400-103">HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE</span></span>

<span data-ttu-id="98400-104">O tipo de dados **HCRYPTPROV \_ ou \_ NCRYPT \_ Key \_ Handle** é usado como um identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) ou CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="98400-104">The **HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE** data type is used as a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> <span data-ttu-id="98400-105">Esse identificador deve ser um identificador [**HCRYPTPROV**](hcryptprov.md) que foi criado usando a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) ou um identificador de **\_ \_ identificador de chave NCRYPT** que foi criado usando a função [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="98400-105">This handle must be an [**HCRYPTPROV**](hcryptprov.md) handle that has been created by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function or an **NCRYPT\_KEY\_HANDLE** handle that has been created by using the [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) function.</span></span> <span data-ttu-id="98400-106">Os novos aplicativos sempre devem passar o identificador de **\_ \_ identificador de chave NCRYPT** para um CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="98400-106">New applications should always pass in the **NCRYPT\_KEY\_HANDLE** handle to a CNG CSP.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="98400-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98400-107">Requirements</span></span>



| <span data-ttu-id="98400-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="98400-108">Requirement</span></span> | <span data-ttu-id="98400-109">Valor</span><span class="sxs-lookup"><span data-stu-id="98400-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98400-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98400-110">Minimum supported client</span></span><br/> | <span data-ttu-id="98400-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98400-111">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98400-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98400-112">Minimum supported server</span></span><br/> | <span data-ttu-id="98400-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98400-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98400-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98400-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="98400-115"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="98400-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
