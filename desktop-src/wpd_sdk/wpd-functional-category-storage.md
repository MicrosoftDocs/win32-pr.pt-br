---
description: ARMAZENAMENTO DE CATEGORIA FUNCIONAL WPD \_ \_ \_
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b16d70ebff4c61643b4d5ae0f8b333f5f9a7dc02103a32e14ded7a0ac4d8189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805932"
---
# <a name="wpd_functional_category_storage"></a>ARMAZENAMENTO DE CATEGORIA FUNCIONAL WPD \_ \_ \_

Um objeto funcional WPD \_ FUNCTIONAL CATEGORY STORAGE encapsula o armazenamento de arquivos físico no \_ \_ dispositivo.



| Nome da Propriedade                                                                                                         | Obrigatório ou Opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                                                                                                              |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Obrigatórios.                                                                                                                                              |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação.                                                                         |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                        | Obrigatórios.                                                                                                                                              |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                           | Obrigatórios.                                                                                                                                              |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                                                                                                      |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema).                                                                                  |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                                                                                                      |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                                                                                              |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                       | Recomendado se o objeto não for destinado ao consumo pelo dispositivo.                                                                                  |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto tiver referências a outros objetos.                                                                                                |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                                                                                                              |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                                                              |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                                                                                                 |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                           | Opcional.                                                                                                                                              |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                         | Recomendável.                                                                                                                                           |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                         | Opcional.                                                                                                                                              |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                                                                                             |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                                                              |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                                                                                                              |
| [O OBJETO WPD \_ \_ PODE \_ EXCLUIR](object-properties.md)                                                                     | Necessário se o objeto não puder ser excluído.                                                                                                              |
| [LOCALIDADE DA \_ LINGUAGEM \_ DE OBJETO \_ WPD](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [CATEGORIA DE OBJETO FUNCIONAL WPD \_ \_ \_](miscellaneous-properties.md)                      | Obrigatórios. Consulte [**OBJETO FUNCIONAL TIPO DE CONTEÚDO WPD \_ \_ \_ \_ para**](wpd-content-type-functional-object.md) categorias definidas Windows Dispositivos Portáteis. |
| [TIPO DE \_ ARMAZENAMENTO \_ WPD](storage-properties.md)                                                         | Obrigatórios.                                                                                                                                              |
| [TIPO DE SISTEMA DE \_ \_ ARQUIVOS DE ARMAZENAMENTO \_ WPD \_](storage-properties.md)                               | Opcional.                                                                                                                                              |
| [CAPACIDADE DE ARMAZENAMENTO WPD \_ \_](storage-properties.md)                                                 | Obrigatórios.                                                                                                                                              |
| [ESPAÇO LIVRE NO ARMAZENAMENTO WPD \_ \_ EM \_ \_ \_ BYTES](storage-properties.md)                        | Opcional.                                                                                                                                              |
| [ESPAÇO LIVRE NO ARMAZENAMENTO WPD \_ \_ EM \_ \_ \_ OBJETOS](storage-properties.md)                    | Opcional.                                                                                                                                              |
| [DESCRIÇÃO DO ARMAZENAMENTO WPD \_ \_](storage-properties.md)                                           | Opcional.                                                                                                                                              |
| [NÚMERO DE \_ SÉRIE DO \_ ARMAZENAMENTO WPD \_](storage-properties.md)                                      | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente incluem os recursos a seguir.



| Nome do Recurso                                    | Obrigatório ou Opcional | Descrição                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**ÍCONE DE \_ RECURSO \_ WPD**](wpd-resource-icon.md) | Opcional.            | Contém a representação de ícone para esse armazenamento. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ TIPO \_ DE CONTEÚDO \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



