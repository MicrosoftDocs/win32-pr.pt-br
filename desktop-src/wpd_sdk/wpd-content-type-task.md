---
description: TAREFA TIPO \_ DE \_ CONTEÚDO \_ WPD
ms.assetid: 503d0b11-2113-4df4-8b6b-250f24d09b1f
title: WPD_CONTENT_TYPE_TASK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d42761fa8cbd96b4ce5b4085544906d2333b9d1317181b397140468145a4b37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193530"
---
# <a name="wpd_content_type_task"></a>TAREFA TIPO \_ DE \_ CONTEÚDO \_ WPD

Um objeto que descreve seu tipo como WPD CONTENT TYPE TASK representa uma tarefa, como um \_ item em uma lista de tarefas a \_ \_ fazer.

Esse tipo de objeto dá suporte às propriedades a seguir.



| Nome da Propriedade       | Obrigatório ou Opcional         |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ID DO \_ \_ OBJETO WPD](object-properties.md)                                                                | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [ID PAI \_ \_ DO OBJETO \_ WPD](object-properties.md)                                                 | Obrigatórios.                                                                      |
| [NOME DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto representar um arquivo.                                      |
| [ID EXCLUSIVA \_ \_ PERSISTENTE DO OBJETO \_ \_ WPD](object-properties.md)                          | Obrigatório, somente leitura. Um cliente não pode definir essa propriedade, mesmo no momento da criação. |
| [FORMATO DE OBJETO WPD \_ \_](object-properties.md)                                                        | Obrigatórios.                                                                      |
| [TIPO DE CONTEÚDO \_ \_ DO OBJETO \_ WPD](object-properties.md)                                           | Obrigatórios.                                                                      |
| [\_ \_ ISHIDDEN DE OBJETO WPD](object-properties.md)                                                    | Necessário se o objeto estiver oculto.                                              |
| [ISSYSTEM \_ DO OBJETO WPD \_](object-properties.md)                                                    | Necessário se o objeto for um objeto do sistema (representa um arquivo do sistema).          |
| [TAMANHO DO OBJETO WPD \_ \_](object-properties.md)                                                            | Necessário se o objeto tiver pelo menos um recurso.                              |
| [NOME DO ARQUIVO \_ \_ ORIGINAL DO OBJETO \_ WPD \_](object-properties.md)                              | Necessário se o objeto representar um arquivo.                                      |
| [OBJETO WPD \_ \_ NÃO \_ CONSUMÍVEL](object-properties.md)                                       | Recomendado se o objeto não for destinado ao consumo pelo dispositivo.          |
| [REFERÊNCIAS DE OBJETO WPD \_ \_](object-properties.md)                                                | Necessário se o objeto tiver referências a outros objetos.                        |
| [PALAVRAS-CHAVE \_ DE OBJETO WPD \_](object-properties.md)                                                    | Opcional.                                                                      |
| [ID DE \_ SINCRONIZAÇÃO \_ DE OBJETO \_ WPD](object-properties.md)                                                     | Opcional.                                                                      |
| [O OBJETO WPD \_ \_ É PROTEGIDO \_ POR DRM \_](object-properties.md)                                  | Necessário se o objeto estiver protegido pela tecnologia DRM.                         |
| [DATA DO OBJETO WPD \_ \_ \_ CRIADO](object-properties.md)                                           | Opcional.                                                                      |
| [WPD \_ OBJECT \_ DATE \_ MODIFIED](object-properties.md)                                         | Recomendável.                                                                   |
| [WPD \_ OBJECT \_ DATE \_ AUTHORED](object-properties.md)                                         | Opcional.                                                                      |
| [REFERÊNCIAS DE \_ RETORNO DE \_ \_ OBJETO WPD](object-properties.md)                                                                | Recomendado se o objeto for referenciado por outro objeto.                     |
| [ID DE OBJETO FUNCIONAL DO CONTÊINER DE OBJETO \_ \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                      |
| [OBJETO WPD \_ \_ GERAR MINIATURA DO \_ \_ \_ RECURSO](object-properties.md) | Opcional.                                                                      |
| [O OBJETO WPD \_ \_ PODE \_ EXCLUIR](object-properties.md)                                                                     | Necessário se o objeto não puder ser excluído.                                      |
| [LOCALIDADE DA \_ LINGUAGEM \_ DE OBJETO \_ WPD](object-properties.md)                                                                | Opcional.                                                                      |
| [ASSUNTO DE \_ INFORMAÇÕES \_ COMUNS DO \_ WPD](object-properties.md)                                                            | Obrigatórios.                                                                      |
| [TEXTO DO \_ CORPO DE INFORMAÇÕES COMUNS \_ \_ WPD \_](object-properties.md)                                                         | Recomendável.                                                                   |
| [PRIORIDADE DE \_ INFORMAÇÕES \_ COMUNS WPD \_](object-properties.md)                                                           | Recomendável.                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ START \_ DATETIME](object-properties.md)                                                    | Recomendável.                                                                   |
| [WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME](object-properties.md)                                                      | Recomendável.                                                                   |
| [NOTAS DE \_ INFORMAÇÕES \_ COMUNS DO \_ WPD](object-properties.md)                                                              | Opcional.                                                                      |
| [STATUS DA TAREFA WPD \_ \_](task-properties.md)                                                              | Opcional.                                                                      |
| [PERCENTUAL DE \_ TAREFA WPD \_ \_ CONCLUÍDO](task-properties.md)                                         | Opcional.                                                                      |
| [DATA DO \_ LEMBRETE DA TAREFA \_ \_ WPD](task-properties.md)                                               | Opcional.                                                                      |
| [PROPRIETÁRIO DA \_ TAREFA \_ WPD](task-properties.md)                                                                | Opcional.                                                                      |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



