---
description: DISPOSITIVO DE CATEGORIA \_ FUNCIONAL \_ \_ WPD
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f39cf60e247c0abbbcc66f7fad52099a2a83a93f348b1ac9636bb790b9354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842212"
---
# <a name="wpd_functional_category_device"></a>DISPOSITIVO DE CATEGORIA \_ FUNCIONAL \_ \_ WPD

Um objeto funcional WPD \_ FUNCTIONAL CATEGORY DEVICE encapsula o dispositivo \_ \_ (ou seja, o objeto mais alto do dispositivo). Se um dispositivo implementar essa categoria funcional, ele deverá dar suporte a essas propriedades, além das propriedades listadas para o [objeto de dispositivo](device-object.md).



| Nome da Propriedade                                                                                                         | Obrigatório ou Opcional                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                      |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                                                                           |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Obrigatórios.                                                                                                           |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                      |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                        | Obrigatórios.                                                                                                           |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                           | Obrigatórios.                                                                                                           |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                                   |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema).                                               |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                                   |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                                           |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                       | Recomendado se o objeto não for destinado ao consumo pelo dispositivo.                                               |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto tiver referências a outros objetos.                                                             |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                                                                           |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                           |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                              |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                           | Opcional.                                                                                                           |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                         | Recomendável.                                                                                                        |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                         | Opcional.                                                                                                           |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                                          |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                           |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                                                                           |
| [CATEGORIA DE OBJETO FUNCIONAL WPD \_ \_ \_](miscellaneous-properties.md)                      | Obrigatórios.                                                                                                           |
| [PARCEIRO DE \_ SINCRONIZAÇÃO \_ DE DISPOSITIVO WPD \_](device-properties.md)                                           | Opcional.                                                                                                           |
| [VERSÃO DE FIRMWARE DO DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                   | Obrigatórios.                                                                                                           |
| [NÍVEL DE \_ ENERGIA DO \_ DISPOSITIVO WPD \_](device-properties.md)                                             | Recomendado se o dispositivo tiver uma bateria.                                                                                |
| [FONTE DE \_ ENERGIA DO \_ DISPOSITIVO WPD \_](device-properties.md)                                           | Recomendável.                                                                                                        |
| [WPD \_ DEVICE \_ PROTOCOL](device-properties.md)                                                    | Recomendável.                                                                                                        |
| [FABRICANTE DO \_ DISPOSITIVO \_ WPD](device-properties.md)                                            | Obrigatórios.                                                                                                           |
| [MODELO DE DISPOSITIVO WPD \_ \_](device-properties.md)                                                          | Obrigatórios.                                                                                                           |
| [NÚMERO DE \_ SÉRIE DO \_ DISPOSITIVO WPD \_](device-properties.md)                                         | Obrigatórios.                                                                                                           |
| [O DISPOSITIVO WPD \_ DÁ SUPORTE A NÃO \_ \_ \_ CONSUMÍVEIS](device-properties.md)                    | Necessário se o dispositivo dá suporte a objetos não consumíveis; ou seja, se o dispositivo puder ser usado para armazenamento de dados simples. |
| [WPD \_ DEVICE \_ DATETIME](device-properties.md)                                                    | Opcional.                                                                                                           |
| [NOME AMIGÁVEL \_ DO \_ DISPOSITIVO WPD \_](device-properties.md)                                         | Recomendável.                                                                                                        |
| [ESQUEMAS DE DRM COM SUPORTE DO DISPOSITIVO WPD \_ \_ \_ \_](device-properties.md)                        | Recomendado se o dispositivo dá suporte à tecnologia DRM.                                                                  |
| [OS FORMATOS COM SUPORTE DO DISPOSITIVO WPD \_ \_ SÃO \_ \_ \_ ORDENADOS](device-properties.md)       | Recomendado se o dispositivo dá suporte à ordenação de formato preferencial.                                                       |
| [TIPO DE DISPOSITIVO WPD \_ \_](device-properties.md)                                                            | Recomendável.                                                                                                        |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ TIPO \_ DE CONTEÚDO \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



