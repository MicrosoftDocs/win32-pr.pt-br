---
description: O \_ método Get loopbackmode Obtém o modo de loopback multicast.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Método IMulticastControl:: get_LoopbackMode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761965"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>Método testloopbackmode de IMulticastControl:: get \_

\[**obter \_ Loopbackmode** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ loopbackmode** Obtém o modo de loopback multicast.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMode* \[ fora\]
</dt> <dd>

Ponteiro para o descritor do [**\_ \_ modo de loopback multicast**](multicast-loopback-mode.md) do modo de loopback atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Significado                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *pMode* não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




