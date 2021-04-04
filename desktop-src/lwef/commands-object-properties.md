---
title: Propriedades do objeto Commands
description: Propriedades do objeto Commands
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4493b1e146a011434f7a0324a4008031a575d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007384"
---
# <a name="commands-object-properties"></a>Propriedades do objeto Commands

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor oferece suporte às seguintes propriedades para a coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) :

-   [**Legenda**](caption-property-cmds.md)
-   [**Contar**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**HelpContextid**](helpcontextid-property.md)
-   [**Visible**](visible-property-cso.md)
-   [**Voz**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

Uma entrada para a coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) pode aparecer no menu pop-up e na janela de comandos de voz para um caractere. Para fazer essa entrada aparecer no menu pop-up, defina sua propriedade [**Caption**](caption-property-cmds.md) . Para incluir a entrada na janela de comandos de voz, defina sua propriedade [**VoiceCaption**](voicecaption-property.md) . (Para compatibilidade com versões anteriores, se não houver nenhum **VoiceCaption**, a configuração de **legenda** será usada)

A tabela a seguir resume como as propriedades de um objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) afetam a apresentação da entrada:



| Propriedade Caption                                                                                                                                                                                                                                            | Propriedade Voice-Caption | Propriedade de voz | Propriedade Visible | Aparece no menu pop-up do caractere | Aparece na janela de comandos de voz |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Sim                                                                                                                                                                                                                                                         | Sim                    | Sim            | True             | Sim, usando legenda                 | Sim, usando VoiceCaption          |
| Sim                                                                                                                                                                                                                                                         | Sim                    | Não             | True             | Sim, usando legenda                 | Não                               |
| Sim                                                                                                                                                                                                                                                         | Sim                    | Sim            | Falso            | Não                                 | Sim, usando VoiceCaption          |
| Sim                                                                                                                                                                                                                                                         | Sim                    | Não             | Falso            | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Sim                    | Sim            | True             | Não                                 | Sim, usando VoiceCaption          |
| Não                                                                                                                                                                                                                                                          | Sim                    | Sim            | Falso            | Não                                 | Sim, usando VoiceCaption          |
| Não                                                                                                                                                                                                                                                          | Sim                    | Não             | True             | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Sim                    | Não             | Falso            | Não                                 | Não                               |
| Sim                                                                                                                                                                                                                                                         | Nº 1                    | Sim            | True             | Sim, usando legenda                 | Sim, usando legenda               |
| Sim                                                                                                                                                                                                                                                         | Não                     | Não             | True             | Sim                                | Não                               |
| Sim                                                                                                                                                                                                                                                         | Não                     | Sim            | Falso            | Não                                 | Sim, usando legenda               |
| Sim                                                                                                                                                                                                                                                         | Não                     | Não             | Falso            | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Sim            | True             | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Sim            | Falso            | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Não             | True             | Não                                 | Não                               |
| Não                                                                                                                                                                                                                                                          | Não                     | Não             | Falso            | Não                                 | Não                               |
|  Se a configuração da propriedade for nula. Em algumas linguagens de programação, uma cadeia de caracteres vazia não pode ser interpretada como a mesma que uma cadeia de caracteres nula.  O comando ainda é acessível por voz e aparece na janela comandos de voz como "(comando indefinido)".<br/> |                        |                |                  |                                    |                                  |



 

 

