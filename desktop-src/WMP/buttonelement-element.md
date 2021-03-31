---
title: Elemento BUTTONelement
description: Elemento BUTTONelement
ms.assetid: 2c1bac51-8aea-4c73-b9b4-4ddbf1e4231b
keywords:
- Aparência do Windows Media Player, elemento BUTTONelement
- elemento skins, BUTTONelement
- Elemento BUTTONelement
- referência de capas, elemento BUTTONelement
- elementos, BUTTONelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4cc69154821981874f0072f6282f708cc4826d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636377"
---
# <a name="buttonelement-element"></a>Elemento BUTTONelement

O elemento **buttonelement** define um único botão dentro de um elemento de **botão** pai. Ele dá suporte aos seguintes atributos. Elementos **buttonelement** predefinidos também são fornecidos para sua conveniência.

O elemento **buttonelement** dá suporte aos seguintes atributos.



| Atributo                                      | Descrição                                                                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](buttonelement-cursor.md)             | Especifica ou recupera o valor do cursor **buttonelement** que aparece quando o mouse está sobre o **botãoelement**.                                                                                      |
| [ligou](buttonelement-down.md)                 | Especifica ou recupera o valor para cima ou para baixo do **botãoelement**.                                                                                                                                            |
| [downToolTip](buttonelement-downtooltip.md)   | Especifica ou recupera o texto de dica de ferramenta que aparece quando o mouse está sobre o **botãoelement** e o **buttonelement** está no estado inoperante.                                                                |
| [index](buttonelement-index.md)               | Recupera o índice do **botãoelement** **dentro do botão**.                                                                                                                                         |
| [mappingColor](buttonelement-mappingcolor.md) | Especifica ou recupera a chave de cor que identifica esse **botão** no grupo **buttonelement** .                                                                                                      |
| [temporárias](buttonelement-sticky.md)             | Especifica ou recupera um valor que indica se o **buttonelement** é adesivo. Quando adesivo, um **buttonelement** alterará os Estados depois de ser clicado e permanecerá no novo estado até ser clicado novamente. |
| [upToolTip](buttonelement-uptooltip.md)       | Especifica ou recupera o texto de dica de ferramenta que aparece quando o mouse está sobre o **botãoelement** e o **buttonelement** está no estado ativo ou activo.                                                        |



 

O elemento **buttonelement** dá suporte ao método a seguir.



| Método                           | Descrição                                                            |
|----------------------------------|------------------------------------------------------------------------|
| [Selecione](buttonelement-click.md) | Chama o manipulador de eventos **onclick** definido para o **buttonelement**. |



 

O elemento **buttonelement** pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [manipuladores de eventos de ambiente](ambient-event-handlers.md).

O elemento **buttonelement** dá suporte aos seguintes atributos de ambiente: [Enabled](ambientattributes-enabled.md) e [tabStop](ambientattributes-tabstop.md).

Efeitos predefinidos são elementos de **efeitos** normais com várias configurações de atributo comuns especificadas por padrão. Os seguintes elementos **buttonelement** predefinidos estão disponíveis.



| BOTÃO predefinidoelement         | Description                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [FFWDELEMENT](ffwdelement.md)   | Um **buttonelement** com um manipulador de eventos interno **onclick** que chama **Player. Controls. Fastforward**. |
| [PRÓXIMOelement](nextelement.md)   | Um **buttonelement** com um manipulador de eventos interno **onclick** que chama **Player. Controls. Next**.        |
| [Pausar](pauseelement.md) | Um **buttonelement** com um manipulador de eventos interno **onclick** que chama **Player. Controls. Pause**.       |
| [PLAYelement](playerelement.md) | Um **buttonelement** com um manipulador de eventos interno **onclick** que chama **Player. Controls. Play**.        |
| [ANTERIORelement](prevelement.md)   | Um **buttonelement** com um manipulador de eventos interno **onclick** que chama **Player. Controls. Previous**.    |
| [REWELEMENT](rewelement.md)     | Um **buttonelement** com um manipulador de eventos interno **onclick** que chama **Player. Controls. retrocesso**.      |
| [STOPelement](stopelement.md)   | Um **buttonelement** com um manipulador de eventos interno **onclick** que chama **Player. Controls. Stop**.        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




