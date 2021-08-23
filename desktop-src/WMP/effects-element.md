---
title: Elemento EFFECTS
description: Elemento EFFECTS
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Windows Media Player capas, elemento EFFECTS
- skins, elemento EFFECTS
- Elemento EFFECTS
- referência para capas, elemento EFFECTS
- elementos, EFFECTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a859414ffae934cafaa0c35b6b364eb42a5795bbeeef637857a0d81f47623379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651136"
---
# <a name="effects-element"></a>Elemento EFFECTS

O **elemento EFFECTS** fornece uma maneira de organizar e manipular visualizações usando os seguintes atributos e métodos. Um elemento **EFFECTS** predefinido também é fornecido para conveniência.

O **elemento EFFECTS** dá suporte aos atributos a seguir.



| Atributo                                                        | Descrição                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | Especifica ou recupera um valor que indica se todas as visualizações no Registro de deve ser incluído.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Especifica ou recupera a visualização atual.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Recupera o número de predefinições disponíveis para a visualização atual.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Recupera o título de exibição da visualização atual.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Recupera o nome do Registro da visualização atual.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Especifica ou recupera a predefinição atual da visualização atual.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Recupera o título da predefinição atual da visualização atual.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Recupera um valor que indica se a visualização atual pode ser exibida em tela inteira.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Recupera o número de visualizações disponíveis.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Recupera um valor que indica se a visualização atual tem uma página de propriedades.                                                                                                                                                                  |
| [Fullscreen](effects-fullscreen.md)                             | Especifica ou recupera um valor que indica se a visualização atual é exibida em tela inteira. Só pode ser definido em tempo de executar.                                                                                                                   |
| [Janela](effects-windowed.md)                                 | Especifica ou recupera um valor que indica se a visualização será janelada ou sem janela, ou seja, se todo o retângulo do controle ficará visível em todos os momentos ou se ela poderá ser recortada. Só pode ser definido em tempo de design. |



 

O **elemento EFFECTS** dá suporte aos métodos a seguir.



| Método                                       | Descrição                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Recupera o nome amigável da visualização com o índice do Registro especificado.                               |
| [effectType](effects-effecttype.md)         | Recupera o nome do Registro da visualização com o índice do Registro especificado.                               |
| [avançar](effects-next.md)                     | Exibe a próxima predefinição de visualização, movendo para a próxima visualização, se necessário.                            |
| [nextEffect](effects-nexteffect.md)         | Exibe a primeira predefinição da próxima visualização, ignorando predefinições intermediárias.                                |
| [nextPreset](effects-nextpreset.md)         | Exibe a próxima predefinição da visualização atual.                                                            |
| [Anterior](effects-previous.md)             | Exibe a predefinição de visualização anterior, passando para a última predefinição da visualização anterior, se necessário. |
| [previousEffect](effects-previouseffect.md) | Exibe a visualização anterior, ignorando predefinições.                                                            |
| [previousPreset](effects-previouspreset.md) | Exibe a predefinição anterior da visualização atual.                                                        |
| [configurações](effects-settings.md)             | Exibe a página de atributo para a visualização atual, se presente.                                            |



 

O **elemento EFFECTS** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [Atributos de ambiente e](ambient-attributes.md) [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Efeitos predefinidos são elementos **EFFECTS** normais com várias configurações de atributo comuns especificadas por padrão. Os seguintes efeitos predefinidos estão disponíveis.



| EFEITOS predefinidos           | Descrição                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Um **elemento EFFECTS** que itera pelos efeitos disponíveis. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




