---
description: Tenho um arquivo AVI que contém um fluxo Windows vídeo de mídia.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Tenho um arquivo AVI que contém um fluxo Windows vídeo de mídia. Como convertê-lo em um arquivo WMV?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfc2a5980533487c7a1c8716806fcedda1c7147bdacaf3ea0c887acbff0f83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777136"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a>Tenho um arquivo AVI que contém um fluxo Windows vídeo de mídia. Como convertê-lo em um arquivo WMV?

As interfaces Windows codec de Áudio de Mídia e Vídeo não fornecem métodos para criar arquivos usando o ASF (Advanced Systems Format), que é o formato usado para arquivos WMV. Se você quiser converter um arquivo (usando qualquer contêiner) em um arquivo ASF, deverá usar os objetos do SDK Windows Formato de Mídia.

Recupere os exemplos Windows Mídia compactada do arquivo de origem e passe-os para o objeto de autor como amostras de fluxo. Para obter mais informações, consulte a documentação do SDK do Windows Media Format 9 Series.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



