---
description: CAPTURA DE IMAGEM AINDA \_ \_ DA \_ CATEGORIA \_ FUNCIONAL WPD \_
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fb0f6f19930780784083eaeddc1156bf55c99943aae8ad5850374c04211dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444806"
---
# <a name="wpd_functional_category_still_image_capture"></a>CAPTURA DE IMAGEM AINDA \_ \_ DA \_ CATEGORIA \_ FUNCIONAL WPD \_

Um objeto funcional WPD FUNCTIONAL CATEGORY STILL IMAGE CAPTURE encapsula a funcionalidade de captura de imagem ainda em um dispositivo, como uma câmera ou anexo \_ \_ da \_ \_ \_ câmera.



| Nome da Propriedade                                                                                                            | Obrigatório ou Opcional                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                   | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                    | Obrigatórios.                                                                                                                                              |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                               | Obrigatórios.                                                                                                                                              |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                             | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                           | Obrigatórios.                                                                                                                                              |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                              | Obrigatórios.                                                                                                                                              |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                       | Necessário se o objeto estiver oculto.                                                                                                                      |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                       | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema).                                                                                  |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                               | Necessário se o objeto tiver pelo menos um recurso.                                                                                                      |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                                 | Necessário se o objeto representar um arquivo.                                                                                                              |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                          | Recomendado se o objeto não for destinado ao consumo pelo dispositivo.                                                                                  |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                   | Necessário se o objeto tiver referências a outros objetos.                                                                                                |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                       | Opcional.                                                                                                                                              |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                        | Opcional.                                                                                                                                              |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                     | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                                                                 |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                              | Opcional.                                                                                                                                              |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                            | Recomendável.                                                                                                                                           |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                            | Opcional.                                                                                                                                              |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                   | Recomendado se o objeto for referenciado por outro objeto.                                                                                             |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)        | Opcional.                                                                                                                                              |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md)    | Opcional.                                                                                                                                              |
| [O OBJETO WPD \_ \_ PODE \_ EXCLUIR](object-properties.md)                                                                        | Necessário se o objeto não puder ser excluído.                                                                                                              |
| [LOCALIDADE DA \_ LINGUAGEM \_ DE OBJETO \_ WPD](object-properties.md)                                                                   | Opcional.                                                                                                                                              |
| [CATEGORIA DE OBJETO FUNCIONAL WPD \_ \_ \_](miscellaneous-properties.md)                         | Obrigatórios. Consulte [**OBJETO FUNCIONAL TIPO DE CONTEÚDO WPD \_ \_ \_ \_ para**](wpd-content-type-functional-object.md) categorias definidas Windows Dispositivos Portáteis. |
| [RESOLUÇÃO DE CAPTURA DE IMAGEM DO WPD \_ STILL \_ \_ \_](still-image-properties.md)                  | Obrigatórios.                                                                                                                                              |
| [FORMATO DE CAPTURA \_ DE \_ IMAGEM WPD STILL \_ \_](still-image-properties.md)                          | Obrigatórios.                                                                                                                                              |
| [CONFIGURAÇÃO DE \_ COMPACTAÇÃO \_ DE IMAGEM DO \_ WPD STILL \_](still-image-properties.md)                | Opcional.                                                                                                                                              |
| [BALANCEAR BRANCO DA IMAGEM DO WPD \_ STILL \_ \_ \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ RGB \_ GAIN](still-image-properties.md)                                      | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FNUMBER](still-image-properties.md)                                         | Opcional.                                                                                                                                              |
| [COMPRIMENTO FOCAL \_ DA IMAGEM DE WPD \_ \_ \_ STILL](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [DISTÂNCIA DE FOCO \_ DA IMAGEM DE WPD \_ \_ \_ STILL](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [MODO DE \_ FOCO DE IMAGEM AINDA \_ \_ WPD \_](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [MODO DE MEDIÇÃO DE \_ \_ EXPOSIÇÃO DE \_ IMAGEM \_ \_ DO WPD STILL](still-image-properties.md)         | Opcional.                                                                                                                                              |
| [MODO FLASH \_ DE \_ IMAGEM AINDA \_ \_ WPD](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [TEMPO DE EXPOSIÇÃO \_ DA IMAGEM DE WPD STILL \_ \_ \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [MODO DO PROGRAMA DE \_ \_ EXPOSIÇÃO DE \_ IMAGEM \_ \_ WPD STILL](still-image-properties.md)           | Opcional.                                                                                                                                              |
| [ÍNDICE DE EXPOSIÇÃO \_ DE IMAGEM DE WPD STILL \_ \_ \_](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [COMPENSAÇÃO DE \_ DESVIO DE EXPOSIÇÃO DE \_ \_ IMAGEM \_ DE WPD STILL \_](still-image-properties.md) | Opcional.                                                                                                                                              |
| [ATRASO NA CAPTURA DE IMAGEM DO WPD \_ STILL \_ \_ \_](still-image-properties.md)                            | Opcional.                                                                                                                                              |
| [MODO DE CAPTURA DE IMAGEM DO WPD \_ STILL \_ \_ \_](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [CONTRASTE DE IMAGEM \_ DE WPD \_ \_ STILL](still-image-properties.md)                                       | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ SHARPNESS](still-image-properties.md)                                     | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ DIGITAL \_ ZOOM](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [MODO DE EFEITO \_ DE \_ IMAGEM AINDA \_ \_ WPD](still-image-properties.md)                                | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ BURST \_ NUMBER](still-image-properties.md)                              | Opcional.                                                                                                                                              |
| [INTERVALO DE \_ ESTOURO DE IMAGEM DE WPD STILL \_ \_ \_](still-image-properties.md)                          | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ TIMELAPSE \_ NUMBER](still-image-properties.md)                      | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ TIMELAPSE \_ INTERVAL](still-image-properties.md)                  | Opcional.                                                                                                                                              |
| [MODO DE MEDIÇÃO DE \_ \_ FOCO DE \_ IMAGEM \_ \_ WPD STILL](still-image-properties.md)               | Opcional.                                                                                                                                              |
| [URL DE UPLOAD DE IMAGEM DO WPD \_ STILL \_ \_ \_](still-image-properties.md)                                  | Opcional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ ARTIST](still-image-properties.md)                                           | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

Muitas dessas propriedades têm efeitos interconectados. Por exemplo, se **WPD \_ STILL IMAGE EXPOSURE \_ \_ \_ METERING \_ MODE** for definido como automático, o f-stop, o tempo de exposição e o medidor de exposição serão vinculados; variar um deles fará com que os outros variem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ TIPO \_ DE CONTEÚDO \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



