---
description: O método GetRange Obtém o intervalo de valores válidos para uma determinada propriedade de qualidade de chamada.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'Método ITCallQualityControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767758"
---
# <a name="itcallqualitycontrolgetrange-method"></a>Método ITCallQualityControl:: GetRange

\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **GetRange** Obtém o intervalo de valores válidos para uma determinada [propriedade de qualidade de chamada](callqualityproperty.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade* \[ no\]
</dt> <dd>

Membro da enumeração [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*plMin* \[ fora\]
</dt> <dd>

Valor mínimo válido para a propriedade de entrada.

</dd> <dt>

*plMax* \[ fora\]
</dt> <dd>

Valor máximo válido para a propriedade de entrada.

</dd> <dt>

*plSteppingDelta* \[ fora\]
</dt> <dd>

Incremento pelo qual o valor da propriedade pode ser aumentado ou diminuído.

</dd> <dt>

*plDefault* \[ fora\]
</dt> <dd>

Valor padrão para o parâmetro *Property* .

</dd> <dt>

*plFlags* \[ fora\]
</dt> <dd>

Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




