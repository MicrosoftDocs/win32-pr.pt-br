---
title: Evento Player. ScriptCommand
description: O evento ScriptCommand ocorre quando um comando ou uma URL sincronizada é recebida. | Evento Player. ScriptCommand
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Windows Media Player de eventos ScriptCommand
- Windows Media Player de eventos ScriptCommand, classe Player
- classe de jogador Windows Media Player, evento ScriptCommand
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f54aac54cf56e65b71dbd604d57d5ae9404a0148db139779ced3aa9e0da0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572424"
---
# <a name="playerscriptcommand-event"></a>Evento Player. ScriptCommand

O evento **ScriptCommand** ocorre quando um comando ou uma URL sincronizada é recebida.

## <a name="syntax"></a>Sintaxe


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*scType* 
</dt> <dd>

Cadeia de caracteres que especifica o tipo de comando de script.

</dd> <dt>

*Param* 
</dt> <dd>

**Cadeia de caracteres** que especifica o comando de script.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

os comandos podem ser inseridos entre os sons e as imagens de um arquivo de mídia Windows ou fluxo. Os comandos são um par de cadeias de caracteres Unicode associadas a um horário designado no fluxo. quando o fluxo atinge o tempo associado ao comando, o controle de Windows Media Player envia um evento **ScriptCommand** com dois parâmetros. Um parâmetro especifica o tipo de comando que está sendo enviado e o outro parâmetro especifica o comando. O tipo de parâmetro é usado para determinar como o parâmetro de comando é processado. Qualquer tipo de comando pode ser inserido em um arquivo ou fluxo para ser manipulado pelo evento **ScriptCommand** .

A tabela a seguir lista os tipos de comando de script que são processados automaticamente pelo Windows Media Player.



| Type                   | Descrição                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | O controle exibe o texto associado na DIV especificada por *ClosedCaption*. **captioningID**.                                                                  |
| CIRCUNSTÂNCIA                  | Informa o controle para executar instruções definidas para o evento especificado.                                                                                          |
| NOME do arquivo               | O controle redefine sua propriedade **URL** , tenta abrir o arquivo especificado e começa a reproduzir o novo fluxo imediatamente.                                        |
| OPENEVENT              | Armazena em buffer o comando de tipo de evento associado para execução oportuna do script de evento.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | O parâmetro *param* contém o texto Lyric sincronizado. Windows Media Player exibe o texto lyric na área de legenda codificada do recurso que agora está em **execução** . |
| TEXT                   | O controle exibe o texto associado na DIV especificada por *ClosedCaption*. **captioningID**.                                                                  |
| URL                    | o controle abrirá automaticamente a URL especificada usando o navegador de Internet padrão se o *Configurações*. a propriedade **invokeURLs** está definida como true.                      |



 

Você pode inserir qualquer outro tipo de comando, desde que forneça o código recíproco para manipular o comando. embora comandos desconhecidos sejam ignorados pelo controle de Windows Media Player, eles ainda são enviados para o evento **ScriptCommand** .

os comandos de URL recebidos pelo controle de Windows Media Player são invocados automaticamente no navegador da Web padrão se o *Configurações*. a propriedade **invokeURLs** está definida como true. você pode usar o *Configurações*. Propriedade **DefaultFrame** para especificar o quadro de destino no qual a página da Web é exibida.

a url enviada para Windows Media Player é processada em relação à URL base especificada pelo *Configurações*. Propriedade **baseURL** . A URL base é concatenada com a URL relativamente especificada, resultando em uma URL totalmente especificada que é passada como o parâmetro de comando pelo evento **ScriptCommand** .

o controle de Windows Media Player sempre processa comandos de tipo de URL de entrada da seguinte maneira:

1.  Um comando de tipo de URL é recebido.
2.  *Configurações*. **baseURL** é usado para criar uma URL completa a partir da URL relativa especificada no comando de script.
3.  *ScriptCommand* é chamado.
4.  depois que *ScriptCommand* retorna, *Configurações*. **invokeURLs** está marcada.
5.  se *Configurações*. **invokeURLs** é true e o comando é um tipo de URL, a URL especificada é invocada. se *Configurações*. **invokeURLs** é false ou, se o comando não for um tipo de URL, o comando será ignorado.

ao criar um arquivo de mídia Windows, você pode especificar em qual quadro a nova URL é exibida, concatenando dois e comercial e o nome do quadro no campo parâmetro. O exemplo a seguir ilustra os parâmetros típicos de *ScriptCommand* . Ele especifica que a URL *mypage* deve ser iniciada no quadro *myframe* .


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



O evento ScriptCommand não será chamado se o arquivo estiver sendo examinado (rápido-encaminhado ou revertido rapidamente).

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Configurações. baseURL**](settings-baseurl.md)
</dt> <dt>

[**Configurações. defaultframe**](settings-defaultframe.md)
</dt> <dt>

[**Configurações. invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





