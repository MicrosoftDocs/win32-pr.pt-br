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
# <a name="hcryptprov_or_ncrypt_key_handle"></a>\_identificador de chave HCRYPTPROV ou \_ NCRYPT \_ \_

O tipo de dados **HCRYPTPROV \_ ou \_ NCRYPT \_ Key \_ Handle** é usado como um identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) ou CSP CNG. Esse identificador deve ser um identificador [**HCRYPTPROV**](hcryptprov.md) que foi criado usando a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) ou um identificador de **\_ \_ identificador de chave NCRYPT** que foi criado usando a função [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) . Os novos aplicativos sempre devem passar o identificador de **\_ \_ identificador de chave NCRYPT** para um CSP CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
