---
title: Capturando diretamente de um dispositivo para um arquivo ASF (QASF)
description: Capturando diretamente de um dispositivo para um arquivo ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- SDK do Windows Media Format, capturando de dispositivos para arquivos ASF (QASF)
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), capturando de dispositivos (QASF)
- ASF (formato de sistemas avançados), capturando de dispositivos (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, capturando de dispositivos para arquivos ASF (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105812234"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Capturando diretamente de um dispositivo para um arquivo ASF (QASF)

Ao capturar áudio ou vídeo diretamente em um arquivo ASF, o grafo de filtro é semelhante ao diagrama a seguir, dependendo do tipo de dispositivo de captura que está sendo usado.

![Grafo de captura de webcam para WMV](images/asf-webcam.png)

A documentação do SDK do DirectShow descreve detalhadamente como criar gráficos de captura, mas há um ponto importante a ser lembrado ao criar gráficos de captura usando o gravador ASF do WM: o gravador ASF do WM não será executado, a menos que todos os seus PINs estejam conectados. Se você configurar o gravador ASF do WM com o perfil de sistema padrão (não recomendado) ou qualquer perfil com fluxos de áudio e vídeo, ele criará um PIN de entrada para cada fluxo e cada um desses Pins deverá ser conectado. Se você não pretende capturar áudio, por exemplo, certifique-se de configurar o filtro com um perfil somente de vídeo para que nenhum PIN de áudio seja criado.

 

 




