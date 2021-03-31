---
title: Inserindo formatos de fluxo nativos em arquivos ASF (QASF)
description: Inserindo formatos de fluxo nativos em arquivos ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- SDK do Windows Media Format, formatos de fluxo nativos (QASF)
- SDK do Windows Media Format, inserindo formatos de fluxo nativos em arquivos ASF (QASF)
- SDK do Windows Media Format, DirectShow
- Formato de sistema avançado (ASF), inserção de formatos de fluxo nativos (QASF)
- ASF (formato de sistemas avançados), inserindo formatos de fluxo nativos (QASF)
- ASF (Advanced Systems Format), QASF (formatos de fluxo nativos)
- ASF (formato de sistemas avançados), formatos de fluxo nativos (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, formatos de fluxo nativos (QASF)
- DirectShow, inserindo formatos de fluxo nativos em arquivos ASF (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822906"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Inserindo formatos de fluxo nativos em arquivos ASF (QASF)

Por padrão, o [gravador ASF do WM](wm-asf-writer-filter.md) espera fluxos de áudio e vídeo descompactados em seus PINs de entrada e usa o Windows Media Format SDK para acessar os codecs de vídeo do Windows Media Audio e Windows Media, que compactam os fluxos. Mas o contêiner de arquivo ASF pode ser usado para qualquer tipo de dados. Ao colocar dados de mídia digital em um contêiner de arquivo ASF, você pode adicionar recursos fornecidos pelo ASF, como metadados e DRM (gerenciamento de direitos digitais), sem a necessidade de transcodificar o conteúdo.

Para criar um arquivo ASF que contém conteúdo que não é baseado no Windows Media, o aplicativo deve compactar o fluxo no fluxo do grafo de filtro do gravador ASF do WM e ignorar o mecanismo de compactação do gravador ASF do WM chamando [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) da seguinte maneira:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



Em seguida, configure o filtro com o perfil desejado. É essencial que o tipo de mídia do fluxo de entrada corresponda exatamente ao formato no perfil. Em alguns casos, pode ser necessário examinar o formato do fluxo de entrada e criar um perfil personalizado para fazer a correspondência. Para obter mais informações, consulte [para criar arquivos ASF usando codecs de](to-create-asf-files-using-third-party-codecs.md)terceiros.

Ao conectar o gravador ASF do WM ao filtro upstream, use o método **IGraphBuilder:: ConnectDirect** . Não use nenhum método de "conexão inteligente" como **IGraphBuilder:: Connect** ou **IGraphBuilder:: RenderFile** para conectar o filtro, pois isso desabilitará o modo "ignorar compactação" do filtro.

 

 




