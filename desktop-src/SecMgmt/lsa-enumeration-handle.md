---
description: 'O tipo de dados LSA ENUMERATION HANDLE é usado pela função LSA que enumera objetos \_ \_ TrustedDomain: LsaEnumerateTrustedDomainsEx.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c612edb3fe3dc6faf9028d32c625f13f68899302c6b48b3eba1cf0b3bda701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969195"
---
# <a name="lsa_enumeration_handle"></a>LSA \_ ENUMERATION \_ HANDLE

O **tipo de dados LSA \_ ENUMERATION \_ HANDLE** é usado pela função LSA que enumera objetos [**TrustedDomain:**](trusteddomain-object.md) [**LsaEnumerateTrustedDomainsEx.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex) Essa função foi projetada para que você possa fazer várias chamadas para enumerar todos os objetos de um determinado tipo no banco de dados.

Na chamada de função de enumeração inicial, você passa um ponteiro para uma variável **LSA \_ ENUMERATION \_ HANDLE** que é inicializada como zero. A função atualiza esse valor. Se a função retornar um valor que indica que há mais objetos a enumerar, chame a função novamente e passe o valor atualizado de **\_ LSA ENUMERATION \_ HANDLE** para obter uma enumeração continuando do ponto em que a enumeração anterior foi deixada.


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Ntsecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




