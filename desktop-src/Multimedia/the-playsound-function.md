---
title: A função PlaySound
description: A função PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- áudio de multimídia, função PlaySound
- áudio, função PlaySound
- áudio de onda, função PlaySound
- Função PlaySound, sobre
- função sndPlaySound
- Função PlaySound, em comparação com a função sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1921ec4ef91f6266b48ee80d7f42be4540124c0b5c98dc18438ce0d16c398c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370846"
---
# <a name="the-playsound-function"></a>A função PlaySound

Você pode usar a função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproduzir áudio de onda se o som couber na memória disponível. (A função [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) oferece um subconjunto dos recursos do PlaySound. Para maximizar a portabilidade do seu aplicativo baseado em Win32, use o **PlaySound**, não **sndPlaySound**.)

A função **PlaySound** permite que você especifique um som de uma das três maneiras:

-   Como um alerta do sistema, usando o alias armazenado no arquivo de WIN.INI ou no registro
-   Como um nome de arquivo
-   Como um identificador de recurso

A função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) permite reproduzir um som em um loop contínuo, terminando somente quando você chama o **PlaySound** novamente, especificando **NULL** ou o identificador de som de outro som para o parâmetro *pszSound* .

Você pode usar o **PlaySound** para reproduzir o som de forma síncrona ou assíncrona e controlar o comportamento da função de outras maneiras quando ele deve compartilhar recursos do sistema.

Para obter mais informações sobre como usar o PlaySound, consulte os seguintes tópicos:

-   [Usando o PlaySound para reproduzir arquivos de Waveform-Audio](using-playsound-to-play-waveform-audio-files.md)
-   [Usando o PlaySound para repetir sons](using-playsound-to-loop-sounds.md)
-   [Usando o PlaySound para reproduzir sons do sistema](using-playsound-to-play-system-sounds.md)

Para obter mais exemplos de como usar o **PlaySound** em seus aplicativos baseados no Win32, consulte [reproduzindo recursos de onda](playing-wave-resources.md).

 

 