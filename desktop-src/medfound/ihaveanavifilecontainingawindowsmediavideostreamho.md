---
description: Tenho um arquivo AVI contendo um fluxo de vídeo do Windows Media.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Tenho um arquivo AVI contendo um fluxo de vídeo do Windows Media. Como posso convertê-lo em um arquivo WMV?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105765608"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a>Tenho um arquivo AVI contendo um fluxo de vídeo do Windows Media. Como posso convertê-lo em um arquivo WMV?

As interfaces do codec de áudio e vídeo do Windows Media não fornecem métodos para criar arquivos usando o ASF (Advanced Systems Format), que é o formato usado para arquivos WMV. Se você quiser converter um arquivo (usando qualquer contêiner) em um arquivo ASF, deverá usar os objetos do Windows Media Format SDK.

Recupere os exemplos do Windows Media compactados do arquivo de origem e passe-os para o objeto do gravador como amostras de fluxo. Para obter mais informações, consulte a documentação do SDK da série Windows Media Format 9 Series.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



