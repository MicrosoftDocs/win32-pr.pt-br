---
description: Atributos do gravador de coletor
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Atributos do gravador de coletor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091031"
---
# <a name="sink-writer-attributes"></a>Atributos do gravador de coletor

Os atributos a seguir podem ser usados para inicializar o gravador do coletor.



| Atributo                                                                                  | Descrição                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_baixa \_ LATÊNCIA do MF](mf-low-latency.md)                                                     | Habilita o processamento de baixa latência.                                                                                                                                                                                                    |
| [\_conversores do MF ReadWrite \_ Disable \_](mf-readwrite-disable-converters.md)                  | Habilita ou desabilita conversões de formato pelo gravador de coletor.                                                                                                                                                                         |
| [MF \_ ReadWrite \_ habilitar \_ \_ transformações de hardware](mf-readwrite-enable-hardware-transforms.md) | Permite que o gravador de coletor use transformações de Media Foundation baseadas em hardware (MFTs).                                                                                                                                                  |
| [\_retorno de \_ \_ chamada assíncrono do gravador de coletor MF \_](mf-sink-writer-async-callback.md)                     | Contém um ponteiro para a interface de retorno de chamada do aplicativo para o gravador do coletor.                                                                                                                                                    |
| [\_limitação de \_ \_ desabilitação do gravador de coletor MF \_](mf-sink-writer-disable-throttling.md)             | Especifica se o gravador do coletor limita a taxa de dados de entrada.                                                                                                                                                                |
| [\_contêinertype de transcodificação MF \_](mf-transcode-containertype.md)                             | Especifica o tipo de contêiner do arquivo de saída.                                                                                                                                                                                   |
| [\_Atributo de \_ desbloqueio de FIELDOFUSE MFT \_](mft-fieldofuse-unlock-attribute.md)                  | Contém um ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que é usado para desbloquear um MFT com restrições de campo de uso. Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md). |
| [\_Gerenciador de \_ D3D do gravador de coletor MF \_ \_](mf-sink-writer-d3d-manager.md)                           | Use esse atributo para fornecer um dispositivo Direct3D para qualquer codificador de vídeo ou coletores de mídia carregados pelo gravador de coletor.                                                                                                                   |



 

Use esses atributos com os seguintes métodos e funções:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Para usar qualquer um desses atributos, primeiro chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos. Em seguida, use a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para definir os atributos desejados no repositório de atributos. Passe o ponteiro **IMFAttributes** para o parâmetro *pAttributes* de qualquer um dos métodos ou funções listados anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



