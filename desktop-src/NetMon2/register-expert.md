---
description: O especialista deve implementar a função Registrar especialista. Monitor de Rede chama a função Registrar especialista para obter informações sobre o especialista.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrar função de retorno de chamada especialista (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 1203682e82b01b7665c9661c3f58c14bbf2cd479cac62c72a64505b0e25feaa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889566"
---
# <a name="register-expert-callback-function"></a>Registrar função de retorno de chamada especialista

O especialista deve implementar a **função Registrar** especialista. Monitor de Rede chama a **função Registrar** especialista para obter informações sobre o especialista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pExpertInfo* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura EXPERTENUMINFO**](expertenuminfo.md) que Monitor de Rede aloca. O especialista preenche a estrutura com todas as informações solicitadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno **será TRUE** e a função retornará as informações solicitadas.

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

O **membro** Version da estrutura [**EXPERTENUMINFO**](expertenuminfo.md) deve ser zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




