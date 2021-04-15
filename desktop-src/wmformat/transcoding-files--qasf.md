---
title: Transcodificação de arquivos (QASF)
description: Transcodificação de arquivos (QASF)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- SDK do Windows Media Format, transcodificação de arquivos (QASF)
- SDK do Windows Media Format, DirectShow
- Formato de sistema avançado (ASF), transcodificação de arquivos (QASF)
- ASF (formato de sistemas avançados), transcodificação de arquivos (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, transcodificação de arquivos (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104570133"
---
# <a name="transcoding-files-qasf"></a>Transcodificação de arquivos (QASF)

Você pode criar um grafo de filtro de transcodificação de arquivo usando o [gravador ASF do WM](wm-asf-writer-filter.md) de várias maneiras. A maneira mais fácil é criar, configurar e adicionar o gravador ASF do WM ao grafo de filtro e, em seguida, usar o método **IGraphBuilder:: RenderFile** para criar o grafo automaticamente.

Uma maneira alternativa é adicionar cada filtro manualmente ao grafo e conectar os Pins. Depois de adicionar o gravador ASF do WM, configure-o usando os métodos **IConfigAsfWriter** se o perfil padrão não for adequado e conecte os Pins de entrada do gravador ASF do WM aos pins de saída correspondentes nos filtros upstream.

A ilustração a seguir mostra as configurações típicas de gráfico de filtro de transcodificação do gravador ASF do WM.

![gráficos de filtro de transcodificação típicos](images/asf-transcode.png)

 

 




