---
description: Exemplo de EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Exemplo de EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089741"
---
# <a name="evrpresenter-sample"></a>Exemplo de EVRPresenter

Mostra como implementar um apresentador personalizado para o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR). O apresentador personalizado pode ser usado com o filtro EVR do DirectShow ou com o coletor de EVR Microsoft Media Foundation.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Media Foundation:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a>Uso

O exemplo EVRPresenter cria uma DLL que é um servidor COM para o apresentador. Antes de usar o apresentador personalizado, você deve registrar a DLL.

Para usar este exemplo no Media Foundation:

1.  Compile o exemplo.
2.  Regsvr32 EvrPresenter.dll.
3.  Compile e execute o [exemplo MFPlayer](/previous-versions//bb970516(v=vs.85)).
4.  No menu **arquivo** , selecione **abrir** arquivo.
5.  Na caixa de diálogo **Abrir arquivo** , selecione **apresentador personalizado do EVR.**
6.  Selecione um arquivo para reprodução.

Para usar este exemplo no DirectShow:

1.  Compile o exemplo.
2.  Registrar EvrPresenter.dll.
3.  Compile e execute o exemplo EVRPlayer. Este exemplo está incluído com os exemplos do DirectShow no SDK do Windows.
4.  No menu **arquivo** , selecione **apresentador de EVR**.
5.  Selecione um arquivo para reprodução.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> <dt>

[Como escrever um apresentador EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
