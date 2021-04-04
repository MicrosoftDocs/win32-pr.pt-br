---
title: Mensagem de MM_MCINOTIFY (mmsystem. h)
description: A \_ mensagem mm MCINOTIFY notifica um aplicativo de que um dispositivo MCI concluiu uma operação. Os dispositivos MCI enviam essa mensagem somente quando o \_ sinalizador de notificação MCI é usado.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- Multimídia do Windows de mensagem MM_MCINOTIFY
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
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085899"
---
# <a name="mm_mcinotify-message"></a>\_Mensagem mm MCINOTIFY

A mensagem **mm \_ MCINOTIFY** notifica um aplicativo de que um dispositivo MCI concluiu uma operação. Os dispositivos MCI enviam essa mensagem somente quando o \_ sinalizador de notificação MCI é usado.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Motivo da notificação. Os seguintes valores são definidos:



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_notificação MCI \_ anulada    | O dispositivo recebeu um comando que impediu que as condições atuais para iniciar a função de retorno de chamada fossem atendidas. Se um novo comando interromper o comando atual e ele também solicitar notificação, o dispositivo enviará essa mensagem somente e não a \_ notificação MCI será \_ substituída |
| \_falha na notificação do MCI \_    | Ocorreu um erro de dispositivo enquanto o dispositivo estava executando o comando.                                                                                                                                                                                                            |
| \_notificação MCI \_ bem-sucedida | As condições que iniciam a função de retorno de chamada foram atendidas.                                                                                                                                                                                                                 |
| \_notificação MCI \_ substituída | O dispositivo recebeu outro comando com o sinalizador "notificar" definido e as condições atuais para iniciar a função de retorno de chamada foram substituídas.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Identificador do dispositivo que inicia a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre o \_ sinalizador de notificação MCI, consulte [o sinalizador notificar](the-notify-flag.md).

Um dispositivo retorna o sinalizador de notificação MCI com \_ \_ êxito com **mm \_ MCINOTIFY** quando a ação de um comando é concluída. Por exemplo, um dispositivo de áudio de CD usa esse sinalizador para notificação para o comando [**Play**](play.md) ( [**\_ reprodução MCI**](mci-play.md)) quando o dispositivo termina de ser reproduzido. O comando **Play** é bem-sucedido somente quando atinge a posição final especificada ou atinge o final da mídia. Da mesma forma, os comandos [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) e [**Record**](record.md) ( [**\_ registro MCI**](mci-record.md)) não retornam \_ \_ a notificação de MCI com êxito até atingirem a posição final especificada ou atingirem o final da mídia.

Um dispositivo retorna o \_ sinalizador de notificação MCI \_ abortado com **mm \_ MCINOTIFY** somente quando recebe um comando que impede que ele atenda às condições de notificação. Por exemplo, o comando [**Play**](play.md) não anulará a notificação para um comando de **reprodução** anterior, desde que o novo comando não altere a direção da reprodução nem altere a posição final. Os comandos de [**busca**](seek.md) e [**registro**](record.md) se comportam da mesma forma. O MCI também não envia \_ uma notificação MCI \_ abortada quando a reprodução ou a gravação é pausada com o comando [**Pause**](pause.md) ( [**MCI \_ Pause**](mci-pause.md)). Enviar o comando [**retomar**](resume.md) ( [**MCI \_ resume**](mci-resume.md)) permite que eles continuem a atender às condições de retorno de chamada.

Quando o aplicativo solicitar uma notificação para um comando, verifique o retorno de erro das funções [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Se essas funções encontrarem um erro e retornarem um valor diferente de zero, o MCI não definirá a notificação para o comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Mensagens MCI](mci-messages.md)
</dt> <dt>

[**temporariamente**](pause.md)
</dt> <dt>

[**reproduzir**](play.md)
</dt> <dt>

[**gravável**](record.md)
</dt> <dt>

[**Volte**](resume.md)
</dt> <dt>

[**Procure**](seek.md)
</dt> </dl>

 

