---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Observação aos autores do GPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942bd1e8725428ee49bb937f3978622413160476
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105780071"
---
# <a name="note-to-gpd-authors"></a>Observação aos autores do GPD

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Para os autores de documentos de PrintCapabilities que estão familiarizados com os arquivos GPD, algumas palavras-chave GPD não têm equivalentes no documento PrintCapabilities. A tabela a seguir contém as palavras-chave GPD sem um equivalente do documento PrintCapabilities e o motivo pelo qual não há nenhum equivalente.



| Palavra-chave GPD                                                                            | Explicação                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Restrições<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | As restrições não são definidas no documento de PrintCapabilities porque os clientes de recursos de PrintCapabilities não devem processar, impor ou resolvê-las. Essas tarefas são deixadas para que o provedor PrintTicket seja executado durante a validação do PrintTicket. Plug-ins unidrv podem fornecer seu próprio código de validação de PrintTicket ou podem depender de unidrv para realizar essa validação. No último caso, o unidrv impõe quaisquer restrições definidas no arquivo GPD.<br/> Os drivers monolíticos devem fornecer seu próprio código de validação de PrintTicket e devem fornecer seu próprio método de expressar e impor restrições.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*Defaultoption<br/>                                                             | Há um método PrintTicket que retorna um PrintTicket padrão, que por definição tem todas as configurações padrão para cada recurso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*Recurso de funcionalidade<br/>                                                               | Um recurso pode ser dividido em três categorias diferentes:<br/> Um recurso cujas configurações são definidas em um PrintTicket. Esse tipo de recurso é chamado de documento-adesivo porque essas configurações determinam diretamente a maneira como um documento é processado.<br/> Um recurso cujas configurações refletem atributos de dispositivo físico que não são controlados pelo usuário, como a quantidade de memória no dispositivo ou que indicam a presença de Complementos opcionais, como alimentadores de papel ou duplexadors. Esse tipo de recurso é chamado de dispositivo adesivo ou de impressora. O estado desse tipo de recurso é importante porque ele pode restringir uma opção que pertence a um recurso de documento-adesivo.<br/> Um recurso adesivo de dispositivo ou de impressora pode ser categorizado ainda mais como um recurso adesivo de impressora (interface do usuário) ou um recurso auto-adesivo automático. Um recurso de impressora de interface de usuário deve ser exibido em uma interface do usuário que um administrador pode definir. O dispositivo detecta automaticamente um recurso automático de impressora.<br/> |
| \*Alternar... \* Casos<br/>                                                         | Um provedor de PrintCapabilities deve implementar um método que cria um documento de PrintCapabilities que enumera recursos de impressora ou de documento-adesivo, dependendo do tipo especificado pelo chamador. Por esse motivo, não há necessidade de apresentar as mesmas informações por meio do próprio documento de PrintCapabilities.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




