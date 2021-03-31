---
description: O especialista deve implementar a função de especialista em registro. Monitor de Rede chama a função de especialista de registro para obter informações sobre o especialista.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrar função de retorno de chamada de especialista (Netmon. h)
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
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827861"
---
# <a name="register-expert-callback-function"></a>Registrar função de retorno de chamada de especialista

O especialista deve implementar a função de especialista em **registro** . Monitor de Rede chama a função de especialista de **registro** para obter informações sobre o especialista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pExpertInfo* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma estrutura [**EXPERTENUMINFO**](expertenuminfo.md) que monitor de rede aloca. O especialista preenche a estrutura com todas as informações solicitadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será **true** e a função retornará as informações solicitadas.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

O membro da **versão** da estrutura [**EXPERTENUMINFO**](expertenuminfo.md) deve ser zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




