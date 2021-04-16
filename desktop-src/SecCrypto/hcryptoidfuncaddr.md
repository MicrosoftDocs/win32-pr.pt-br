---
description: Representa um identificador para uma função instalável do identificador de objeto (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750754"
---
# <a name="hcryptoidfuncaddr"></a><span data-ttu-id="26353-103">HCRYPTOIDFUNCADDR</span><span class="sxs-lookup"><span data-stu-id="26353-103">HCRYPTOIDFUNCADDR</span></span>

<span data-ttu-id="26353-104">O tipo de dados **HCRYPTOIDFUNCADDR** representa um identificador para uma função instalável do [*identificador de objeto*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="26353-104">The **HCRYPTOIDFUNCADDR** data type represents a handle to an [*object identifier*](../secgloss/o-gly.md) (OID) installable function.</span></span> <span data-ttu-id="26353-105">As funções [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)e [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , e a estrutura [**de \_ \_ \_ informações Prov do repositório de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) usam esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="26353-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), and [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) functions, and the [**CERT\_STORE\_PROV\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a><span data-ttu-id="26353-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26353-106">Requirements</span></span>



| <span data-ttu-id="26353-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="26353-107">Requirement</span></span> | <span data-ttu-id="26353-108">Valor</span><span class="sxs-lookup"><span data-stu-id="26353-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26353-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26353-109">Minimum supported client</span></span><br/> | <span data-ttu-id="26353-110">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="26353-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="26353-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26353-111">Minimum supported server</span></span><br/> | <span data-ttu-id="26353-112">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26353-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26353-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26353-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="26353-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="26353-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
