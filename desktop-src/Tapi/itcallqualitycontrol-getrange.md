---
description: O método GetRange obtém o intervalo de valores válidos para uma determinada propriedade de qualidade de chamada.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: Método ITCallQualityControl::GetRange (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8d21c9266e64a9bcb31da0028a0ea28b8de98793d56d5bcf28c791c5497756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762432"
---
# <a name="itcallqualitycontrolgetrange-method"></a>Método ITCallQualityControl::GetRange

\[Esse método não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método GetRange** obtém o intervalo de valores válidos para uma determinada propriedade [de qualidade de chamada](callqualityproperty.md).

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

*Propriedade* \[ Em\]
</dt> <dd>

Membro da [**enum CallQualityProperty.**](callqualityproperty.md)

</dd> <dt>

*plMin* \[ out\]
</dt> <dd>

Valor mínimo válido para a propriedade de entrada.

</dd> <dt>

*plMax* \[ out\]
</dt> <dd>

Valor máximo válido para a propriedade de entrada.

</dd> <dt>

*plSteppingDelta* \[ out\]
</dt> <dd>

Incremente pelo qual o valor da propriedade pode ser aumentado ou reduzido.

</dd> <dt>

*plDefault* \[ out\]
</dt> <dd>

Valor padrão para o *parâmetro* Property.

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Valor da [**enum TAPIControlFlags**](tapicontrolflags.md) que indica como o *valor property* é controlado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




