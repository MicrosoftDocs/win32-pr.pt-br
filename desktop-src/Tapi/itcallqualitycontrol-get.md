---
description: O método Get Obtém o valor de uma determinada propriedade de controle de qualidade de chamada.
ms.assetid: 0fec408e-2751-4c99-afe1-4337d22eff83
title: 'Método ITCallQualityControl:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea42768c173c0c073abe356e1ae6816a486a03c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779465"
---
# <a name="itcallqualitycontrolget-method"></a>Método ITCallQualityControl:: Get

\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get** Obtém o valor de uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Get(
  [in]  CallQualityProperty Property,
  [out] long                *plValue,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade* \[ no\]
</dt> <dd>

Membro da enumeração [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*plValue* \[ fora\]
</dt> <dd>

Valor da *Propriedade* de entrada.

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

 

 




