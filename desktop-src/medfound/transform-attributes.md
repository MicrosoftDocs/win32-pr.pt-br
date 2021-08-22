---
description: Transformar atributos
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Transformar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d5b7a5f4ff6174a48058c81fe1cdea382b18c058985da803efa4110eb12e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034554"
---
# <a name="transform-attributes"></a>Transformar atributos

Os atributos a seguir se aplicam [a Media Foundation transformação](media-foundation-transforms.md) (MFTs) ou a objetos de ativação para MFTs ou ambos. [](activation-objects.md)



| Atributo                                                                                                     | Descrição                                                                                                                                                                                   | Aplica-se A                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ ACTIVATE \_ MFT \_ LOCKED**](mf-activate-mft-locked-attribute.md)                                         | Especifica se o Carregador de Topologia alterará os tipos de mídia em um MFT.                                                                                                                  | MFTs                        |
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                                                       | Especifica se uma transformação Media Foundation (MFT) dá suporte à Aceleração de Vídeo directX.                                                                                                     | MFTs                        |
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                                                | Especifica se um MFT executa o processamento assíncrono.                                                                                                                                    | MFTs                        |
| [DESBLOQUEIO \_ \_ ASSÍNCRONO DE TRANSFORMAÇÃO MF \_](mf-transform-async-unlock.md)                                                 | Habilita o uso de um MFT assíncrono.                                                                                                                                                       | MFTs                        |
| [Atributo MF \_ TRANSFORM \_ CATEGORY \_](mf-transform-category-attribute.md)                                     | Especifica a categoria de um MFT.                                                                                                                                                            | Objetos de ativação MFT      |
| [Atributo MF \_ TRANSFORM \_ FLAGS \_](mf-transform-flags-attribute.md)                                           | Contém sinalizadores para um objeto de ativação MFT.                                                                                                                                                  | Objetos de ativação MFT      |
| [Atributo MFT \_ CODEC \_ GATES \_](mft-codec-merit-attribute.md)                                                 | Contém o valor de valor de um codec de hardware.                                                                                                                                                 | Objetos de ativação MFT      |
| [ATRIBUTO MFT \_ CONNECTED \_ \_ STREAM](mft-connected-stream-attribute.md)                                       | Contém um ponteiro para os atributos de fluxo do fluxo conectado em um MFT baseado em hardware.                                                                                                  | MFTs                        |
| [MFT \_ CONECTADO AO FLUXO \_ \_ \_ HW](mft-connected-to-hw-stream.md)                                              | Especifica se um MFT baseado em hardware está conectado a outro MFT baseado em hardware.                                                                                                            | MFTs                        |
| [O \_ DECODIFICADOR MFT \_ EXPÕE TIPOS DE SAÍDA EM ORDEM \_ \_ \_ \_ \_ NATIVA](mft-decoder-expose-output-types-in-native-order.md) | Especifica se um decodificador expõe tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.                                                                                   | MFTs                        |
| [DICA DE RESOLUÇÃO DE VÍDEO FINAL DO \_ DECODIFICADOR \_ \_ \_ \_ MFT](mft-decoder-final-video-resolution-hint.md)                   | Especifica a resolução de saída final da imagem decodificada, após o processamento de vídeo.                                                                                                           | MFTs                        |
| [O \_ CODIFICADOR MFT \_ DÁ SUPORTE A EVENTOS DE \_ \_ CONFIGURAÇÃO](mft-encoder-supports-config-event.md)                                | Especifica que o codificador MFT dá suporte ao recebimento [de eventos MEEncodingParameter](meencodingparameters.md) durante o streaming.                                                                     | MFTs                        |
| [LUID DO \_ ADAPTADOR MFT ENUM \_ \_](mft-enum-adapter-luid.md)                                                         | Especifica um identificador exclusivo para um adaptador de vídeo. Use esse atributo ao chamar MFTEnum2 para enumerar MFTs associados a um adaptador específico.                                             | MFTs                        |
| [Atributo de \_ URL de HARDWARE MFT ENUM \_ \_ \_](mft-enum-hardware-url-attribute.md)                                    | Contém o link simbólico para um MFT baseado em hardware.                                                                                                                                          | Objetos de ativação MFTs/MFT |
| [Atributo de ID DE FORNECEDOR DE \_ \_ HARDWARE \_ \_ MFT ENUM \_](mft-enum-hardware-vendor-id-attribute.md)                       | Especifica a ID do fornecedor para uma transformação baseada em Media Foundation hardware                                                                                                                       | MFTs                        |
| [ATRIBUTO SOMENTE TRANSCODE MFT \_ ENUM \_ \_ \_](mft-enum-transcode-only-attribute.md)                                | Especifica se um decodificador é otimizado para transcodificação em vez de para reprodução.                                                                                                            | MFTs                        |
| [Atributo MFT \_ FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                     | Contém um [**ponteiro IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que pode ser usado para desbloquear o MFT.                                                                            | Objetos de ativação MFT      |
| [Atributo MFT \_ FRIENDLY \_ \_ NAME](mft-friendly-name-attribute.md)                                             | Contém o nome de exibição de um MFT baseado em hardware.                                                                                                                                           | Objetos de ativação MFT      |
| [Atributos MFT \_ INPUT \_ TYPES \_](mft-input-types-attributes.md)                                               | Contém os tipos de entrada registrados para um MFT.                                                                                                                                               | Objetos de ativação MFT      |
| [Atributos MFT \_ OUTPUT \_ TYPES \_](mft-output-types-attributes.md)                                             | Contém os tipos de saída registrados para um MFT.                                                                                                                                              | Objetos de ativação MFT      |
| [PERFIL DO \_ CODIFICADOR PREFERENCIAL DO MFT \_ \_](mft-preferred-encoder-profile.md)                                         | Contém propriedades de configuração para um codificador.                                                                                                                                             | Objetos de ativação MFT      |
| [Atributo MFT \_ PREFERRED \_ OUTPUTTYPE \_](mft-preferred-outputtype-attribute.md)                               | Especifica o formato de saída preferencial para um codificador.                                                                                                                                         | Objetos de ativação MFT      |
| [Atributo MFT \_ PREFERRED \_ OUTPUTTYPE \_](mft-preferred-outputtype-attribute.md)                               | Especifica o formato de saída preferencial para um codificador.                                                                                                                                         | Objetos de ativação MFT      |
| [Atributo LOCAL do PROCESSO \_ \_ MFT \_](mft-process-local-attribute.md)                                             | Especifica se um MFT está registrado somente no processo do aplicativo.                                                                                                                     | Objetos de ativação MFT      |
| [MFT \_ REMUX \_ MARK \_ I \_ PICTURE \_ AS \_ CLEAN \_ POINT](mft-remux-mark-i-picture-as-clean-point.md)                 | Especifica se o MFT de remux de vídeo H.264 deve marcar imagens I como um ponto limpo para melhor capacidade de busca. Isso tem o potencial de corrupção em buscas em arquivos MP4 finais não compatíveis. | Objetos de ativação MFT      |
| [SUPORTE PARA MFT \_ \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | Especifica se uma transformação Media Foundation (MFT) dá suporte a vídeo estéreo 3D.                                                                                                          | Objetos de ativação MFT      |
| [**ALTERAÇÃO DE FORMATO \_ DINÂMICO DE SUPORTE \_ \_ DO \_ MFT**](mft-support-dynamic-format-change-attribute.md)                  | Especifica se uma transformação Media Foundation (MFT) dá suporte a alterações de formato dinâmico.                                                                                                         | MFTs                        |
| [Atributo \_ \_ CLSID MFT TRANSFORM \_](mft-transform-clsid-attribute.md)                                         | Contém o CLSID (identificador de classe) de um MFT.                                                                                                                                              | Objetos de ativação MFT      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> </dl>

 

 



