---
description: 'Depois que o custo do arquivo for concluído, o instalador terá todas as informações necessárias para processar as duas ações de manipulação de arquivo: DuplicateFiles e MoveFile.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Instalação de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091689"
---
# <a name="file-installation"></a>Instalação de arquivo

Depois que o [custo do arquivo](file-costing.md) for concluído, o instalador terá todas as informações necessárias para processar as duas ações de manipulação de arquivo: [DuplicateFiles](duplicatefiles-action.md) e [MoveFile](movefiles-action.md).

Use a [ação DuplicateFiles](duplicatefiles-action.md) para especificar os arquivos que o instalador deve duplicar na [tabela duplicatafile](duplicatefile-table.md). Use a [ação MoveFiles](movefiles-action.md)para determinar quais arquivos mover consultando a [tabela MoveFile](movefile-table.md).

Observe que o campo de opções da [tabela MoveFile](movefile-table.md) especifica se o arquivo original deve ser excluído ou não do local atual. Os arquivos movidos ou copiados pela ação MoveFiles não são excluídos quando o produto é desinstalado.

A [ação InstallFiles](installfiles-action.md) é chamada depois que todas as outras operações de manipulação de arquivo forem concluídas. A ação InstallFiles processa a [tabela de mídia](media-table.md), a [tabela de arquivos](file-table.md)e a tabela de [componentes](component-table.md) para determinar quais arquivos serão copiados da origem para o destino.

A [ação InstallFiles](installfiles-action.md) cria a estrutura de diretório necessária para instalar todos os arquivos. Se uma pasta vazia explicitamente for necessária para ser instalada, a [ação Createfolders](createfolders-action.md) poderá ser chamada para criá-la.

 

 



