---
description: Limpa o estado da sessão que está sendo aberta ou a sessão aberta no momento.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Função WFDDisplaySinkCloseSession (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7e8169c541535eb2c5adfd0959da47cee4951750687f7d926798534ddc7cbf88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064896"
---
# <a name="wfddisplaysinkclosesession-function"></a>Função WFDDisplaySinkCloseSession

Limpa o estado da sessão que está sendo aberta ou a sessão aberta no momento.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSessionHandle* \[ no\]
</dt> <dd>

O identificador recebido por meio da invocação de retorno de chamada de notificação do coletor de vídeo do WFD mais recente que incluiu um. [**\_ \_ \_ \_**](wfd-display-sink-notification-callback.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

## <a name="remarks"></a>Comentários

seu aplicativo pode chamar essa função para encerrar a sessão de Miracast por qualquer motivo. Seu aplicativo não precisa chamá-lo quando recebe o tipo **DisconnectedNotification** em seu retorno de chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 10<br/>                                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2016<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_retorno de \_ chamada de notificação do coletor de vídeo WFD \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




