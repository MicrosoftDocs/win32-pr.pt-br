---
description: O método set define o valor de uma determinada propriedade de controle de qualidade de chamada.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'Método ITCallQualityControl:: Set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5506e4c318440c2b611a2404590bdf638d34a7da2353a5598d09aecf2990668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003384"
---
# <a name="itcallqualitycontrolset-method"></a>Método ITCallQualityControl:: Set

\[esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **set** define o valor de uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade* \[ no\]
</dt> <dd>

Membro da enumeração [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*lvalue* \[ no\]
</dt> <dd>

Valor desejado para a propriedade.

</dd> <dt>

*lFlags* \[ no\]
</dt> <dd>

Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* deve ser controlado.

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
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
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

 

 




