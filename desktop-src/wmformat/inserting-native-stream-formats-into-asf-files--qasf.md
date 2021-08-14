---
title: Inserindo formatos de fluxo nativos em arquivos ASF (QASF)
description: Inserindo formatos de fluxo nativos em arquivos ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows SDK do formato de mídia, QASF (formatos de fluxo nativos)
- Windows SDK do formato de mídia, inserindo formatos de fluxo nativos em arquivos ASF (QASF)
- Windows SDK do formato de mídia, DirectShow
- Formato de sistema avançado (ASF), inserção de formatos de fluxo nativos (QASF)
- ASF (formato de sistemas avançados), inserindo formatos de fluxo nativos (QASF)
- ASF (Advanced Systems Format), QASF (formatos de fluxo nativos)
- ASF (formato de sistemas avançados), formatos de fluxo nativos (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, formatos de fluxo nativos (QASF)
- DirectShow, inserindo formatos de fluxo nativos em arquivos ASF (QASF)
- Windows SDK do formato de mídia, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b395748520943a62645a88c018131f909577191ebafbe1f9c4d3a80219cb39f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701773"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Inserindo formatos de fluxo nativos em arquivos ASF (QASF)

por padrão, o [gravador ASF do WM](wm-asf-writer-filter.md) espera fluxos de áudio e vídeo descompactados em seus pins de entrada e usa o Windows SDK de formato de mídia para acessar os codecs de vídeo de mídia Windows e Windows de mídia, que compactam os fluxos. Mas o contêiner de arquivo ASF pode ser usado para qualquer tipo de dados. Ao colocar dados de mídia digital em um contêiner de arquivo ASF, você pode adicionar recursos fornecidos pelo ASF, como metadados e DRM (gerenciamento de direitos digitais), sem a necessidade de transcodificar o conteúdo.

para criar um arquivo ASF que contém conteúdo que não é Windows com base na mídia, o aplicativo deve compactar o fluxo no fluxo do grafo de filtro do gravador asf do wm e ignorar o mecanismo de compactação do gravador asf do wm chamando [**IConfigAsfWriter2:: setparam**](iconfigasfwriter2-setparam.md) da seguinte maneira:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



Em seguida, configure o filtro com o perfil desejado. É essencial que o tipo de mídia do fluxo de entrada corresponda exatamente ao formato no perfil. Em alguns casos, pode ser necessário examinar o formato do fluxo de entrada e criar um perfil personalizado para fazer a correspondência. Para obter mais informações, consulte [para criar arquivos ASF usando codecs de](to-create-asf-files-using-third-party-codecs.md)terceiros.

Ao conectar o gravador ASF do WM ao filtro upstream, use o método **IGraphBuilder:: ConnectDirect** . não use nenhum método "intelligent connect", como **IGraphBuilder:: Conexão** ou **IGraphBuilder:: renderfile** para conectar o filtro, pois isso desabilitará o modo "ignorar compactação" do filtro.

 

 




