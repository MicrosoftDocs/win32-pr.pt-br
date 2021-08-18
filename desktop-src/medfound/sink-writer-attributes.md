---
description: Atributos do Sink Writer
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Atributos do Sink Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bf64dd4279ef2e35ed86f50c4444412b3cc70205f6aad52adac8a41895af11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012362"
---
# <a name="sink-writer-attributes"></a>Atributos do Sink Writer

Os atributos a seguir podem ser usados para inicializar o sink writer.



| Atributo                                                                                  | Descrição                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ BAIXA \_ LATÊNCIA](mf-low-latency.md)                                                     | Habilita o processamento de baixa latência.                                                                                                                                                                                                    |
| [CONVERSORES DE DESABILITAÇÃO DE MF \_ READWRITE \_ \_](mf-readwrite-disable-converters.md)                  | Habilita ou desabilita conversões de formato pelo autor do sink.                                                                                                                                                                         |
| [MF \_ READWRITE \_ ENABLE \_ HARDWARE \_ TRANSFORMS](mf-readwrite-enable-hardware-transforms.md) | Permite que o autor do sink use MFTs (transformaçãos Media Foundation hardware).                                                                                                                                                  |
| [RETORNO DE CHAMADA \_ \_ \_ ASSÍNCRONO DO MF SINK \_ WRITER](mf-sink-writer-async-callback.md)                     | Contém um ponteiro para a interface de retorno de chamada do aplicativo para o autor do sink.                                                                                                                                                    |
| [MF \_ SINK \_ WRITER \_ DISABLE \_ THROTTLING](mf-sink-writer-disable-throttling.md)             | Especifica se o autor do sink limita a taxa de dados de entrada.                                                                                                                                                                |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                             | Especifica o tipo de contêiner do arquivo de saída.                                                                                                                                                                                   |
| [Atributo MFT \_ FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                  | Contém um [**ponteiro IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que é usado para desbloquear um MFT com restrições de campo de uso. Para obter mais informações, consulte [Restrições de campo de uso.](field-of-use-restrictions.md) |
| [MF \_ SINK \_ WRITER \_ D3D \_ MANAGER](mf-sink-writer-d3d-manager.md)                           | Use esse atributo para fornecer um dispositivo Direct3D para quaisquer codificadores de vídeo ou sinks de mídia carregados pelo autor do sink.                                                                                                                   |



 

Use estes atributos com os seguintes métodos e funções:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Para usar qualquer um desses atributos, primeiro chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo armazenamento de atributos. Em seguida, use a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para definir os atributos desejados no armazenamento de atributos. Passe o **ponteiro IMFAttributes** para o parâmetro *pAttributes* de qualquer um dos métodos ou funções listados anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



