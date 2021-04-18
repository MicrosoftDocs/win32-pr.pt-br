---
description: 'O \_ tipo de \_ dados identificador de enumeração LSA é usado pela função LSA que enumera objetos TrustedDomain: LsaEnumerateTrustedDomainsEx.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758155"
---
# <a name="lsa_enumeration_handle"></a>\_identificador de enumeração LSA \_

O tipo de dados **\_ \_ identificador de enumeração LSA** é usado pela função LSA que enumera objetos [**TrustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex). Essa função foi projetada para que você possa fazer várias chamadas para enumerar todos os objetos de um determinado tipo no banco de dados.

Na chamada de função de enumeração inicial, você passa um ponteiro para uma variável de **\_ \_ identificador de enumeração LSA** que é inicializada como zero. A função atualiza esse valor. Se a função retornar um valor que indica que há mais objetos a serem enumerados, chame a função novamente e passe o valor de **\_ \_ identificador de enumeração LSA** atualizado para obter uma enumeração continuando do ponto em que a enumeração anterior parou.


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




