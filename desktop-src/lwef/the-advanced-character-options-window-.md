---
title: Janela Opções avançadas de caractere (janela comandos de voz)
description: A janela Opções de caractere avançadas
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f481871d3861da99b54829e5c6e1b34c9137060a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294678"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Janela Opções avançadas de caractere (janela comandos de voz)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A janela Opções avançadas de caractere fornece opções para que os usuários ajustem sua interação com todos os caracteres. Por exemplo, os usuários podem desabilitar a entrada de fala ou alterar os parâmetros de entrada. Os usuários também podem alterar as configurações de saída para a palavra balão. Essas configurações substituem qualquer conjunto por um aplicativo cliente ou definidos como parte da definição de caractere. Seu aplicativo não pode alterar ou desabilitar essas opções, pois elas se aplicam às preferências gerais do usuário para a operação de todos os caracteres. No entanto, o servidor notificará seu aplicativo ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) quando o usuário alterar e aplicar uma opção. Você também pode exibir ou fechar a janela usando a propriedade [**Visible**](visible-property.md) da janela e acessar seu local por meio de suas propriedades [**Top**](top-property.md) e [**Left**](left-property.md) .

Além de dar suporte à animação de um caractere, o Microsoft Agent dá suporte à saída de áudio para o caractere. Isso inclui efeitos de som e saída falados. Para saída falada, o servidor automaticamente o Lip sincroniza as imagens de boca definidas pelo caractere para a saída. Você pode escolher a síntese de conversão de texto em fala (TTS), áudio gravado ou apenas a saída de texto de balão de palavras.

 

 




