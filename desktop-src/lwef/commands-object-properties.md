---
title: Propriedades do objeto Commands
description: Propriedades do objeto Commands
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b9e8f8e6e7b44697891cd567fce8ca0f5db13a0142936b5cf48bdb52721392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716536"
---
# <a name="commands-object-properties"></a>Propriedades do objeto Commands

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor dá suporte às seguintes propriedades para a [**coleção Comandos:**](/windows/desktop/lwef/the-commands-collection-object)

-   [**Legenda**](caption-property-cmds.md)
-   [**Contagem**](count-property.md)
-   [**Defaultcommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**HelpContextID**](helpcontextid-property.md)
-   [**Visível**](visible-property-cso.md)
-   [**Voz**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

Uma entrada para a [**coleção Comandos**](/windows/desktop/lwef/the-commands-collection-object) pode aparecer no menu pop-up e na Janela comandos de voz para um caractere. Para fazer com que essa entrada apareça no menu pop-up, de definido sua [**propriedade Caption.**](caption-property-cmds.md) Para incluir a entrada na janela Comandos de Voz, de definido sua [**propriedade VoiceCaption.**](voicecaption-property.md) (Para compatibilidade com backward, se não houver **VoiceCaption**, a **configuração Legenda** será usada)

A tabela a seguir resume como as propriedades de um [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) afetam a apresentação da entrada:



| Propriedade Caption                                                                                                                                                                                                                                            | Voice-Caption propriedade | Propriedade Voice | Propriedade Visible | Aparece no menu pop-up do caractere | Aparece na janela Comandos de Voz |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Sim                                                                                                                                                                                                                                                         | Sim                    | Sim            | Verdadeiro             | Sim, usando Legenda                 | Sim, usando VoiceCaption          |
| Sim                                                                                                                                                                                                                                                         | Sim                    | Não             | Verdadeiro             | Sim, usando Legenda                 | Não                               |
| Sim                                                                                                                                                                                                                                                         | Sim                    | Sim            | Falso            | Não                                 | Sim, usando VoiceCaption          |
| Sim                                                                                                                                                                                                                                                         | Sim                    | Não             | Falso            | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Sim                    | Sim            | True             | Não                                 | Sim, usando VoiceCaption          |
| Não                                                                                                                                                                                                                                                          | Sim                    | Sim            | Falso            | Não                                 | Sim, usando VoiceCaption          |
| Não                                                                                                                                                                                                                                                          | Sim                    | Não             | True             | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Sim                    | Não             | Falso            | Não                                 | Não                               |
| Sim                                                                                                                                                                                                                                                         | Nº 1                    | Sim            | Verdadeiro             | Sim, usando Legenda                 | Sim, usando Legenda               |
| Sim                                                                                                                                                                                                                                                         | Não                     | Não             | True             | Sim                                | Não                               |
| Sim                                                                                                                                                                                                                                                         | Não                     | Sim            | Falso            | Não                                 | Sim, usando Legenda               |
| Sim                                                                                                                                                                                                                                                         | Não                     | Não             | Falso            | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Sim            | True             | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Sim            | Falso            | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Não             | True             | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Não             | Falso            | Não                                 | Não                               |
|  Se a configuração de propriedade for nula. Em algumas linguagens de programação, uma cadeia de caracteres vazia pode não ser interpretada como a mesma que uma cadeia de caracteres nula.  O comando ainda é acessível por voz e aparece na Janela Comandos de Voz como "(comando indefinido)".<br/> |                        |                |                  |                                    |                                  |



 

 

