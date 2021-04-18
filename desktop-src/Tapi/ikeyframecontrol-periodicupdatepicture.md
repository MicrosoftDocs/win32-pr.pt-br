---
description: O método PeriodicUpdatePicture é chamado por um aplicativo para configurar um temporizador no fluxo que solicitará atualizações de imagem periodicamente. As atualizações de imagem causam alto uso de largura de banda, portanto, esse método normalmente será usado em vez de UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: 'IKeyFrameControl: método eriodicUpdatePicture de:P (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800032"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a>IKeyFrameControl: método eriodicUpdatePicture de:P

\[O **PeriodicUpdatePicture** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **PeriodicUpdatePicture** é chamado por um aplicativo para configurar um temporizador no fluxo que solicitará atualizações de imagem periodicamente. As atualizações de imagem causam alto uso de largura de banda, portanto, esse método normalmente será usado em vez de [**UpdatePicture**](ikeyframecontrol-updatepicture.md).

Se o método for chamado quando o fluxo estiver ativo, o temporizador será iniciado imediatamente. Se o fluxo não estiver ativo, o temporizador será iniciado quando o fluxo entrar no estado ativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnable* \[ no\]
</dt> <dd>

**Verdadeiro** habilita o temporizador. **False** desabilita.

</dd> <dt>

*dwInterval* \[ no\]
</dt> <dd>

O intervalo para o temporizador, em segundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | O método foi bem-sucedido.<br/>              |
| <dl> <dt>**E \_ falha**</dt> </dl> | Falha por motivos inesperados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

 




