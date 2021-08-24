---
description: O método \_ get LoopbackMode obtém o modo de loopback multicast.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: Método IMulticastControl::get_LoopbackMode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a3f9a600ea64bacf7cafdc5071df264d79079adfefd4a771eea9569fcbb092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013016"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>Método IMulticastControl::get \_ LoopbackMode

\[**get \_ LoopbackMode** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get LoopbackMode** obtém o modo de loopback multicast.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMode* \[ out\]
</dt> <dd>

Ponteiro para o [**descritor \_ MODO LOOPBACK \_ MULTICAST**](multicast-loopback-mode.md) do modo de loopback atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                        | Significado                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro pMode* não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




