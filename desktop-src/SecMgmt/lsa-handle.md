---
description: Identificador para o objeto de política local.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011075"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

