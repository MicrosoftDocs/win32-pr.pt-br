---
title: Tipos de dispositivo
description: Tipos de dispositivo
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636724"
---
# <a name="device-types"></a>Tipos de dispositivo

O MCI reconhece um conjunto básico de *tipos de dispositivo*. Um tipo de dispositivo é um conjunto de drivers MCI que compartilham um conjunto de comandos comum e são usados para controlar dispositivos multimídia ou arquivos de dados semelhantes. Muitos comandos MCI, como [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), exigem que você especifique um tipo de dispositivo.

A tabela a seguir lista os tipos de dispositivos definidos. A implementação atual do MCI inclui conjuntos de comandos para um subconjunto desses dispositivos.



| Tipo de dispositivo      | Constante                      | Descrição                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | \_áudio MCI DEVTYPE \_ CD \_       | Player de áudio de CD                                  |
| **DATs**          | \_dat DEVTYPE \_ MCI             | Player de fita de áudio digital                        |
| **digitalvideo** | \_ \_ vídeo digital DEVTYPE \_ MCI  | Vídeo digital em uma janela (não baseado em GDI)        |
| **outros**        | \_DEVTYPE MCI \_           | Dispositivo MCI indefinido                             |
| **Overlay**      | sobreposição de \_ DEVTYPE MCI \_         | Dispositivo de sobreposição (vídeo analógico em uma janela)        |
| **detector**      | \_scanner MCI DEVTYPE \_         | Scanner de imagem                                    |
| **sequenciador**    | \_ \_ sequenciador DEVTYPE MCI       | Sequenciador MIDI                                   |
| **videocassete**          | \_VCR DEVTYPE \_ MCI             | Gravador ou player de fita de vídeo                |
| **videodisc**    | \_VIDEODISC MCI DEVTYPE \_       | VIDEODISC Player                                 |
| **waveaudio**    | \_áudio MCI DEVTYPE \_ Wave \_ | Dispositivo de áudio que reproduz arquivos de formato de onda digitalizados |



 

Neste documento, os nomes dos tipos de dispositivo estão em negrito. Nomes de tipo de dispositivo são usados com a interface de cadeia de caracteres de comando. As constantes do tipo de dispositivo são usadas com a interface de mensagem de comando.

 

 




