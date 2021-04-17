---
description: Representa um identificador para um conjunto de funções instaláveis do identificador de objeto (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770339"
---
# <a name="hcryptoidfuncset"></a><span data-ttu-id="96970-103">HCRYPTOIDFUNCSET</span><span class="sxs-lookup"><span data-stu-id="96970-103">HCRYPTOIDFUNCSET</span></span>

<span data-ttu-id="96970-104">O tipo de dados **HCRYPTOIDFUNCSET** representa um identificador para um conjunto de funções instaláveis do [*identificador de objeto*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="96970-104">The **HCRYPTOIDFUNCSET** data type represents a handle to a set of [*object identifier*](../secgloss/o-gly.md) (OID) installable functions.</span></span> <span data-ttu-id="96970-105">As funções [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)e [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) usam esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="96970-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress), and [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) functions use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a><span data-ttu-id="96970-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96970-106">Requirements</span></span>



| <span data-ttu-id="96970-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="96970-107">Requirement</span></span> | <span data-ttu-id="96970-108">Valor</span><span class="sxs-lookup"><span data-stu-id="96970-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96970-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96970-109">Minimum supported client</span></span><br/> | <span data-ttu-id="96970-110">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96970-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96970-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96970-111">Minimum supported server</span></span><br/> | <span data-ttu-id="96970-112">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96970-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96970-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96970-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="96970-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="96970-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
