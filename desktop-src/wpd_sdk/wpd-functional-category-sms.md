---
description: SMS DA CATEGORIA FUNCIONAL WPD \_ \_ \_
ms.assetid: dbb536a6-9c12-459d-8098-ebe4fc4c8f2f
title: WPD_FUNCTIONAL_CATEGORY_SMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273807900639f7c220bbb1828233bd717a8b814160167df3be87bda904d5a3e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838926"
---
# <a name="wpd_functional_category_sms"></a>SMS DA CATEGORIA FUNCIONAL WPD \_ \_ \_

Um objeto funcional WPD FUNCTIONAL CATEGORY SMS encapsula a funcionalidade de serviço de mensagem curta (normalmente chamada \_ \_ de \_ "mensagens de texto") no dispositivo.



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
| [PROVEDOR DE \_ SMS \_ WPD](sms-properties.md)                                                             | Obrigatórios.                                                                                                                                              |
| [WPD \_ SMS \_ TIMEOUT](sms-properties.md)                                                               | Obrigatórios.                                                                                                                                              |
| [PAYLOAD \_ MÁXIMO DE SMS WPD \_ \_](sms-properties.md)                                                      | Obrigatórios.                                                                                                                                              |
| [CODIFICAÇÃO DE \_ SMS \_ WPD](sms-properties.md)                                                             | Obrigatórios.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Esses objetos normalmente não hospedam recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ TIPO \_ DE CONTEÚDO \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



