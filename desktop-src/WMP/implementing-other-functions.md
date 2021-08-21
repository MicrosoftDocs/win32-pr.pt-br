---
title: Implementando outras funções
description: Implementando outras funções
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- visualizações, interface IWMPEffects
- visualizações personalizadas, interface IWMPEffects
- visualizações, função render
- visualizações personalizadas, função render
- Função render, funções adicionais
- Interface IWMPEffects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73392204357ec856c5c04f2a0f24028ea29e5f09c3aa203d95ed8e2cc7e4ded3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508926"
---
# <a name="implementing-other-functions"></a>Implementando outras funções

Definitivamente, você desejará escrever sua própria implementação da função **render** . Várias outras funções que também são funções membro da interface **IWMPEffects** são fornecidas. algumas fornecerão informações extras que você pode optar por usar e outras fornecerão automaticamente Windows Media Player com informações que foram geradas pelo assistente, como o nome de sua visualização.

A interface **IWMPEffects** dá suporte às seguintes funções, além de **render**:



| Função                                                   | Descrição                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Implementação padrão não fornecida pelo assistente.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Obtém os recursos de sua visualização e os transmite para Windows Media Player.                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | O assistente criou duas predefinições quando gerou o código para sua visualização. Essa função é chamada quando o desenvolvedor de pele deseja obter o índice da predefinição atual. Você não vai querer alterar a implementação dessa função porque ela usa apenas as informações definidas por outras funções. |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | O assistente criou duas predefinições quando gerou o código para sua visualização. Você pode alterar a contagem alterando a implementação de **GetPresetCount**. Confira [predefinições](presets.md) para obter mais informações sobre como alterar as predefinições.                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | O assistente criou duas predefinições quando gerou o código para sua visualização. Você pode alterar os títulos usados alterando a implementação de **GetPresetTitle**. Confira [predefinições](presets.md) para obter mais informações sobre como alterar as predefinições.                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Obtém o título de sua visualização e a passa para Windows Media Player. O assistente usou o nome do seu projeto para gerar o nome que é passado de volta.                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Implementação padrão não fornecida pelo assistente.                                                                                                                                                                                                                                                           |
| [MediaInfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Recupera o número de canais de áudio e a taxa de amostragem do áudio atualmente em execução.                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Implementação padrão não fornecida pelo assistente.                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | O assistente criou duas predefinições quando gerou o código para sua visualização. essa função é chamada quando Windows Media Player deseja alterar para uma predefinição nomeada.                                                                                                                                   |



 

A interface **IWMPEffects2** dá suporte às seguintes funções adicionais:



| Função                                            | Descrição                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criar](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | ao renderizar em uma janela, Windows Media Player chama essa função para permitir que você crie uma nova janela para renderização.                          |
| [Destruir](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | ao renderizar em uma janela, Windows Media Player chama essa função para permitir que você destrua a janela criada quando **Create** foi chamado. |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Essa função permite que sua visualização responda quando um novo item de mídia tiver sido carregado pelo Player.                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Essa função recebe mensagens do Windows do Player ao renderizar no modo sem janela.                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Essa função é chamada pelo Player em vez de **IWMPEffects:: render** quando o player está sendo renderizado no modo de janela.                          |
| [Setcore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Essa função recebe um ponteiro para a interface **IWMPCore** .                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando seu código**](implementing-your-code.md)
</dt> </dl>

 

 




