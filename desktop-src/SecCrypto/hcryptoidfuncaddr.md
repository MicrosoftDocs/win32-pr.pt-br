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
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

O tipo de dados **HCRYPTOIDFUNCADDR** representa um identificador para uma função instalável do [*identificador de objeto*](../secgloss/o-gly.md) (OID). As funções [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)e [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , e a estrutura [**de \_ \_ \_ informações Prov do repositório de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) usam esse tipo de dados.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
