---
title: Capturando diretamente de um dispositivo para um arquivo ASF (QASF)
description: Capturando diretamente de um dispositivo para um arquivo ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows SDK de Formato de Mídia, capturando de dispositivos para arquivos ASF (QASF)
- Windows SDK de formato de mídia, DirectShow
- ASF (Advanced Systems Format), capturando de dispositivos (QASF)
- ASF (Formato de Sistemas Avançados), capturando de dispositivos (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow,capturando de dispositivos para arquivos ASF (QASF)
- Windows SDK de formato de mídia, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570e773e39b4c2d76bd95f0a4ac90269be295585ef91e6e50f653b121cbc8d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705081"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Capturando diretamente de um dispositivo para um arquivo ASF (QASF)

Ao capturar áudio ou vídeo diretamente em um arquivo ASF, o grafo de filtro se parece com o diagrama a seguir, dependendo do tipo de dispositivo de captura que está sendo usado.

![webcam para grafo de captura de wmv](images/asf-webcam.png)

A documentação do SDK do DirectShow descreve detalhadamente como criar grafos de captura, mas há um ponto importante a ser lembrado ao criar grafos de captura usando o Wm ASF Writer: o Wm ASF Writer não será executado, a menos que todos os seus pinos sejam conectados. Se você configurar o Wm ASF Writer com o perfil de sistema padrão (não recomendado) ou qualquer perfil com fluxos de áudio e vídeo, ele criará um pino de entrada para cada fluxo e cada um desses pinos deverá estar conectado. Se você não pretende capturar áudio, por exemplo, configure o filtro com um perfil somente vídeo para que nenhum pino de áudio seja criado.

 

 




