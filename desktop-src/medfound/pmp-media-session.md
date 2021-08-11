---
description: Sessão de mídia PMP
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: Sessão de mídia PMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683bc6d3dcc78bfb18daedabab614c95c33492fb7e17d48cbe7f6f08bdc766ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239191"
---
# <a name="pmp-media-session"></a>Sessão de mídia PMP

Um aplicativo pode criar a [Sessão de Mídia](media-session.md) em um processo separado chamado processo PMP (Caminho de Mídia Protegida). [](protected-media-path.md) A principal finalidade do processo PMP é habilitar a reprodução de conteúdo protegido usando DRM (gerenciamento de direitos digitais). Por padrão, o processo PMP é criado dentro de um PE (Ambiente Protegido). Somente componentes confiáveis assinados podem ser carregados dentro de um PE. Um benefício secundário do processo PMP é que ele isola o processo do aplicativo do pipeline de mídia. Para obter mais informações sobre o processo PMP, consulte [Caminho de mídia protegido.](protected-media-path.md)

Para criar a Sessão de Mídia dentro do processo PMP, chame a [**função MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) Opcionalmente, você pode passar o sinalizador **MFPMPSESSION \_ PROCESSO \_ DESPROTEGIDO.** Se esse sinalizador for definido, o processo PMP será criado dentro de um processo desprotegido e não em um processo PE. O processo desprotegido não pode ser usado para reprodução drm, mas lhe dá os benefícios do isolamento do processo.

A [**função MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) retorna um ponteiro para um objeto proxy para a Sessão de Mídia. O aplicativo se comunica com a Sessão de Mídia por meio do proxy.

![uma ilustração da sessão de mídia dentro do processo pmp](images/pmp01.png)

Por padrão, quando o aplicativo cria uma topologia, a fonte de mídia é criada dentro do processo do aplicativo. Um proxy para a fonte de mídia é criado dentro do processo PMP. A fonte de mídia pode criar objetos dentro do processo PMP usando a interface [**IMFPMPHost.**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) Por exemplo, para dar suporte ao DRM, uma fonte de mídia cria um objeto chamado ITA (autoridade de *confiança de entrada).* O ITA deve ser criado dentro do processo PMP. (Para obter mais informações sobre ITAs, consulte [Caminho de mídia protegido](protected-media-path.md).) Para usar a interface [**IMFPMPHost,**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) faça o seguinte:

1.  A fonte de mídia deve implementar a interface [**IMFPMPClient.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)
2.  Durante a resolução da topologia, o proxy da Sessão de Mídia chama o [**método IMFPMPClient::SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) na fonte de mídia.
3.  A fonte de mídia chama [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) para criar o objeto dentro do processo PMP. O objeto deve ter um CLSID registrado. Além disso, para carregar dentro do PE, o objeto deve ser confiável e assinado digitalmente. Para obter informações sobre componentes de mídia protegidos por assinatura de código, consulte o white paper assinatura de código para componentes de mídia [protegidos no Windows Vista](/windows-hardware/test/hlk/)

A ilustração a seguir mostra a fonte de mídia criada no processo do aplicativo.

![uma ilustração de uma fonte de mídia no processo do aplicativo.](images/pmp02.png)

Outra alternativa é criar a fonte de mídia dentro da sessão PMP.

1.  De definir o [**atributo MF \_ SESSION REMOTE \_ SOURCE \_ \_ MODE**](mf-session-remote-source-mode-attribute.md) ao criar a Sessão de Mídia. Os atributos de configuração são especificados *no parâmetro pConfiguration* da [**função MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)
2.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) na Sessão de Mídia para obter um ponteiro para a interface [**IMFPMPHost.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) O identificador de serviço é **MF \_ PMP \_ SERVICE.**
3.  Chame [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) com o identificador de classe **CLSID \_ MFSourceResolver** para criar o resolvedor de origem dentro do processo PMP. O método retorna um ponteiro para um proxy para o resolvedor de origem.
4.  Chame [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) ou [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) para criar a fonte de mídia.
    > [!Note]  
    > Nesse caso, você deve usar as versões assíncronas desses métodos, pois as versões síncronas não são remotamente remotamente.

     

A ilustração a seguir mostra a fonte de mídia criada no processo PMP.

![uma ilustração de uma fonte de mídia no processo pmp.](images/pmp03.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como reproduzir arquivos de mídia protegidos](how-to-play-protected-media-files.md)
</dt> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Caminho de mídia protegida](protected-media-path.md)
</dt> </dl>

 

 
