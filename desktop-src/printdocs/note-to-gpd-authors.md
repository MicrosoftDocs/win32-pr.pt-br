---
description: Revise as palavras-chave gpd sem equivalentes de documento PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Observação para autores de GPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fe9d0c4ce36cf603d492688f4faa426e3050b9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119811"
---
# <a name="note-to-gpd-authors"></a>Observação para autores de GPD

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Para os autores de documentos PrintCapabilities que estão familiarizados com arquivos GPD, algumas palavras-chave GPD não têm equivalentes no documento PrintCapabilities. A tabela a seguir contém as palavras-chave GPD sem um documento PrintCapabilities equivalente e o motivo pelo qual não há equivalente.



| Palavra-chave GPD                                                                            | Explicação                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Restrições<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | As restrições não são definidas no documento PrintCapabilities porque os clientes PrintCapabilities não devem processá-las, impor ou resolvê-las. Essas tarefas são deixadas para o provedor PrintTicket executar durante a validação de PrintTicket. Os plug-ins Unidrv podem fornecer seu próprio código de validação printTicket ou podem contar com Unidrv para realizar essa validação. No último caso, Unidrv impõe quaisquer restrições definidas no arquivo GPD.<br/> Drivers monolíticos devem fornecer seu próprio código de validação printTicket e devem fornecer seu próprio método de expressão e imposição de restrições.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*DefaultOption<br/>                                                             | Há um método PrintTicket que retorna um PrintTicket padrão, que, por definição, tem todas as configurações padrão para cada recurso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Um recurso pode ser dividido em três categorias diferentes:<br/> Um Recurso cujas configurações são definidas em um PrintTicket. Esse tipo de Recurso é chamado de document-sticky porque essas configurações determinam diretamente a maneira como um documento é processado.<br/> Um Recurso cujas configurações refletem atributos de dispositivo físico que não são controlados pelo usuário, como a quantidade de memória no dispositivo ou que indicam a presença de complementos opcionais, como feeds de papel ou duplexadores. Esse tipo de Recurso é chamado de sticky do dispositivo ou da impressora. O estado desse tipo de Recurso é importante porque ele pode restringir uma Opção que pertence a um recurso com sticky de documento.<br/> Um recurso de dispositivo autoaderido ou de impressora pode ser categorizado ainda mais como um recurso autoaderido por impressora (interface do usuário) ou como um recurso autoaderido por impressora. Um recurso de impressora de interface do usuário deve ser exibido em uma interface do usuário que um administrador pode definir. O dispositivo detecta automaticamente um Recurso autoadereado por impressora.<br/> |
| \*Alternar ... \* Caso<br/>                                                         | Um provedor PrintCapabilities deve implementar um método que cria um documento PrintCapabilities que enumera os Recursos de impressão autoescapta ou de documento, dependendo do tipo especificado pelo chamador. Por esse motivo, não é necessário apresentar as mesmas informações por meio do próprio documento PrintCapabilities.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




