---
description: Representa um identificador para uma função instalável do identificador de objeto (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb36bdd98332842d89533c9c34a880aecdc8555cd64bb03888c0bd146cea3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006544"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

O tipo de dados **HCRYPTOIDFUNCADDR** representa um identificador para uma função instalável do [*identificador de objeto*](../secgloss/o-gly.md) (OID). As funções [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)e [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , e a estrutura [**de \_ \_ \_ informações Prov do repositório de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) usam esse tipo de dados.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
