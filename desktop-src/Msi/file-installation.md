---
description: 'Depois que o custo do arquivo for concluído, o instalador terá todas as informações necessárias para processar as duas ações de manipulação de arquivo: DuplicateFiles e MoveFile.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Instalação de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a987a7e61f646f58abd0ec699ce03bd29d85dfa2ddb01e8f693750acda740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636694"
---
# <a name="file-installation"></a>Instalação de arquivo

Depois que o [custo do arquivo](file-costing.md) for concluído, o instalador terá todas as informações necessárias para processar as duas ações de manipulação de arquivo: [DuplicateFiles](duplicatefiles-action.md) e [MoveFile](movefiles-action.md).

Use a [ação DuplicateFiles](duplicatefiles-action.md) para especificar os arquivos que o instalador deve duplicar na [tabela duplicatafile](duplicatefile-table.md). Use a [ação MoveFiles](movefiles-action.md)para determinar quais arquivos mover consultando a [tabela MoveFile](movefile-table.md).

Observe que o campo de opções da [tabela MoveFile](movefile-table.md) especifica se o arquivo original deve ser excluído ou não do local atual. Os arquivos movidos ou copiados pela ação MoveFiles não são excluídos quando o produto é desinstalado.

A [ação InstallFiles](installfiles-action.md) é chamada depois que todas as outras operações de manipulação de arquivo forem concluídas. A ação InstallFiles processa a [tabela de mídia](media-table.md), a [tabela de arquivos](file-table.md)e a tabela de [componentes](component-table.md) para determinar quais arquivos serão copiados da origem para o destino.

A [ação InstallFiles](installfiles-action.md) cria a estrutura de diretório necessária para instalar todos os arquivos. Se uma pasta vazia explicitamente for necessária para ser instalada, a [ação Createfolders](createfolders-action.md) poderá ser chamada para criá-la.

 

 



