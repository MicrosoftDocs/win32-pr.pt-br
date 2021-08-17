---
description: O \_ loopbackMode put define o modo de loopback multicast.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: Método IMulticastControl::p ut_LoopbackMode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d564fbfd3e5ea0db2c168b6207823945eceb148af17d78bed25cbc59bb4e5ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140409"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>Método LoopbackMode IMulticastControl::p ut \_

\[**put \_ LoopbackMode** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **\_ loopbackMode put** define o modo de loopback multicast.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*modo* \[ Em\]
</dt> <dd>

[**MULTICAST \_ Descritor \_ DE MODO LOOPBACK**](multicast-loopback-mode.md) do novo modo de loopback.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro mode* não é válido.<br/> |



 

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

 

 




