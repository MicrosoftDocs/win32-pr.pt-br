---
description: A função GetProperty retorna um identificador para uma determinada propriedade.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Função GetProperty (Netmon. h)
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
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920692"
---
# <a name="getproperty-function"></a>Função GetProperty

A função **GetProperty** retorna um identificador para uma determinada propriedade.

## <a name="syntax"></a>Sintaxe


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProtocol* \[ no\]
</dt> <dd>

Identificador para o protocolo.

</dd> <dt>

*PropertyName* \[ no\]
</dt> <dd>

Nome da propriedade (por exemplo, **soma de verificação**).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será o identificador para a propriedade.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

A função **GetProperty** pode ser usada para obter o identificador de propriedade necessário para localizar instâncias da propriedade. As funções usadas para localizar as instâncias de propriedade são [FindPropertyInstance](findpropertyinstance.md) (que localiza a primeira instância) e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (que localiza a próxima instância).

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetProperty** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




