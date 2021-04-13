---
description: .
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: Sessão de mídia do PMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e14d9e403620d273bb4aeb3347cba523f304b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297884"
---
# <a name="pmp-media-session"></a>Sessão de mídia do PMP

Um aplicativo pode criar a [sessão de mídia](media-session.md) em um processo separado chamado de processo PMP ( [caminho de mídia protegido](protected-media-path.md) ). A principal finalidade do processo de PMP é habilitar a reprodução de conteúdo protegido usando o DRM (gerenciamento de direitos digitais). Por padrão, o processo de PMP é criado dentro de um ambiente protegido (PE). Somente os componentes confiáveis e assinados podem ser carregados dentro de um PE. Um benefício secundário do processo de PMP é que ele isola o processo do aplicativo do pipeline de mídia. Para obter mais informações sobre o processo de PMP, consulte [proteção de caminho de mídia](protected-media-path.md).

Para criar a sessão de mídia dentro do processo do PMP, chame a função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) . Opcionalmente, você pode passar o sinalizador **de \_ \_ processo desprotegido do MFPMPSESSION** . Se esse sinalizador for definido, o processo de PMP será criado dentro de um processo desprotegido e não como um processo PE. O processo desprotegido não pode ser usado para reprodução de DRM, mas oferece os benefícios do isolamento do processo.

A função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) retorna um ponteiro para um objeto proxy para a sessão de mídia. O aplicativo se comunica com a sessão de mídia por meio do proxy.

![uma ilustração da sessão de mídia dentro do processo de PMP](images/pmp01.png)

Por padrão, quando o aplicativo cria uma topologia, a origem da mídia é criada dentro do processo do aplicativo. Um proxy para a origem da mídia é criado dentro do processo do PMP. A origem da mídia pode criar objetos dentro do processo de PMP usando a interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) . Por exemplo, para dar suporte a DRM, uma origem de mídia cria um objeto chamado de ita ( *autoridade de confiança de entrada* ). O ITA deve ser criado dentro do processo de PMP. (Para obter mais informações sobre ITAs, consulte o [caminho de mídia protegido](protected-media-path.md).) Para usar a interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , faça o seguinte:

1.  A origem da mídia deve implementar a interface [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) .
2.  Durante a resolução da topologia, o proxy de sessão de mídia chama o método [**IMFPMPClient:: SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) na origem da mídia.
3.  A origem de mídia chama [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) para criar o objeto dentro do processo de PMP. O objeto deve ter um CLSID registrado. Além disso, para carregar dentro do PE, o objeto deve ser confiável e assinado digitalmente. Para obter informações sobre componentes de mídia protegidos por assinatura de código, consulte o white paper [assinatura de código para componentes de mídia protegidos no Windows Vista](/windows-hardware/test/hlk/)

A ilustração a seguir mostra a origem da mídia criada no processo do aplicativo.

![uma ilustração de uma origem de mídia no processo do aplicativo.](images/pmp02.png)

Outra alternativa é criar a origem da mídia dentro da sessão do PMP.

1.  Defina o [**atributo \_ \_ modo de \_ origem \_ remoto da sessão MF**](mf-session-remote-source-mode-attribute.md) ao criar a sessão de mídia. Os atributos de configuração são especificados no parâmetro *pConfiguration* da função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .
2.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) na sessão de mídia para obter um ponteiro para a interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) . O identificador de serviço é o **\_ \_ serviço MF PMP**.
3.  Chame [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) com o CLSID do identificador de classe **\_ MFSourceResolver** para criar o resolvedor de origem dentro do processo de PMP. O método retorna um ponteiro para um proxy para o resolvedor de origem.
4.  Chame [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) ou [**IMFSourceResolver:: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) para criar a origem da mídia.
    > [!Note]  
    > Nesse caso, você deve usar as versões assíncronas desses métodos, pois as versões síncronas não são remotas.

     

A ilustração a seguir mostra a origem da mídia criada no processo do PMP.

![uma ilustração de uma fonte de mídia no processo do PMP.](images/pmp03.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como reproduzir arquivos de mídia protegidos](how-to-play-protected-media-files.md)
</dt> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Caminho de mídia protegido](protected-media-path.md)
</dt> </dl>

 

 
