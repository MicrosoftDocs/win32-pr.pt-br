---
description: Interoperabilidade com APIs de áudio herdadas
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilidade com APIs de áudio herdadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920486"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilidade com APIs de áudio herdadas

Muitos aplicativos existentes usam APIs de áudio herdadas, como DirectSound, DirectShow e as funções de multimídia do Windows. Com apenas pequenas modificações, esses aplicativos podem ser aumentados para fazer uso de [funções de dispositivo](device-roles.md), [controles de volume de sessão](session-volume-controls.md)e outros recursos das principais APIs de áudio no Windows Vista.

Conforme discutido nos [componentes de áudio do modo de usuário](user-mode-audio-components.md), as principais APIs de áudio servem como base na qual as APIs de áudio de nível superior são criadas. No Windows Vista, os dispositivos de áudio que os aplicativos acessam por meio de APIs de áudio herdadas como DirectSound e as funções **waveOutXxx** e **waveInXxx** do Windows Media são, de fato, [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) implementados pelas APIs de áudio principal. Devido a limitações inerentes nas interfaces de APIs de áudio herdadas, um aplicativo pode acessar alguns, mas não todos os recursos de dispositivos de ponto de extremidade de áudio por meio dessas interfaces. As seções a seguir descrevem as técnicas para aprimorar os aplicativos existentes, acessando recursos adicionais dos dispositivos de ponto de extremidade de áudio diretamente por meio das APIs de áudio principal. Esses aprimoramentos normalmente exigem apenas pequenas alterações no código do aplicativo existente.

As seções a seguir descrevem como incorporar recursos das APIs de áudio principais em aplicativos existentes que usam APIs de áudio herdadas:

-   [Funções de dispositivo para aplicativos DirectSound](device-roles-for-directsound-applications.md)
-   [Funções de dispositivo para aplicativos do DirectShow](device-roles-for-directshow-applications.md)
-   [Funções de dispositivo para aplicativos multimídia herdados do Windows](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md)
-   [Sons de notificação para aplicativos de áudio herdados](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de dispositivo](device-roles.md)
</dt> </dl>

 

 



