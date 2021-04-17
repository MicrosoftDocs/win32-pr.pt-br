---
description: '\_armazenamento de \_ categoria \_ funcional WPD'
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3000c63207286bc1dae153e3f930231909e92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769139"
---
# <a name="wpd_functional_category_storage"></a>\_armazenamento de \_ categoria \_ funcional WPD

Um \_ \_ objeto funcional de armazenamento de categoria funcional WPD \_ encapsula o armazenamento de arquivos físico no dispositivo.



| Nome da Propriedade                                                                                                         | Obrigatório ou opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ID de objeto WPD \_](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [\_ \_ ID pai do objeto WPD \_](object-properties.md)                                                 | Obrigatórios.                                                                                                                                              |
| [\_nome do objeto WPD \_](object-properties.md)                                                            | Obrigatórios.                                                                                                                                              |
| [\_ \_ \_ ID exclusiva persistente do objeto WPD \_](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obrigatórios.                                                                                                                                              |
| [\_tipo de \_ conteúdo de objeto WPD \_](object-properties.md)                                           | Obrigatórios.                                                                                                                                              |
| [objeto WPD- \_ \_ oculto](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                                                                      |
| [IsSystem de \_ objetos WPD \_](object-properties.md)                                                    | Obrigatório se o objeto for um objeto do sistema (representa um arquivo do sistema).                                                                                  |
| [\_tamanho do objeto WPD \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                                                                      |
| [\_nome de \_ \_ arquivo original do objeto \_ WPD](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                                                                              |
| [\_objeto WPD \_ não \_ consumível](object-properties.md)                                       | Recomendado se o objeto não for destinada ao consumo pelo dispositivo.                                                                                  |
| [\_referências de objetos WPD \_](object-properties.md)                                                | Obrigatório se o objeto tiver referências a outros objetos.                                                                                                |
| [\_ \_ palavras-chave do objeto WPD](object-properties.md)                                                    | Opcional.                                                                                                                                              |
| [\_ID de \_ sincronização do objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                                                              |
| [o \_ objeto \_ WPD \_ é \_ protegido por DRM](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                                                                 |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                           | Opcional.                                                                                                                                              |
| [\_data do objeto WPD \_ \_ modificado](object-properties.md)                                         | Recomendável.                                                                                                                                           |
| [\_data do objeto WPD \_ \_ criado](object-properties.md)                                         | Opcional.                                                                                                                                              |
| [\_referências de \_ retorno de objeto WPD \_](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                                                                             |
| [\_ID de \_ \_ objeto funcional \_ do contêiner de objetos WPD \_](object-properties.md)     | Opcional.                                                                                                                                              |
| [o \_ objeto WPD \_ gera \_ miniaturas \_ do \_ recurso](object-properties.md) | Opcional.                                                                                                                                              |
| [o \_ objeto WPD \_ pode \_ excluir](object-properties.md)                                                                     | Obrigatório se o objeto não puder ser excluído.                                                                                                              |
| [\_localidade do \_ idioma do objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [\_categoria de \_ objeto \_ funcional WPD](miscellaneous-properties.md)                      | Obrigatórios. Consulte [**\_ \_ \_ \_ objeto funcional de tipo de conteúdo WPD**](wpd-content-type-functional-object.md) para categorias definidas por dispositivos portáteis do Windows. |
| [\_tipo de armazenamento WPD \_](storage-properties.md)                                                         | Obrigatórios.                                                                                                                                              |
| [\_tipo de \_ sistema de arquivos de armazenamento WPD \_ \_](storage-properties.md)                               | Opcional.                                                                                                                                              |
| [\_capacidade de armazenamento WPD \_](storage-properties.md)                                                 | Obrigatórios.                                                                                                                                              |
| [\_ \_ espaço livre de armazenamento WPD \_ \_ em \_ bytes](storage-properties.md)                        | Opcional.                                                                                                                                              |
| [\_ \_ espaço livre de armazenamento WPD \_ \_ em \_ objetos](storage-properties.md)                    | Opcional.                                                                                                                                              |
| [\_Descrição do armazenamento WPD \_](storage-properties.md)                                           | Opcional.                                                                                                                                              |
| [\_número de \_ série de armazenamento WPD \_](storage-properties.md)                                      | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os seguintes recursos.



| Nome do Recurso                                    | Obrigatório ou opcional | Descrição                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**\_ícone de recurso WPD \_**](wpd-resource-icon.md) | Opcional.            | Contém a representação do ícone para esse armazenamento. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_ \_ objeto funcional de tipo de conteúdo WPD \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



