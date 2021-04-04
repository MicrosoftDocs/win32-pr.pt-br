---
description: Sobre a sessão de mídia
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Sobre a sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930086"
---
# <a name="about-the-media-session"></a>Sobre a sessão de mídia

A sessão de mídia expõe a interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . Há duas maneiras de criar a sessão de mídia, dependendo se seu aplicativo oferecerá suporte a conteúdo protegido:

-   Se seu aplicativo não oferecer suporte a conteúdo protegido, você poderá criar a sessão de mídia chamando o [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession). Essa função cria a sessão de mídia dentro do processo do aplicativo.
-   Para dar suporte ao conteúdo protegido, crie a sessão de mídia chamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Essa função cria a sessão de mídia dentro do processo do caminho de mídia protegido (PMP). O aplicativo recebe um ponteiro para um objeto proxy que realiza o marshaling de chamadas de método entre o limite do processo. Observe que a sessão de mídia do PMP pode ser usada para reproduzir conteúdo não criptografado, bem como conteúdo protegido.

Qualquer aplicativo que use a sessão de mídia seguirá estas etapas gerais:

1.  Crie uma topologia.
2.  Enfileirar a topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).
3.  Controle o fluxo de dados chamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
4.  Antes de o aplicativo sair, chame [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a sessão de mídia.
5.  Desligue todas as fontes de mídia criadas pelo aplicativo chamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
6.  Desligue a sessão de mídia chamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

Ao usar a sessão de mídia, o aplicativo não deve iniciar, pausar ou parar diretamente a origem da mídia. Todas as alterações de estado devem ser iniciadas chamando métodos [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . As alterações de estado na origem da mídia são manipuladas pela sessão de mídia.

Muitos outros detalhes dependerão da funcionalidade específica do seu aplicativo.

## <a name="protected-content"></a>Conteúdo protegido

Para reproduzir conteúdo protegido, você deve criar a sessão de mídia dentro do caminho de mídia protegido (PMP), chamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Essa função cria uma instância da sessão de mídia dentro da PMP e retorna um ponteiro para um objeto proxy que realiza o marshaling das interfaces entre o limite do processo.

Na maioria dos aspectos, o uso da sessão de mídia dentro do PMP é transparente para o aplicativo. No entanto, o aplicativo pode precisar invocar determinadas ações que permitem ao usuário reproduzir o conteúdo. Por exemplo, o usuário pode precisar obter uma licença de DRM. Media Foundation define um mecanismo genérico para essas ações usando a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .

Para mais informações, consulte os seguintes tópicos:

-   [Caminho de mídia protegido](protected-media-path.md)
-   [Como reproduzir arquivos de mídia protegidos](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Relógio de apresentação

A sessão de mídia gerencia todos os aspectos do relógio de apresentação:

-   Criando o relógio de apresentação.

-   Selecionando a fonte de tempo.

-   Notificando os coletores de mídia sobre o relógio

-   Iniciando, parando e pausando o relógio conforme necessário.

-   Desligando o relógio.

Para obter um ponteiro para o relógio de apresentação, chame [**IMFMediaSession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) na sessão de mídia. O relógio de apresentação não retorna um tempo válido até que a sessão de mídia envie o evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador MF TOPOSTATUS \_ Ready. Até lá, **getclock** retorna MF \_ E \_ Clock \_ sem \_ fonte de tempo \_ .

Um aplicativo que usa a sessão de mídia nunca deve iniciar, parar ou pausar o relógio de apresentação; alterar a taxa de clock; ou desligue o relógio.

Quando o aplicativo chama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), a sessão de mídia inicia o relógio de apresentação com uma hora de início igual à posição inicial especificada no método **Start** . Para obter mais informações sobre a sessão de mídia, consulte [sessão de mídia](media-session.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> </dl>

 

 



