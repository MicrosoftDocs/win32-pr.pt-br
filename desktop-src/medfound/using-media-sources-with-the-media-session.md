---
description: Usando fontes de mídia com a sessão de mídia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Usando fontes de mídia com a sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ffec1b854829b5b8a0317d10adf121463e539dde471bc5b3063b1479037ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688720"
---
# <a name="using-media-sources-with-the-media-session"></a>Usando fontes de mídia com a sessão de mídia

Se você estiver usando a Sessão de Mídia para controlar a reprodução, o conjunto de métodos que você deve chamar em uma fonte de mídia será restrito. Esta seção descreve como usar a fonte de mídia em conjunto com a Sessão de Mídia.

Aqui estão as etapas básicas que seu aplicativo executará:

1.  Crie a fonte de mídia. Para criar uma fonte de mídia, use o resolvedor de origem. Para obter mais informações, consulte [Resolvedor de origem](source-resolver.md). O resolvedor de origem retorna um ponteiro para a interface [**IMFMediaSource da origem.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) (Se você tiver escrito uma fonte de mídia personalizada, poderá fornecer um método de criação personalizado.)

2.  Configure a apresentação. Para configurar a apresentação da origem, chame [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Você pode modificar essa cópia, mas as alterações não se tornam ativas até que a reprodução seja iniciada. Não modifique o descritor de apresentação durante a reprodução. Para obter mais informações, consulte [Descritores de apresentação](presentation-descriptors.md).

3.  Crie uma topologia que contenha a fonte de mídia. Para obter mais informações, consulte [Topologias](topologies.md).

4.  Use a Sessão de Mídia para controlar a reprodução. A Sessão de Mídia chama métodos na fonte de mídia. O aplicativo não deve chamar nenhum método na fonte de mídia no momento.

5.  Antes de liberar a fonte de mídia, chame [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para desligar a origem.

    > [!Note]  
    > Se você estiver usando a origem do sequenciador, a origem do sequenciador manipulará o desligamento das fontes de segmento. Para obter mais informações, consulte [Sequencer Source](sequencer-source.md).

     

Se você usar a Sessão de Mídia, os únicos métodos que você deve chamar na fonte de mídia serão [**CreatePresentationDescriptor,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)e [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). Especialmente:

-   Não chame [**Iniciar,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) [**Pausar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)ou [**Parar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); esses métodos devem ser chamados somente pela Sessão de Mídia.

-   Não chame nenhum [**método IMFMediaStream.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

-   Não recupere eventos diretamente da fonte de mídia ou de nenhum dos fluxos. A Sessão de Mídia deve receber esses eventos para que o pipeline funcione corretamente. A Sessão de Mídia encaminha todos os eventos que são necessários para o aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> </dl>

 

 



