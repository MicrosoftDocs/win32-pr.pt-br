---
title: Janela Opções avançadas de caractere (janela Comandos de Voz)
description: Saiba mais sobre a Janela Opções Avançadas de Caracteres, que fornece opções para os usuários ajustarem sua interação com todos os caracteres.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404350"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Janela Opções avançadas de caractere (janela Comandos de Voz)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A janela Opções avançadas de caractere fornece opções para que os usuários ajustem sua interação com todos os caracteres. Por exemplo, os usuários podem desabilitar a entrada de fala ou alterar parâmetros de entrada. Os usuários também podem alterar as configurações de saída para a palavra balão. Essas configurações substituem qualquer conjunto por um aplicativo cliente ou definidos como parte da definição de caracteres. Seu aplicativo não pode alterar nem desabilitar essas opções, pois elas se aplicam às preferências gerais do usuário para a operação de todos os caracteres. No entanto, o servidor notificará seu aplicativo ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) quando o usuário mudar e aplicar uma opção. Você também pode exibir ou fechar a janela usando a propriedade [**Visible**](visible-property.md) da janela e acessar seu local por meio de suas [**propriedades Superior**](top-property.md) [**e**](left-property.md) Esquerda.

Além de dar suporte à animação de um caractere, o Microsoft Agent dá suporte à saída de áudio para o caractere. Isso inclui a saída falada e efeitos de som. Para a saída falada, o servidor sincroniza automaticamente as imagens de boca definidas do caractere com a saída. Você pode escolher a síntese de TTS (texto em fala), áudio gravado ou apenas saída de texto de balão de palavra.

 

 




