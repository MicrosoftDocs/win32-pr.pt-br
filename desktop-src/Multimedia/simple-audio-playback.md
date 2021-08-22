---
title: Reprodução de áudio simples
description: Reprodução de áudio simples
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- áudio multimídia, forma de onda
- audio,waveform
- áudio de forma de onda, reprodução simples
- Função MessageBeep
- Função sndPlaySound
- Função PlaySound, reprodução simples
- áudio multimídia, função PlaySound
- audio, função PlaySound
- waveform audio, função PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6388f9800f93080e995ae537c2458a22da033ab2149b4bfca114c25025d97434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688686"
---
# <a name="simple-audio-playback"></a>Reprodução de áudio simples

Você pode usar as funções a seguir para reproduzir áudio waveform em seu aplicativo em uma única chamada de função.



| Função                                                      | Descrição                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Messagebeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Reproduz o som que corresponde a um nível de alerta do sistema especificado.                                                 |
| [**Sndplaysound**](/previous-versions//dd798676(v=vs.85))                          | Reproduz o som que corresponde ao som do sistema inserido no Registro ou ao conteúdo do arquivo especificado. |
| [**Playsound**](/previous-versions//dd743680(v=vs.85))                                | Fornece toda a funcionalidade do [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e pode acessar diretamente os recursos.           |



 

A **função MessageBeep** é uma parte padrão da API do Win32; como seus recursos são muito limitados e estão documentados em outro lugar, isso não é discutido aqui.

As funções listadas suportam as seguintes fontes de áudio waveform:

-   Arquivos waveform-audio associados aos níveis de alerta do sistema
-   Arquivos waveform-audio especificados por entradas no Registro
-   Recursos WAVE na memória
-   Arquivos waveform-audio especificados pelo nome

As [**funções sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e [**PlaySound**](/previous-versions//dd743680(v=vs.85)) carregam um arquivo waveform-audio inteiro na memória e, na verdade, limitam o tamanho do arquivo que podem reproduzir. Use **sndPlaySound** e **PlaySound** para reproduzir arquivos waveform-audio pequenos – até cerca de 100 mil. Essas duas funções também exigem que os dados de som sejam em um formato reproduzível por um dos drivers de áudio de forma de onda instalados, incluindo o mapeado de onda.

Para arquivos de som maiores, use os serviços MCI (Interface de Controle de Mídia). Para obter mais informações, consulte [MCI](mci.md).

 

 