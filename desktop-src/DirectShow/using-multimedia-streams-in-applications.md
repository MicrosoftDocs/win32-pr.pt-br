---
description: Usando Fluxos multimídia em aplicativos
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Usando Fluxos multimídia em aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faadcf755019291ae394d03aac5fb16aa632605b5e1c5bc2a8a457de55343757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525956"
---
# <a name="using-multimedia-streams-in-applications"></a>Usando Fluxos multimídia em aplicativos

> [!Note]  
> Essas APIs foram preterida. Os aplicativos devem usar [**o filtro Grabber de**](sample-grabber-filter.md) exemplo ou implementar um filtro personalizado para obter dados de um DirectShow de filtro.

 

As interfaces de streaming multimídia simplificam muito o processo de manipulação de dados multimídia removendo a dependência de características específicas da fonte de hardware ou software e fornecendo suporte para todos os formatos de mídia do Microsoft DirectX®. Fluxos abstrai os dados para um nível muito alto; os aplicativos podem até mesmo mover dados de um fluxo para outro sem saber nada sobre o formato dos dados.

Execute as etapas a seguir para criar um fluxo multimídia.

1.  Crie o fluxo multimídia. O método de criação e inicialização do fluxo é específico da arquitetura. DirectShow dá suporte à interface [**IAMMultiMediaStream,**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) que é usada para inicializar o fluxo. Outras implementações de servidor em processo do [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) serão criadas e inicializadas usando mecanismos diferentes.
2.  Depois que o objeto de fluxo multimídia for inicializado, o aplicativo usará **QueryInterface** para recuperar a interface **IMultiMediaStream** para o objeto. Use essa interface para determinar as propriedades do fluxo e enumerar os próprios fluxos. Você pode recuperar um fluxo específico chamando o [**método IMultiMediaStream::GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) com uma ID de finalidade específica. O MSPID \_ PrimaryVideo e o MSPID PrimaryAudio, que representam os fluxos de áudio e vídeo primários, são as IDs de finalidade mais \_ usadas.
3.  Chame **IUnknown::QueryInterface para** uma interface específica para o tipo de mídia do fluxo. Se você quiser renderizar um fluxo de vídeo, por exemplo, recupere sua interface [**IDirectDrawMediaStream.**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) Interfaces específicas de mídia definem métodos adicionais necessários para aproveitar ao máximo os recursos de um formato.
4.  Crie um ou mais exemplos dos dados de fluxo. Cada fluxo de mídia dá suporte [**ao método IMediaStream::CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) para criação de exemplo. O exemplo resultante dá suporte à interface [**IStreamSample,**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) que fornece controle sobre o exemplo e suas características. Normalmente, o fluxo de mídia dá suporte a um método específico de formato de criação de exemplo que é mais poderoso do que os métodos **IStreamSample** mencionados anteriormente. **IDirectDrawMediaStream,** por exemplo, pode criar amostras anexadas a uma superfície e retângulo de recorte do DirectDraw desejados. No entanto, em algumas situações, você deve lidar com os dados sem saber sobre o formato de dados. Se você quiser transmitir dados independentes de seu formato, use o método **IMediaStream::CreateSharedSample** para criar os exemplos de dados.
5.  Depois de criar todos os exemplos de fluxo desejados, inicie o fluxo chamando o método [**IMultiMediaStream::SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) e passe o sinalizador STREAMSTATE \_ RUN como seu parâmetro.
6.  Chame [**IStreamSample::Update para**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) atualizar o exemplo de fluxo. Quando o **método IStreamSample::Update** é final, você pode acessar os dados do exemplo. Se você quiser um gatilho de um evento ou uma chamada de função específica quando a atualização retornar, passe os ponteiros apropriados para o **método IStreamSample::Update.**

Para obter mais informações sobre as interfaces de streaming multimídia, consulte [Streaming multimídia](multimedia-streaming.md).

 

 



