---
description: Objeto device
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Objeto device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5279f63c7dabd8bd5b523d9234e33a60d9cf05608ac7b3f1b7601fd8c25024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083610"
---
# <a name="device-object"></a>Objeto device

O objeto de dispositivo dá suporte às propriedades a seguir. Um aplicativo pode solicitar essas propriedades consultando o objeto raiz (especificando a ID de objeto de constante **WPD \_ DEVICE OBJECT \_ \_ ID** definida). Todos os valores do objeto de dispositivo são somente leitura.

Se um determinado dispositivo implementar a [categoria DE DISPOSITIVO WPD FUNCTIONAL \_ \_ CATEGORY, \_ ](wpd-functional-category-device.md) ele também deverá dar suporte às propriedades associadas a essa categoria.



| Nome da Propriedade                                                                                                         | Obrigatório ou Opcional                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatórios. O valor é **WPD \_ DEVICE OBJECT \_ \_ ID**.                                                         |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios. O valor é uma cadeia de caracteres vazia.                                                                     |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                                                   |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatórios.                                                                                                   |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto de dispositivo não deve ser mostrado ao usuário.                                              |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto do dispositivo tiver referências a outros objetos.                                              |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                                                                   |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                   |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                                                                   |
| [PARCEIRO DE \_ SINCRONIZAÇÃO \_ DE DISPOSITIVO WPD \_](device-properties.md)                                           | Opcional.                                                                                                   |
| [VERSÃO DE FIRMWARE DO DISPOSITIVO WPD \_ \_ \_](device-properties.md)                                   | Obrigatórios.                                                                                                   |
| [NÍVEL DE \_ ENERGIA DO \_ DISPOSITIVO WPD \_](device-properties.md)                                             | Recomendado se o dispositivo tiver uma bateria.                                                                    |
| [FONTE DE \_ ENERGIA DO \_ DISPOSITIVO WPD \_](device-properties.md)                                           | Recomendável.                                                                                                |
| [WPD \_ DEVICE \_ PROTOCOL](device-properties.md)                                                    | Recomendável.                                                                                                |
| [FABRICANTE DO \_ DISPOSITIVO \_ WPD](device-properties.md)                                            | Obrigatórios.                                                                                                   |
| [MODELO DE DISPOSITIVO WPD \_ \_](device-properties.md)                                                          | Obrigatórios.                                                                                                   |
| [NÚMERO DE \_ SÉRIE DO \_ DISPOSITIVO WPD \_](device-properties.md)                                         | Obrigatórios.                                                                                                   |
| [O DISPOSITIVO WPD \_ DÁ SUPORTE A NÃO \_ \_ \_ CONSUMÍVEIS](device-properties.md)                    | Necessário se o dispositivo dá suporte a objetos não consumíveis; ou seja, se ele puder ser usado para armazenamento de dados simples. |
| [WPD \_ DEVICE \_ DATETIME](device-properties.md)                                                    | Opcional.                                                                                                   |
| [NOME AMIGÁVEL \_ DO \_ DISPOSITIVO WPD \_](device-properties.md)                                         | Recomendável.                                                                                                |
| [ESQUEMA DE DRM COM \_ \_ SUPORTE DO \_ DISPOSITIVO \_ WPD](device-properties.md)                          | Recomendado se o dispositivo dá suporte a DRM (Rights Management digital).                                         |
| [OS FORMATOS COM SUPORTE DO DISPOSITIVO WPD \_ \_ SÃO \_ \_ \_ ORDENADOS](device-properties.md)       | Recomendado se o dispositivo dá suporte à ordenação de formato preferencial.                                               |
| [TIPO DE DISPOSITIVO WPD \_ \_](device-properties.md)                                                            | Recomendável.                                                                                                |
| [ID EXCLUSIVA \_ \_ FUNCIONAL DO DISPOSITIVO \_ \_ WPD](device-properties.md)                          | Opcional.                                                                                                   |
| [ID EXCLUSIVA \_ DO MODELO DE DISPOSITIVO \_ \_ \_ WPD](device-properties.md)                                    | Opcional.                                                                                                   |
| [TRANSPORTE DE DISPOSITIVO WPD \_ \_](device-properties.md)                                                  | Recomendável.                                                                                                |
| [ESTÁGIO DE \_ USO DO \_ \_ DISPOSITIVO \_ WPD](device-properties.md)                                  | Opcional.                                                                                                   |
| [CATEGORIA DE OBJETO FUNCIONAL WPD \_ \_ \_](device-properties.md)                             | Obrigatórios.                                                                                                   |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

## <a name="commands"></a>Comandos

Além das propriedades, os dispositivos devem dar suporte a um conjunto específico de comandos definidos Windows Dispositivos Portáteis. Quais comandos um objeto ou dispositivo dá suporte depende de seu tipo, funcionalidade e funcionalidades.

A tabela a seguir descreve as classes de comando que se aplicam a dispositivos, por funcionalidade. Normalmente, um dispositivo se enquadra em várias categorias e deve dar suporte aos comandos para todas as categorias aplicáveis. Por exemplo, um telefone celular com uma câmera se enquadraria em três categorias: todos os dispositivos, dispositivos SMS e ainda dispositivos de captura de imagem. Um driver personalizado e um aplicativo cliente podem dar suporte a comandos ou propriedades adicionais que você define, mas deve dar suporte aos comandos a seguir. Para ver uma descrição dos comandos específicos que se enquadram em cada categoria de comando, consulte [Comandos](commands.md).



| Descrição                                                                                                                                                                                                                      | Categorias de comando                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Todos os dispositivos.                                                                                                                                                                                                                     | **FUNCIONALIDADES DE \_ \_ CATEGORIA WPDWPD \_ CATEGORIA \_ COMUM**<br/> **ENUMERAÇÃO DE \_ OBJETO DE \_ CATEGORIA WPD \_**<br/> **GERENCIAMENTO DE OBJETOS DE CATEGORIA WPD \_ \_ \_**<br/> **PROPRIEDADES DO \_ OBJETO DE \_ CATEGORIA WPD \_**<br/> **PROPRIEDADES DE OBJETO DE CATEGORIA WPD \_ \_ EM \_ \_ MASSA**<br/> **RECURSOS DE OBJETO \_ DE \_ CATEGORIA \_ WPD**<br/> |
| Dispositivos que podem capturar imagens ainda, como câmeras digitais.                                                                                                                                                                  | **CAPTURA DE IMAGEM \_ AINDA \_ DA CATEGORIA \_ \_ WPD**                                                                                                                                                                                                                                                                                   |
| Dispositivos que podem enviar mensagens sms (serviço de mensagem curta), como telefones celulares. O envio de mensagens SMS geralmente é chamado de "mensagens de texto".                                                                                      | **WPD \_ CATEGORY \_ SMS**                                                                                                                                                                                                                                                                                                     |
| Dispositivos que funcionam como dispositivos de armazenamento. Isso inclui unidades externas. Se um dispositivo dá suporte à capacidade de formatar um armazenamento ou mover objetos de um local para outro, o driver deverá dar suporte a essa categoria.<br/> | **ARMAZENAMENTO DE \_ CATEGORIA \_ WPD**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 




