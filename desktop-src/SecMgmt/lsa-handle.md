---
description: Identificador para o objeto de política local.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c674708a1fe29dda1fa01ba56739cfb58f23a037055ae11c5a4e4ab60690de3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894570"
---
# <a name="lsa_handle"></a>identificador de LSA \_

O tipo de dados de **\_ identificador LSA** é um identificador para o objeto de [**política**](policy-object.md) local.


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>Comentários

Antes de poder usar a API de diretiva local, seu aplicativo deve abrir um identificador para um objeto de [**política**](policy-object.md) . Para fazer isso, chame [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy). Essa função retorna um identificador que seu aplicativo pode especificar em chamadas de função de política LSA subsequentes.

Cada identificador tem um conjunto associado de permissões que determinam as operações que seu aplicativo pode executar no objeto de [**política**](policy-object.md) usando o identificador. Seu aplicativo pode abrir mais de um identificador para o objeto de **política** por vez. Quando um identificador não é mais necessário, seu aplicativo deve fechá-lo chamando [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

