---
title: Tipos de dispositivo
description: Tipos de dispositivo
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167eedddfc61960de35e979480c44b8f2efab5bf89738047446196b81a95a5b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497156"
---
# <a name="device-types"></a>Tipos de dispositivo

A MCI reconhece um conjunto básico de tipos *de dispositivo.* Um tipo de dispositivo é um conjunto de drivers MCI que compartilham um conjunto de comandos comum e são usados para controlar dispositivos multimídia ou arquivos de dados semelhantes. Muitos comandos MCI, como [**open**](open.md) ([**MCI \_ OPEN**](mci-open.md)), exigem que você especifique um tipo de dispositivo.

A tabela a seguir lista os tipos de dispositivo definidos. A implementação atual da MCI inclui conjuntos de comandos para um subconjunto desses dispositivos.



| Tipo de dispositivo      | Constante                      | Descrição                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | MCI \_ DEVTYPE \_ CD \_ AUDIO       | Player de áudio de CD                                  |
| **Dat**          | MCI \_ DEVTYPE \_ DAT             | Player de fita de áudio digital                        |
| **digitalvideo** | VÍDEO DIGITAL MCI \_ DEVTYPE \_ \_  | Vídeo digital em uma janela (não baseado em GDI)        |
| **Outros**        | MCI \_ DEVTYPE \_ OTHER           | Dispositivo MCI indefinido                             |
| **Sobreposição**      | SOBREPOSIÇÃO \_ DE MCI DEVTYPE \_         | Dispositivo de sobreposição (vídeo análogo em uma janela)        |
| **scanner**      | MCI \_ DEVTYPE \_ SCANNER         | Scanner de imagem                                    |
| **sequenciador**    | MCI \_ DEVTYPE \_ SEQUENCER       | Sequenciador MIDI                                   |
| **Videocassete**          | MCI \_ DEVTYPE \_ VCR             | Gravador ou player de gravador de vídeo                |
| **videodisc**    | MCI \_ DEVTYPE \_ VIDEODISC       | Player do Videodisc                                 |
| **Waveaudio**    | MCI \_ DEVTYPE \_ WAVEFORM \_ AUDIO | Dispositivo de áudio que reproduz arquivos de forma de onda digitalizados |



 

Neste documento, os nomes dos tipos de dispositivo estão em negrito. Os nomes de tipo de dispositivo são usados com a interface de cadeia de caracteres de comando. Constantes de tipo de dispositivo são usadas com a interface de mensagem de comando.

 

 




