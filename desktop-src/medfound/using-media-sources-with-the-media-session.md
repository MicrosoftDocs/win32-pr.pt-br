---
description: Usando fontes de mídia com a sessão de mídia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Usando fontes de mídia com a sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930130"
---
# <a name="using-media-sources-with-the-media-session"></a>Usando fontes de mídia com a sessão de mídia

Se você estiver usando a sessão de mídia para controlar a reprodução, o conjunto de métodos que você deve chamar em uma fonte de mídia será restrito. Esta seção descreve como usar a origem de mídia em conjunto com a sessão de mídia.

Aqui estão as etapas básicas que seu aplicativo executará:

1.  Crie a origem da mídia. Para criar uma fonte de mídia, use o resolvedor de origem. Para obter mais informações, consulte [resolvedor de origem](source-resolver.md). O resolvedor de origem retorna um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte. (Se você tiver escrito uma fonte de mídia personalizada, poderá fornecer um método de criação personalizado em vez disso.)

2.  Configure a apresentação. Para configurar a apresentação da origem, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Você pode modificar essa cópia, mas as alterações não se tornam ativas até que a reprodução seja iniciada. Não modifique o descritor de apresentação durante a reprodução. Para obter mais informações, consulte [descritores de apresentação](presentation-descriptors.md).

3.  Crie uma topologia que contenha a origem da mídia. Para obter mais informações, consulte [topologias](topologies.md).

4.  Use a sessão de mídia para controlar a reprodução. A sessão de mídia chama métodos na origem da mídia. O aplicativo não deve chamar nenhum método na origem da mídia no momento.

5.  Antes de liberar a origem da mídia, chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para desligar a origem.

    > [!Note]  
    > Se você estiver usando a origem do sequenciador, a origem do sequenciador manipulará o desligamento das fontes de segmento. Para obter mais informações, consulte [origem do sequenciador](sequencer-source.md).

     

Se você usar a sessão de mídia, os únicos métodos que você deve chamar na origem da mídia são [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)e [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). Especialmente:

-   Não chame [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pausar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)ou [**parar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); Esses métodos devem ser chamados apenas pela sessão de mídia.

-   Não chame nenhum método [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .

-   Não recupere eventos diretamente da origem de mídia ou de qualquer um dos fluxos. A sessão de mídia deve receber esses eventos para que o pipeline funcione corretamente. A sessão de mídia encaminha todos os eventos que são necessários para o aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> </dl>

 

 



