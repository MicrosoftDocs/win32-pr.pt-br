---
description: Objeto de dispositivo
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Objeto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef76dbe26b1fd2c8d2bfd6da708728c9eb2177b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501608"
---
# <a name="device-object"></a>Objeto de dispositivo

O objeto de dispositivo dá suporte às propriedades a seguir. Um aplicativo pode solicitar essas propriedades consultando o objeto raiz (especificando a ID de objeto constante de **\_ ID de \_ objeto \_ do dispositivo WPD** definido). Todos os valores do objeto de dispositivo são somente leitura.

Se um determinado dispositivo implementar a categoria de [ \_ \_ \_ dispositivo de categoria funcional WPD](wpd-functional-category-device.md) , ele também deverá oferecer suporte às propriedades associadas a essa categoria.



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatórios. O valor é **\_ ID de \_ objeto \_ de dispositivo WPD**.                                                         |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios. O valor é uma cadeia de caracteres vazia.                                                                     |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                                                   |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatórios.                                                                                                   |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto de dispositivo não deve ser mostrado ao usuário.                                              |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Necessário se o objeto do dispositivo tiver referências a outros objetos.                                              |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                                                   |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                   |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                                                   |
| [\_parceiro de \_ sincronização de dispositivos WPD \_](device-properties.md)                                           | Opcional.                                                                                                   |
| [\_versão do \_ firmware do dispositivo WPD \_](device-properties.md)                                   | Obrigatórios.                                                                                                   |
| [\_nível de \_ energia do dispositivo WPD \_](device-properties.md)                                             | Recomendado se o dispositivo tiver uma bateria.                                                                    |
| [\_fonte de \_ energia do dispositivo WPD \_](device-properties.md)                                           | Recomendável.                                                                                                |
| [\_protocolo de dispositivo WPD \_](device-properties.md)                                                    | Recomendável.                                                                                                |
| [\_fabricante do dispositivo WPD \_](device-properties.md)                                            | Obrigatórios.                                                                                                   |
| [\_modelo de dispositivo WPD \_](device-properties.md)                                                          | Obrigatórios.                                                                                                   |
| [\_número de \_ série do dispositivo WPD \_](device-properties.md)                                         | Obrigatórios.                                                                                                   |
| [o \_ dispositivo WPD \_ dá suporte a \_ não \_ consumível](device-properties.md)                    | Necessário se o dispositivo oferecer suporte a objetos não consumíveis; ou seja, se ele puder ser usado para armazenamento de dados simples. |
| [data e hora do \_ dispositivo WPD \_](device-properties.md)                                                    | Opcional.                                                                                                   |
| [\_ \_ nome amigável do dispositivo WPD \_](device-properties.md)                                         | Recomendável.                                                                                                |
| [\_esquema de \_ DRM com suporte do dispositivo \_ WPD \_](device-properties.md)                          | Recomendado se o dispositivo der suporte a DRM (Rights Management digital).                                         |
| [os \_ \_ formatos com suporte do dispositivo WPD \_ \_ são \_ ordenados](device-properties.md)       | Recomendado se o dispositivo der suporte à ordenação de formato preferencial.                                               |
| [\_tipo de dispositivo WPD \_](device-properties.md)                                                            | Recomendável.                                                                                                |
| [\_ \_ \_ ID exclusiva funcional do dispositivo WPD \_](device-properties.md)                          | Opcional.                                                                                                   |
| [\_ \_ ID exclusiva do modelo de dispositivo WPD \_ \_](device-properties.md)                                    | Opcional.                                                                                                   |
| [\_transporte de dispositivo WPD \_](device-properties.md)                                                  | Recomendável.                                                                                                |
| [\_dispositivo WPD \_ usa \_ o \_ estágio do dispositivo](device-properties.md)                                  | Opcional.                                                                                                   |
| [\_categoria de \_ objeto \_ funcional WPD](device-properties.md)                             | Obrigatórios.                                                                                                   |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, esses objetos não hospedam recursos.

## <a name="commands"></a>Comandos

Além das propriedades, os dispositivos devem dar suporte a um conjunto específico de comandos definidos por dispositivos portáteis do Windows. Os comandos aos quais um objeto ou dispositivo dá suporte dependem de seu tipo, funcionalidade e recursos.

A tabela a seguir descreve as classes de comando que se aplicam a dispositivos, por funcionalidade. Normalmente, um dispositivo cai em várias categorias e deve dar suporte aos comandos para todas as categorias aplicáveis. Por exemplo, um telefone celular com uma câmera se enquadraria em três categorias: todos os dispositivos, dispositivos SMS e dispositivos de captura de imagem ainda. Um aplicativo cliente e um driver personalizado podem dar suporte a comandos ou propriedades adicionais que você definir, mas deve dar suporte aos comandos a seguir. Para obter uma descrição dos comandos específicos que se enquadram em cada categoria de comando, consulte [comandos](commands.md).



| Descrição                                                                                                                                                                                                                      | Categorias de comando                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Todos os dispositivos.                                                                                                                                                                                                                     | **categoria \_ WPD \_ CAPABILITIESWPD \_ categoria \_ comum**<br/> **\_enumeração de \_ objetos de categoria WPD \_**<br/> **\_Gerenciamento de \_ objetos de categoria WPD \_**<br/> **\_Propriedades do \_ objeto de categoria WPD \_**<br/> **\_massa de \_ Propriedades de objetos de categoria WPD \_ \_**<br/> **\_recursos de \_ objeto de categoria WPD \_**<br/> |
| Dispositivos que podem capturar imagens ainda, como câmeras digitais.                                                                                                                                                                  | **a \_ categoria \_ WPD \_ ainda \_ captura de imagem**                                                                                                                                                                                                                                                                                   |
| Dispositivos que podem enviar mensagens de SMS (serviço de mensagens curtas), como telefones celulares. O envio de mensagens SMS é geralmente chamado de "mensagens de texto".                                                                                      | **Categoria de WPD do \_ \_ SMS**                                                                                                                                                                                                                                                                                                     |
| Dispositivos que funcionam como dispositivos de armazenamento. Isso inclui unidades externas. Se um dispositivo oferecer suporte à capacidade de Formatar um repositório ou mover objetos de um local para outro, o driver deverá dar suporte a essa categoria.<br/> | **\_armazenamento de categoria WPD \_**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




