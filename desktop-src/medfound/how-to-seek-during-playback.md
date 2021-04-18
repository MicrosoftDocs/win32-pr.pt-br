---
description: Este tópico descreve como buscar durante a reprodução usando o MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Como buscar durante a reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789477"
---
# <a name="how-to-seek-during-playback"></a>Como buscar durante a reprodução

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como buscar durante a reprodução usando o MFPlay.

**Para buscar durante a reprodução**

1.  Inicialize um **PROPVARIANT** para manter o tempo de busca em unidades de 100 nanossegundos, como um tipo **\_ inteiro** (**VT \_ i8**).
2.  Chame [**IMFPMediaPlayer:: SETPOSITION**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition). Especifique **o \_ PositionType do MFP de \_ 100 NS** para o primeiro parâmetro e passe o **PROPVARIANT** para o segundo parâmetro.

## <a name="requirements"></a>Requisitos

O MFPlay requer o Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



