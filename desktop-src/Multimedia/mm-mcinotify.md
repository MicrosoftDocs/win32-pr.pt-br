---
title: MM_MCINOTIFY mensagem (Mmsystem.h)
description: A mensagem MM \_ MCINOTIFY notifica um aplicativo de que um dispositivo MCI concluiu uma operação. Os dispositivos MCI enviam essa mensagem somente quando o sinalizador NOTIFY da MCI \_ é usado.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc03ab0406542472871f35ca3ff619d4d9a6f35725b9322a4c11bc73bc29a5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807506"
---
# <a name="mm_mcinotify-message"></a>Mensagem MM \_ MCINOTIFY

A **mensagem MM \_ MCINOTIFY** notifica um aplicativo de que um dispositivo MCI concluiu uma operação. Os dispositivos MCI enviam essa mensagem somente quando o sinalizador NOTIFY da MCI \_ é usado.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*Wflags*
</dt> <dd>

Motivo da notificação. Os seguintes valores são definidos:



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOTIFICAÇÃO DE MCI \_ \_ ANULADA    | O dispositivo recebeu um comando que impedia que as condições atuais para iniciar a função de retorno de chamada fosse atendidas. Se um novo comando interromper o comando atual e também solicitar notificação, o dispositivo enviará essa mensagem somente e não MCI \_ NOTIFY \_ SUPERSEDED |
| FALHA DE \_ NOTIFICAÇÃO DA MCI \_    | Ocorreu um erro de dispositivo enquanto o dispositivo estava executando o comando.                                                                                                                                                                                                            |
| NOTIFICAÇÃO DE MCI \_ \_ BEM-SUCEDIDA | As condições que iniciam a função de retorno de chamada foram atendidas.                                                                                                                                                                                                                 |
| NOTIFICAÇÃO DA MCI \_ \_ SOBRESEDIDA | O dispositivo recebeu outro comando com o sinalizador "notify" definido e as condições atuais para iniciar a função de retorno de chamada foram superadas.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Identificador do dispositivo que inicia a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre o sinalizador NOTIFY da \_ MCI, consulte O sinalizador de [notificação](the-notify-flag.md).

Um dispositivo retorna o sinalizador MCI \_ NOTIFY SUCCESSFUL com MM \_ **\_ MCINOTIFY** quando a ação de um comando é final. Por exemplo, um dispositivo de áudio cd usa esse sinalizador para notificação para o comando [**play**](play.md) ( [**MCI \_ PLAY**](mci-play.md)) quando o dispositivo termina de reproduzir. O **comando play** é bem-sucedido somente quando atinge a posição final especificada ou atinge o final da mídia. Da mesma forma, os comandos [**seek**](seek.md) ( [**MCI \_ SEEK**](mci-seek.md)) e [**record**](record.md) ( [**MCI \_ RECORD**](mci-record.md)) não retornam MCI NOTIFY SUCCESSFUL até que atinjam a posição final especificada ou cheguem ao final da \_ \_ mídia.

Um dispositivo retorna o sinalizador MCI NOTIFY ABORTED com \_ \_ MM **\_ MCINOTIFY** somente quando recebe um comando que o impede de atender às condições de notificação. Por exemplo, o [**comando play**](play.md) não  anularia a notificação para um comando de reprodução anterior, desde que o novo comando não altere a direção da reprodução nem altere a posição final. Os [**comandos seek**](seek.md) e record [**se**](record.md) comportam da mesma forma. A MCI também não envia MCI NOTIFY ABORTED quando a reprodução ou gravação é pausada com o comando \_ \_ [**pause**](pause.md) [**(MCI \_ PAUSE).**](mci-pause.md) Enviar o [**comando resume**](resume.md) ( [**MCI \_ RESUME**](mci-resume.md)) permite que eles continuem a atender às condições de retorno de chamada.

Quando o aplicativo solicitar notificação para um comando, verifique o retorno de erro das funções [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Se essas funções encontrarem um erro e retornarem um valor não zero, a MCI não definirá a notificação para o comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Mensagens MCI](mci-messages.md)
</dt> <dt>

[**Pausa**](pause.md)
</dt> <dt>

[**Jogar**](play.md)
</dt> <dt>

[**Registro**](record.md)
</dt> <dt>

[**Currículo**](resume.md)
</dt> <dt>

[**Procurar**](seek.md)
</dt> </dl>

 

