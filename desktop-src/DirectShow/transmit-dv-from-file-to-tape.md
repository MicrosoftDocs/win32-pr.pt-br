---
description: Transmitir DV do arquivo para a fita
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmitir DV do arquivo para a fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768521"
---
# <a name="transmit-dv-from-file-to-tape"></a>Transmitir DV do arquivo para a fita

Transmitir do arquivo DV AVI para a fita VTR é complicado um pouco pelo fato de que os arquivos podem digitar-1 ou tipo-2. Para transmitir um arquivo DV para fita, faça o seguinte:

1.  Crie uma instância do filtro de [Driver MSDV](msdv-driver.md) . Para obter mais informações, consulte [selecionando um dispositivo de captura](selecting-a-capture-device.md).
2.  Verifique se o dispositivo está no modo VTR. Caso contrário, você não poderá transmitir para fita. Consulte [modo de dispositivo](device-mode.md).
3.  Inicialize o construtor de gráficos de captura, conforme descrito em [sobre o construtor de grafo de captura](about-the-capture-graph-builder.md).
4.  Crie o grafo. A configuração do grafo depende do tipo de arquivo DV:
    -   [Transmitir do arquivo do tipo-1](transmit-from-type-1-file.md)
    -   [Transmitir do arquivo do tipo 2](transmit-from-type-2-file.md)
5.  Coloque o dispositivo no modo de pausa de registro, conforme descrito em [controlando uma camcorder DV](controlling-a-dv-camcorder.md).
6.  Pause o gráfico de filtro. Enquanto o grafo de filtro é pausado, ele envia um fluxo contínuo que repete o primeiro quadro de vídeo.
7.  Para iniciar a transmissão, coloque o dispositivo no modo de registro e, em seguida, execute o gráfico de filtro. O dispositivo leva um determinado período de tempo até que a cabeça de gravação seja capaz de gravar, portanto, aguarde cerca de dois segundos antes de executar o grafo. Isso pode resultar em alguns quadros duplicados no início da fita, mas garante que nenhum dado seja perdido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



