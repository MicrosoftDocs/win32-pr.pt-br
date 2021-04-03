---
title: Objeto ClosedCaption
description: O objeto ClosedCaption fornece uma maneira de incluir legendas com um clipe de mídia. O texto da legenda está em um arquivo de intercâmbio de mídia acessível (SAMI) sincronizado.
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
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104006763"
---
# <a name="closedcaption-object"></a>Objeto ClosedCaption

O objeto **ClosedCaption** fornece uma maneira de incluir legendas com um clipe de mídia. O texto da legenda está em um arquivo de intercâmbio de mídia acessível (SAMI) sincronizado.

O objeto **ClosedCaption** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Especifica ou recupera o nome do quadro ou controle que exibe a legenda.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Especifica ou recupera o nome do arquivo que contém as informações necessárias para Legendagem oculta. |
| [SAMILang](closedcaption-samilang.md)             | Especifica ou recupera o idioma exibido para legendas ocultas.                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Recupera o número de idiomas com suporte pelo arquivo SAMI atual.                                |
| [SAMIstyle](closedcaption-samistyle.md)           | Especifica ou recupera o estilo de legendagem oculta.                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Recupera o número de estilos com suporte pelo arquivo SAMI atual.                                   |



 

O objeto **ClosedCaption** dá suporte aos métodos a seguir.



| Método                                                 | Descrição                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Recupera o identificador de localidade (LCID) de um idioma com suporte do arquivo SAMI atual. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Recupera o nome de um idioma com suporte no arquivo SAMI atual.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Recupera o nome de um estilo suportado pelo arquivo SAMI atual.                        |



 

O objeto **ClosedCaption** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                                  |
|-----------------------------|-------------------------------------------|
| [Jogador](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




