---
title: Objeto ClosedCaption
description: O objeto ClosedCaption fornece uma maneira de incluir legendas com um clipe de mídia. O texto de legenda está em um arquivo SAMI (Synchronized Accessible Media Interchange).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Objeto ClosedCaption Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10ae51af31e724bd066dbbb9e826569da40159460eb1e7bf570aea331dff86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119588"
---
# <a name="closedcaption-object"></a>Objeto ClosedCaption

O **objeto ClosedCaption** fornece uma maneira de incluir legendas com um clipe de mídia. O texto de legenda está em um arquivo SAMI (Synchronized Accessible Media Interchange).

O **objeto ClosedCaption** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Especifica ou recupera o nome do quadro ou controle que exibe a legenda.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Especifica ou recupera o nome do arquivo que contém as informações necessárias para a legenda fechada. |
| [SAMILang](closedcaption-samilang.md)             | Especifica ou recupera o idioma exibido para legendas fechadas.                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Recupera o número de idiomas com suporte pelo arquivo SAMI atual.                                |
| [SAMIStyle](closedcaption-samistyle.md)           | Especifica ou recupera o estilo de legenda fechada.                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Recupera o número de estilos com suporte pelo arquivo SAMI atual.                                   |



 

O **objeto ClosedCaption** dá suporte aos métodos a seguir.



| Método                                                 | Descrição                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Recupera o LCID (identificador de localidade) de um idioma com suporte no arquivo SAMI atual. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Recupera o nome de um idioma com suporte pelo arquivo SAMI atual.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Recupera o nome de um estilo com suporte pelo arquivo SAMI atual.                        |



 

O **objeto ClosedCaption** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                                  |
|-----------------------------|-------------------------------------------|
| [Jogador](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




