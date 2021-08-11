---
description: Atributos do leitor de origem
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Atributos do leitor de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7bd9c5b3c5a71fb1b91515400fb0cf3670bd3b73b6635c811dcc79bd05e74f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238324"
---
# <a name="source-reader-attributes"></a>Atributos do leitor de origem

Os atributos a seguir podem ser usados para inicializar o [leitor de origem](source-reader.md).



| Atributo                                                                                                            | Descrição                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_baixa \_ LATÊNCIA do MF](mf-low-latency.md)                                                                               | Habilita o processamento de baixa latência.                                                                                                                                                                                                    |
| [\_conversores do MF ReadWrite \_ Disable \_](mf-readwrite-disable-converters.md)                                            | Habilita ou desabilita conversões de formato pelo leitor de origem.                                                                                                                                                                       |
| [MF \_ ReadWrite \_ habilitar \_ \_ transformações de hardware](mf-readwrite-enable-hardware-transforms.md)                           | Permite que o leitor de origem use transformações de Media Foundation baseadas em hardware (MFTs).                                                                                                                                                |
| [\_retorno de \_ \_ chamada assíncrono do leitor de origem MF \_](mf-source-reader-async-callback.md)                                           | Contém um ponteiro para a interface de retorno de chamada do aplicativo para o leitor de origem.                                                                                                                                                  |
| [\_Gerenciador de \_ D3D do leitor de origem MF \_ \_](mf-source-reader-d3d-manager.md)                                                 | Contém um ponteiro para o Gerenciador de Dispositivos do Microsoft [Direct3D](direct3d-device-manager.md).                                                                                                                                        |
| [\_leitor de origem MF \_ \_ desabilitar \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Especifica se o leitor de origem habilita a DXVA (aceleração de vídeo do DirectX) no decodificador de vídeo.                                                                                                                                |
| [o \_ \_ leitor de origem MF \_ desconecta o \_ MediaName \_ no \_ desligamento](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Especifica se o leitor de origem desliga a origem da mídia.<br/> Aplica-se somente quando o aplicativo cria o leitor de origem de um objeto de origem de mídia existente.<br/>                                           |
| [\_leitor de origem MF \_ \_ habilitar processamento de \_ \_ vídeo avançado \_](mf-source-reader-enable-advanced-video-processing.md)     | Habilita o processamento de vídeo avançado pelo [leitor de origem](source-reader.md), incluindo conversão de espaço de cor, desentrelaçamento, redimensionamento de vídeo e conversão de taxa de quadros.                                                           |
| [\_leitor de origem MF \_ \_ habilitar \_ processamento de vídeo \_](mf-source-reader-enable-video-processing.md)                        | Habilita o processamento de vídeo limitado pelo leitor de origem.                                                                                                                                                                             |
| [\_config. \_ media do leitor de origem MF \_ \_](mf-source-reader-mediasource-config.md)                                   | Contém propriedades de configuração para a origem da mídia.                                                                                                                                                                            |
| [\_Atributo de \_ desbloqueio de FIELDOFUSE MFT \_](mft-fieldofuse-unlock-attribute.md)                                            | Contém um ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que é usado para desbloquear um MFT com restrições de campo de uso. Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md). |



 

Use esses atributos com os seguintes métodos e funções:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Para usar qualquer um desses atributos, primeiro chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos. Em seguida, use a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para definir os atributos desejados no repositório de atributos. Passe o ponteiro **IMFAttributes** para o parâmetro *pAttributes* de qualquer um dos métodos ou funções listados anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




