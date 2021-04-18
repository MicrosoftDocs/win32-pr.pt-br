---
title: Evento ScriptCommand do objeto AxWindowsMediaPlayer
description: O evento ScriptCommand ocorre quando um comando ou uma URL sincronizada é recebida. | Evento ScriptCommand do objeto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento ScriptCommand do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760465"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>Evento ScriptCommand do objeto AxWindowsMediaPlayer

O evento ScriptCommand ocorre quando um comando ou uma URL sincronizada é recebida.

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade | Descrição                                                   |
|----------|---------------------------------------------------------------|
| scType   | System. StringSpecifies o tipo de comando de script.<br/> |
| param    | System. StringSpecifies o comando de script.<br/>         |



 

## <a name="remarks"></a>Comentários

Os comandos podem ser inseridos entre os sons e as imagens de um arquivo ou fluxo do Windows Media. Os comandos são um par de cadeias de caracteres Unicode associadas a um horário designado no fluxo. Quando o fluxo atinge o tempo associado ao comando, o controle do Windows Media Player envia um evento **ScriptCommand** com dois parâmetros. Um parâmetro especifica o tipo de comando que está sendo enviado e o outro parâmetro especifica o comando. O tipo de parâmetro é usado para determinar como o parâmetro de comando é processado. Qualquer tipo de comando pode ser inserido em um arquivo ou fluxo para ser manipulado pelo evento **ScriptCommand** .

A tabela a seguir lista os tipos de comando de script que são processados automaticamente pelo Windows Media Player.



| Tipo                   | Descrição                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | O controle exibe o texto associado no elemento HTML especificado por IWMPClosedCaption. **captioningId**.                                                       |
| CIRCUNSTÂNCIA                  | O controle executa instruções definidas para o evento especificado.                                                                                                  |
| NOME do arquivo               | O controle redefine sua propriedade **URL** , tenta abrir o arquivo especificado e começa a reproduzir o novo fluxo imediatamente.                                        |
| OPENEVENT              | Armazena em buffer o comando de tipo de evento associado para execução oportuna do script de evento.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | O parâmetro *param* contém o texto Lyric sincronizado. O Windows Media Player exibe o texto Lyric na área de legenda codificada do recurso que agora está em **execução** . |
| TEXT                   | O controle exibe o texto associado no elemento HTML especificado por IWMPClosedCaption. **captioningId**.                                                       |
| URL                    | O controle abrirá automaticamente a URL especificada usando o navegador de Internet padrão se o IWMPSettings. a propriedade **invokeURLs** está definida como true.                    |



 

Você pode inserir qualquer outro tipo de comando, desde que forneça código para manipular o comando. Embora comandos desconhecidos sejam ignorados pelo controle do Windows Media Player, eles ainda são enviados para o evento **ScriptCommand** .

O evento ScriptCommand não será chamado se o arquivo estiver sendo examinado no modo de avanço rápido ou retrocesso.

Os comandos de URL recebidos pelo controle do Windows Media Player serão invocados automaticamente no navegador da Web padrão se o IWMPSettings. a propriedade **invokeURLs** está definida como true. Você pode usar o IWMPSettings. Propriedade **DefaultFrame** para especificar o quadro de destino no qual a página da Web é exibida.

A URL enviada ao Windows Media Player é processada em relação à URL base especificada pelo IWMPSettings. Propriedade **baseURL** . A URL base é concatenada com a URL relativa, resultando em uma URL totalmente especificada que é passada como o parâmetro de comando pelo evento **ScriptCommand** .

O controle do Windows Media Player sempre processa comandos de URL de entrada da seguinte maneira:

1.  Um comando de tipo de URL é recebido.
2.  IWMPSettings. **baseURL** é usado para criar uma URL completa a partir da URL relativa especificada no comando de script.
3.  **ScriptCommand** é chamado.
4.  Após **ScriptCommand** retornar, IWMPSettings. **invokeURLs** está marcada.
5.  Se IWMPSettings. **invokeURLs** é true e o comando é um comando de URL, a URL especificada é invocada. Se IWMPSettings. **invokeURLs** é false ou, se o comando não for um comando de URL, o comando será ignorado.

Ao criar um arquivo de mídia do Windows, você pode especificar em qual quadro a nova URL será exibida, concatenando dois e comercial e o nome do quadro no campo parâmetro. O exemplo a seguir ilustra os parâmetros típicos de **ScriptCommand** . Ele especifica que a URL *mypage* deve ser iniciada no quadro *myframe* .


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



O evento ScriptCommand não será chamado se o arquivo estiver sendo examinado (encaminhado ou rebobinado rapidamente).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. captioningId (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB e C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. DefaultFrame (VB e C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





