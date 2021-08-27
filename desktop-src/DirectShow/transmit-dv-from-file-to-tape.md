---
description: Transmitir DV de arquivo para fita
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmitir DV de arquivo para fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bcd7bf716466cda2fc23a03968da4a51c005070f885183390f944d14994ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086786"
---
# <a name="transmit-dv-from-file-to-tape"></a>Transmitir DV de arquivo para fita

Transmitir do arquivo DV AVI para a fita VTR é um pouco complicado pelo fato de que os arquivos podem ser do tipo 1 ou do tipo 2. Para transmitir um arquivo DV para fita, faça o seguinte:

1.  Crie uma instância do filtro [driver MSDV.](msdv-driver.md) Para obter mais informações, consulte [Selecionando um dispositivo de captura](selecting-a-capture-device.md).
2.  Certifique-se de que o dispositivo está no modo VTR. Caso contrário, você não poderá transmitir para fita. Consulte [Modo de Dispositivo](device-mode.md).
3.  Inicialize o Construtor Graph De captura, conforme descrito em [Sobre o Construtor Graph Capture.](about-the-capture-graph-builder.md)
4.  Crie o grafo. A configuração do grafo depende do tipo de arquivo DV:
    -   [Transmitir do arquivo type-1](transmit-from-type-1-file.md)
    -   [Transmitir do arquivo Type-2](transmit-from-type-2-file.md)
5.  Coloque o dispositivo no modo de pausa de registro, conforme descrito em [Controlando uma gravação DV.](controlling-a-dv-camcorder.md)
6.  Pause o grafo de filtro. Enquanto o grafo de filtro está em pausa, ele envia um fluxo contínuo que repete o primeiro quadro de vídeo.
7.  Para começar a transmitir, coloque o dispositivo no modo de registro e execute o grafo de filtro. O dispositivo leva um determinado período de tempo até que o cabece de gravação seja capaz de gravar, portanto, aguarde cerca de dois segundos antes de executar o grafo. Isso pode resultar em alguns quadros duplicados no início da fita, mas garante que nenhum dado seja perdido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



