---
description: A função GetProperty retorna um handle para uma determinada propriedade.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Função GetProperty (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 07bd5a88017ee16f3bdb1773973283d9ad0f7bc6a942fa4441fb134b5f1930da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365969"
---
# <a name="getproperty-function"></a>Função GetProperty

A **função GetProperty** retorna um handle para uma determinada propriedade.

## <a name="syntax"></a>Sintaxe


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ Em\]
</dt> <dd>

Lidar com o protocolo.

</dd> <dt>

*PropertyName* \[ Em\]
</dt> <dd>

Nome da propriedade (por exemplo, **Checksum**).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será o alça para a propriedade .

Se a função não for bem-sucedida, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

A **função GetProperty** pode ser usada para obter o handle de propriedade necessário para localizar instâncias da propriedade. As funções usadas para localizar instâncias de propriedade [são FindPropertyInstance](findpropertyinstance.md) (que localiza a primeira instância) e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (que localiza a próxima instância).

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função GetProperty.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




