---
description: A função FindPropertyInstance localiza a primeira instância da propriedade especificada pelo parâmetro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Função FindPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770367"
---
# <a name="findpropertyinstance-function"></a>Função FindPropertyInstance

A função **FindPropertyInstance** localiza a primeira instância da propriedade especificada pelo parâmetro *hProperty* .

## <a name="syntax"></a>Sintaxe


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro. O identificador de quadro pode ser recuperado por uma chamada para a função [GetFrame](getframe.md) .

</dd> <dt>

*hProperty* \[ no\]
</dt> <dd>

Identificador para a propriedade que você deseja localizar. O identificador de propriedade pode ser recuperado por uma chamada para a função [GetProperty](getproperty.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (ou seja, se a propriedade for encontrada), o valor de retorno será um ponteiro para a primeira instância da propriedade.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Para recuperar a próxima instância da propriedade, chame [FindPropertyInstanceRestart](findpropertyinstancerestart.md).

Os [*especialistas*](e.md) e os [*analisadores*](p.md)podem chamar a função **FindPropertyInstance** .

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

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




