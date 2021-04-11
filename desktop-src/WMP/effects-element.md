---
title: Elemento EFFECTs
description: Elemento EFFECTs
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Elemento skins, EFFECTs do Windows Media Player
- elemento skins, EFFECTs
- Elemento EFFECTs
- referência de capas, elemento EFFECTs
- elementos, efeitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b6fdcde74288b0dd4215732d1e5b6a281154f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363676"
---
# <a name="effects-element"></a>Elemento EFFECTs

O elemento **Effects** fornece uma maneira de organizar e manipular visualizações usando os seguintes atributos e métodos. Um elemento **Effects** predefinido também é fornecido por conveniência.

O elemento **Effects** dá suporte aos seguintes atributos.



| Atributo                                                        | Descrição                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | Especifica ou recupera um valor que indica se todas as visualizações devem ser incluídas no registro.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Especifica ou recupera a visualização atual.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Recupera o número de predefinições disponíveis para a visualização atual.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Recupera o título de exibição da visualização atual.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Recupera o nome do registro da visualização atual.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Especifica ou recupera a predefinição atual da visualização atual.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Recupera o título da predefinição atual da visualização atual.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Recupera um valor que indica se a visualização atual pode ser exibida em tela inteira.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Recupera o número de visualizações disponíveis.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Recupera um valor que indica se a visualização atual tem uma página de propriedades.                                                                                                                                                                  |
| [Tela inteira](effects-fullscreen.md)                             | Especifica ou recupera um valor que indica se a visualização atual é exibida em tela inteira. Só pode ser definido em tempo de execução.                                                                                                                   |
| [em janelas](effects-windowed.md)                                 | Especifica ou recupera um valor que indica se a visualização será em janela ou sem janela, ou seja, se o retângulo inteiro do controle estará sempre visível ou se ele pode ser recortado. Só pode ser definido em tempo de design. |



 

O elemento **Effects** dá suporte aos métodos a seguir.



| Método                                       | Descrição                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Recupera o nome amigável da visualização com o índice de registro especificado.                               |
| [efeito de](effects-effecttype.md)         | Recupera o nome do registro da visualização com o índice de registro especificado.                               |
| [avançar](effects-next.md)                     | Exibe a próxima predefinição de visualização, movendo para a próxima visualização, se necessário.                            |
| [nextEffect](effects-nexteffect.md)         | Exibe a primeira predefinição da próxima visualização, ignorando as predefinições intermediárias.                                |
| [nextPreset](effects-nextpreset.md)         | Exibe a próxima predefinição da visualização atual.                                                            |
| [Anterior](effects-previous.md)             | Exibe a predefinição de visualização anterior, movendo para a última predefinição da visualização anterior, se necessário. |
| [previousEffect](effects-previouseffect.md) | Exibe a visualização anterior, ignorando as predefinições.                                                            |
| [previousPreset](effects-previouspreset.md) | Exibe a predefinição anterior da visualização atual.                                                        |
| [configurações](effects-settings.md)             | Exibe a página de atributo da visualização atual, se presente.                                            |



 

O elemento **Effects** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente. Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Efeitos predefinidos são elementos de **efeitos** normais com várias configurações de atributo comuns especificadas por padrão. Os seguintes efeitos predefinidos estão disponíveis.



| EFEITOS predefinidos           | Descrição                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Um elemento **Effects** que percorre os efeitos disponíveis. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




