---
description: O método PeriodicUpdatePicture é chamado por um aplicativo para configurar um temporizador no fluxo que solicitará atualizações de imagem periodicamente. As atualizações de imagem causam alto uso de largura de banda, portanto, esse método normalmente será usado em vez de UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: Método IKeyFrameControl::P eriodicUpdatePicture (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87d3412ce32ef599c196a1e8ed4e8afd16da5da52816e293d151d91197eece7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865790"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a>Método IKeyFrameControl::P eriodicUpdatePicture

\[**PeriodicUpdatePicture** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método PeriodicUpdatePicture** é chamado por um aplicativo para configurar um temporizador no fluxo que solicitará atualizações de imagem periodicamente. As atualizações de imagem causam alto uso de largura de banda, portanto, esse método normalmente será usado em vez de [**UpdatePicture.**](ikeyframecontrol-updatepicture.md)

Se o método for chamado quando o fluxo estiver ativo, o temporizador será iniciar imediatamente. Se o fluxo não estiver ativo, o temporizador será iniciado quando o fluxo entrar no estado ativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnable* \[ Em\]
</dt> <dd>

**TRUE** habilita o temporizador. **FALSE** desabilita-o.

</dd> <dt>

*dwInterval* \[ Em\]
</dt> <dd>

O intervalo para o temporizador, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | O método foi bem-sucedido.<br/>              |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Falha por motivos inesperados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

 




