---
title: Evento ScriptCommand do objeto AxWindowsMediaPlayer
description: O evento ScriptCommand ocorre quando um comando ou URL sincronizado é recebido. | Evento ScriptCommand do objeto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento ScriptCommand do objeto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: 26724d8d2d86bd14be9aa5360678dd9caf54620e48d4b361ab120bc2b8927fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509326"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>Evento ScriptCommand do objeto AxWindowsMediaPlayer

O evento ScriptCommand ocorre quando um comando ou URL sincronizado é recebido.

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
| scType   | System.StringSpecifica o tipo de comando de script.<br/> |
| param    | System.StringSpecifica o comando de script.<br/>         |



 

## <a name="remarks"></a>Comentários

Os comandos podem ser inseridos entre os sons e imagens de um Windows mídia ou fluxo. Os comandos são um par de cadeias de caracteres Unicode associadas a uma hora designada no fluxo. Quando o fluxo atinge o tempo associado ao comando, o controle Windows Media Player envia um **evento ScriptCommand** com dois parâmetros. Um parâmetro especifica o tipo de comando que está sendo enviado e o outro parâmetro especifica o comando . O tipo de parâmetro é usado para determinar como o parâmetro de comando é processado. Qualquer tipo de comando pode ser inserido em um arquivo ou fluxo a ser manipulado pelo **evento ScriptCommand.**

A tabela a seguir lista os tipos de comando de script que são processados automaticamente por Windows Media Player.



| Tipo                   | Descrição                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | O controle exibe o texto associado no elemento HTML especificado por IWMPClosedCaption. **captioningId.**                                                       |
| Evento                  | O controle executa instruções definidas para o evento especificado.                                                                                                  |
| Filename               | O controle redefine sua **propriedade de URL,** tenta abrir o arquivo especificado e começa a tocar o novo fluxo imediatamente.                                        |
| Openevent              | Buffers do comando de tipo EVENT associado para execução o tempo há tempo do script EVENT.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | O *parâmetro param* contém o texto de idioma sincronizado. Windows Media Player exibe o texto textão na área de legenda fechada do **recurso Agora Em** Reprodução. |
| TEXT                   | O controle exibe o texto associado no elemento HTML especificado por IWMPClosedCaption. **captioningId.**                                                       |
| URL                    | O controle abre automaticamente a URL especificada usando o navegador da Internet padrão se o IWMPSettings. **A propriedade invokeURLs** é definida como true.                    |



 

Você pode inserir qualquer outro tipo de comando, desde que forneça código para manipular o comando. Embora comandos desconhecidos sejam ignorados pelo controle Windows Media Player, eles ainda são entregues ao **evento ScriptCommand.**

O evento ScriptCommand não será chamado se o arquivo estiver sendo verificado no modo de avanço rápido ou de rebobinamento.

Os comandos de URL recebidos pelo Windows Media Player controle são invocados automaticamente no navegador da Web padrão se o IWMPSettings. **A propriedade invokeURLs** é definida como true. Você pode usar as IWMPSettings. **propriedade defaultFrame** para especificar o quadro de destino no qual a página da Web é exibida.

A URL enviada para Windows Media Player é processada em relação à URL base especificada pelo IWMPSettings. **Propriedade baseURL.** A URL base é concatenada com a URL relativa, resultando em uma URL totalmente especificada que é passada como o parâmetro de comando pelo **evento ScriptCommand.**

O Windows Media Player sempre processa comandos de URL de entrada da seguinte maneira:

1.  Um comando de tipo de URL é recebido.
2.  IWMPSettings. **baseURL** é usada para criar uma URL completa da URL relativa especificada no comando de script.
3.  **ScriptCommand** é chamado.
4.  Depois **que ScriptCommand** retornar, IWMPSettings. **invokeURLs está** marcado.
5.  Se IWMPSettings. **invokeURLs** é true e o comando é um comando de URL, a URL especificada é invocada. Se IWMPSettings. **invokeURLs** é false ou, se o comando não for um comando de URL, o comando será ignorado.

Ao autor de um arquivo Windows Media, você pode especificar em qual quadro a nova URL é exibida concatenando dois entes e o nome do quadro no campo de parâmetro. O exemplo a seguir ilustra parâmetros **ScriptCommand** típicos. Especifica que a URL *mypage* deve ser lançada no *quadro myframe.*


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



O evento ScriptCommand não será chamado se o arquivo estiver sendo verificado (encaminhado ou rewound).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.captioningId (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.baseURL (VB e C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.defaultFrame (VB e C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.invokeURLs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





