---
description: OBJETO FUNCIONAL \_ TIPO \_ DE CONTEÚDO \_ \_ WPD
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58121d351219c246117106d578ed3672ebf25eecf9e159f957494b5c5eae9280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193520"
---
# <a name="wpd_content_type_functional_object"></a>OBJETO FUNCIONAL \_ TIPO \_ DE CONTEÚDO \_ \_ WPD

Um objeto que descreve seu tipo como WPD \_ CONTENT FUNCTIONAL OBJECT representa um objeto \_ \_ funcional, encapsulando a funcionalidade do dispositivo.

Todos os objetos funcionais, independentemente do tipo, são suportados com as propriedades a seguir. (Se você definir um objeto funcional personalizado, ele também deverá dar suporte a essas propriedades.)



| Nome da Propriedade                                                                                                         | Obrigatório ou Opcional                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.        |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                                             |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Obrigatórios.                                                                             |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.        |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                        | Obrigatórios.                                                                             |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                           | Obrigatórios.                                                                             |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                     |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema).                 |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                     |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                             |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                       | Recomendado se o objeto não for destinado ao consumo pelo dispositivo.                 |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto tiver referências a outros objetos.                               |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                                             |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                                             |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                           | Opcional.                                                                             |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                         | Recomendável.                                                                          |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                         | Opcional.                                                                             |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                            |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                             |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                                             |
| [O OBJETO WPD \_ \_ PODE \_ EXCLUIR](object-properties.md)                                                                     | Necessário se o objeto não puder ser excluído.                                             |
| [LOCALIDADE DA \_ LINGUAGEM \_ DE OBJETO \_ WPD](object-properties.md)                                                                | Opcional.                                                                             |
| [CATEGORIA DE OBJETO FUNCIONAL WPD \_ \_ \_](miscellaneous-properties.md)                      | Obrigatórios. Consulte a tabela a seguir para categorias definidas Windows Dispositivos Portáteis. |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

## <a name="functional-object-categories"></a>Categorias de objeto funcional

Objetos funcionais podem ser agrupados em categorias, dependendo de suas funções. Uma categoria é descrita pela propriedade WPD \_ FUNCTIONAL \_ OBJECT CATEGORY \_ (um valor GUID). A categoria determina quais propriedades adicionais têm suporte.

A tabela a seguir descreve as categorias definidas Windows Dispositivos Portáteis. Consulte a descrição da categoria para saber quais propriedades e recursos adicionais o objeto dá suporte.



| Categoria funcional                                                                                        | Descrição                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CATEGORIA FUNCIONAL WPD \_ \_ \_ ALL**](wpd-functional-category-all.md)                                      | Essa categoria funcional é válida apenas como um parâmetro para determinadas funções de consulta (para indicar que todos os tipos de objeto funcionais são aceitáveis) e não é uma categoria funcional relatada pelo driver. |
| [**CAPTURA DE ÁUDIO DA CATEGORIA FUNCIONAL WPD \_ \_ \_ \_**](wpd-functional-category-audio-capture.md)                 | O objeto encapsula a funcionalidade de captura de áudio no dispositivo, por exemplo, um gravador de voz ou outro componente de gravação de áudio.                                                                      |
| [**DISPOSITIVO DE CATEGORIA \_ FUNCIONAL \_ \_ WPD**](wpd-functional-category-device.md)                                | O objeto encapsula o dispositivo (ou seja, o objeto mais alto do dispositivo).                                                                                                                          |
| [**CONFIGURAÇÃO DE REDE \_ DA CATEGORIA FUNCIONAL WPD \_ \_ \_**](wpd-functional-category-network-configuration.md) | O objeto encapsula a funcionalidade de configuração de rede para o dispositivo, por exemplo, perfis de WiFi ou parcerias.                                                                                   |
| [**INFORMAÇÕES DE \_ RENDERIZAÇÃO DE CATEGORIA FUNCIONAL WPD \_ \_ \_**](wpd-functional-category-rendering-information.md) | O objeto descreve os tipos de arquivos de mídia que o dispositivo pode reproduzir.                                                                                                                            |
| [**SMS DA CATEGORIA FUNCIONAL WPD \_ \_ \_**](wpd-functional-category-sms.md)                                      | O objeto encapsula a funcionalidade de serviço de mensagem curta (normalmente chamada de "mensagens de texto") no dispositivo.                                                                                             |
| [**CAPTURA DE IMAGEM AINDA \_ \_ DA \_ CATEGORIA \_ FUNCIONAL WPD \_**](wpd-functional-category-still-image-capture.md)    | O objeto encapsula a funcionalidade de captura de imagem ainda em um dispositivo, como uma câmera ou anexo da câmera.                                                                                              |
| [**ARMAZENAMENTO DE CATEGORIA FUNCIONAL WPD \_ \_ \_**](wpd-functional-category-storage.md)                              | O objeto encapsula o armazenamento de arquivos físicos no dispositivo.                                                                                                                                              |
| [**CAPTURA DE VÍDEO DA \_ \_ CATEGORIA FUNCIONAL \_ WPD \_**](wpd-functional-category-video-capture.md)                 | O objeto encapsula a funcionalidade de captura de vídeo no dispositivo, por exemplo, um componente de gravador de vídeo. Um aplicativo usa esse objeto para obter controle programático.                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



