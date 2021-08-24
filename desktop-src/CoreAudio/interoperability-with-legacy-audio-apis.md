---
description: Interoperabilidade com APIs de áudio herdadas
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilidade com APIs de áudio herdadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f894c20785ebd49e50765ad67ba19056f5439bd5ab8c8fc7e0bcfbdd05fe04ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875426"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilidade com APIs de áudio herdadas

muitos aplicativos existentes usam APIs de áudio herdadas como DirectSound, DirectShow e as funções de multimídia Windows. com apenas pequenas modificações, esses aplicativos podem ser aumentados para fazer uso de [funções de dispositivo](device-roles.md), [controles de volume de sessão](session-volume-controls.md)e outros recursos das APIs de áudio de núcleo no Windows Vista.

Conforme discutido nos [componentes de áudio do modo de usuário](user-mode-audio-components.md), as principais APIs de áudio servem como base na qual as APIs de áudio de nível superior são criadas. no Windows Vista, os dispositivos de áudio que os aplicativos acessam por meio de APIs de áudio herdadas, como DirectSound e as funções de Windows media **waveOutXxx** e **waveInXxx** são, de fato, [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) implementados pelas APIs de áudio principal. Devido a limitações inerentes nas interfaces de APIs de áudio herdadas, um aplicativo pode acessar alguns, mas não todos os recursos de dispositivos de ponto de extremidade de áudio por meio dessas interfaces. As seções a seguir descrevem as técnicas para aprimorar os aplicativos existentes, acessando recursos adicionais dos dispositivos de ponto de extremidade de áudio diretamente por meio das APIs de áudio principal. Esses aprimoramentos normalmente exigem apenas pequenas alterações no código do aplicativo existente.

As seções a seguir descrevem como incorporar recursos das APIs de áudio principais em aplicativos existentes que usam APIs de áudio herdadas:

-   [Funções de dispositivo para aplicativos DirectSound](device-roles-for-directsound-applications.md)
-   [funções de dispositivo para aplicativos DirectShow](device-roles-for-directshow-applications.md)
-   [funções de dispositivo para aplicativos multimídia Windows herdados](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Eventos de áudio para aplicativos de áudio herdados](audio-events-for-legacy-audio-applications.md)
-   [Sons de notificação para aplicativos de áudio herdados](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de dispositivo](device-roles.md)
</dt> </dl>

 

 



