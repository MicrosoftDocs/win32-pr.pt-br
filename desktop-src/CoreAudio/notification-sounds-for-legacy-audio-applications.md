---
description: Sons de notificação para aplicativos de áudio herdados
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Sons de notificação para aplicativos de áudio herdados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce813fb2d38a9995f929c62936879f502392415d040e88ddb50f3b4699734a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077520"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a>Sons de notificação para aplicativos de áudio herdados

no Windows Vista, o sistema operacional atribui todos os seus sons de notificação do sistema a uma sessão de áudio de processo cruzado que é executada por meio do dispositivo de ponto de extremidade de renderização que está atualmente atribuído à [função de dispositivo](device-roles.md)eConsole. O programa de controle de volume do sistema, SNDVOL, exibe um controle deslizante de volume que é dedicado a sons de notificação do sistema.

Alguns aplicativos reproduzem sons de notificação. Em vez de exigir que o usuário gerencie a notificação de um aplicativo com um controle deslizante de volume separado no SNDVOL, o aplicativo pode atribuir seus sons de notificação à mesma sessão que os sons de notificação do sistema. O controle deslizante de volume SNDVOL que controla os sons de notificação do sistema controla os sons de notificação do aplicativo.

para habilitar esse comportamento, Windows o Vista define um \_ sinalizador de sistema do SND para a função de [**PlaySound**](/previous-versions//dd743680(v=vs.85)) herdada. (esse sinalizador não tem suporte em versões anteriores do Windows, incluindo Windows Server 2003, Windows XP e Windows 2000.) Se o chamador definir esse sinalizador, a função **PlaySound** atribuirá o som que ele toca à sessão de processo cruzado que o sistema operacional usa para seus sons de notificação. Se o chamador não definir o sinalizador, o **PlaySound** atribuirá o som que ele toca à sessão padrão — a sessão específica do processo que é identificada pelo valor GUID de sessão GUID \_ NULL. \_O sistema SND é definido no arquivo de cabeçalho mmsystem. h. para obter mais informações sobre o **PlaySound**, consulte a documentação do SDK do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interoperabilidade com APIs de áudio herdadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
