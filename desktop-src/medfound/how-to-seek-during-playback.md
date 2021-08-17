---
description: Este tópico descreve como buscar durante a reprodução usando MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Como buscar durante a reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47e035ff8cc3764a9080698e8596660ce61907319bda70ac019b4cba1f8c27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974415"
---
# <a name="how-to-seek-during-playback"></a>Como buscar durante a reprodução

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tópico descreve como buscar durante a reprodução usando MFPlay.

**Para buscar durante a reprodução**

1.  Inicialize um **PROPVARIANT** para manter o tempo de busca em unidades de 100 nanossegundos, como um tipo **INTEGER \_ GRANDE** (**VT \_ I8**).
2.  Chame [**IMFPMediaPlayer::SetPosition.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition) **Especifique MFP \_ POSITIONTYPE \_ 100NS** para o primeiro parâmetro e passe **o PROPVARIANT** para o segundo parâmetro.

## <a name="requirements"></a>Requisitos

O MFPlay requer Windows 7.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



