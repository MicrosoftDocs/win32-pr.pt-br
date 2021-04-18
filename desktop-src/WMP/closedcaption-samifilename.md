---
title: ClosedCaption.SAMIFileName
description: A propriedade SAMIFileName especifica ou recupera o nome do arquivo que contém as informações necessárias para Legendagem oculta.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption. SAMIFileName Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810574"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

A propriedade **SAMIFileName** especifica ou recupera o nome do arquivo que contém as informações necessárias para Legendagem oculta.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

O arquivo de intercâmbio de mídia acessível (SAMI) sincronizado deve usar uma extensão de nome de arquivo. SMI ou. Sami.

Se você não especificar um valor para **SAMIFileName**, essa propriedade recuperará uma cadeia de caracteres que contém o nome do arquivo ou a URL associada ao item de mídia atual. Essa associação pode ocorrer quando um arquivo SAMI é especificado usando o parâmetro de URL *Sami* , ou automaticamente quando o arquivo Sami tem o mesmo nome que o nome do arquivo de mídia digital (exceto para a extensão de nome de arquivo). Se não houver nenhum arquivo SAMI associado à mídia atual, essa propriedade recuperará uma cadeia de caracteres vazia ("").

Depois de especificar um valor para **SAMIFileName**, esse valor persiste até que você especifique um novo valor (ou até que um novo item de mídia seja aberto usando o parâmetro de URL *Sami* ). Portanto, você deve especificar um novo valor para essa propriedade antes de reproduzir cada novo item de mídia. Dessa forma, o novo valor de **SAMIFileName** entrará em vigor quando o próximo item de mídia for aberto (ou quando o *Player*.**fechar** é chamado). A especificação de um novo valor para **SAMIFileName** não tem nenhum efeito para a mídia atual.

Para fazer com que o Windows Media Player volte a usar o arquivo SAMI associado a um item de mídia específico, especifique um valor para **SAMIFileName** igual a uma cadeia de caracteres vazia ("") antes de reproduzir o próximo item de mídia.

**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

Os três exemplos de JScript a seguir usam *ClosedCaption*. **SAMIFileName** para especificar o nome de um arquivo de texto de legenda oculta. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Player. fechar**](player-close.md)
</dt> </dl>

 

 





