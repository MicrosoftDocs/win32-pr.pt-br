---
description: A ação removidas remove os arquivos instalados anteriormente pela ação InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Ação de RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756892"
---
# <a name="removefiles-action"></a>Ação de RemoveFiles

A ação removidas remove os arquivos instalados anteriormente pela ação [InstallFiles](installfiles-action.md) . Cada um desses arquivos é restringido por um link para uma entrada na tabela de [componentes](component-table.md) . Somente os arquivos com componentes resolvidos para o estado *msiInstallStateAbsent* ou *msiInstallStateLocal* , se o componente for instalado localmente, serão removidos.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [InstallValidate](installvalidate-action.md) deve ser chamada antes de chamar RemoveFiles. Se uma ação [InstallFiles](installfiles-action.md) for usada, ela deverá aparecer após removes.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador do arquivo removido.                   |
| \[9\] | Identificador do diretório que contém o arquivo removido. |



 

## <a name="remarks"></a>Comentários

A tabela [RemoveFile](removefile-table.md) pode ser omitida do banco de dados do instalador se não houver arquivos diversos a serem removidos.

A ação removidas também pode remover arquivos especificados pelo autor que não estão instalados pela ação InstallFiles. Esses arquivos são especificados na tabela [RemoveFile](removefile-table.md) . Cada um desses arquivos é restringido por um link para uma entrada na tabela de [componentes](component-table.md) . Esses arquivos cujos componentes são resolvidos para qualquer estado de ação ativo (ou seja, não no estado desativado ou nulo) são removidos se o arquivo existir no diretório especificado. A remoção de arquivos especificados na tabela RemoveFile é tentada quando o componente vinculado é instalado pela primeira vez, durante uma reinstalação do e novamente quando o componente vinculado é removido.

A ação removidas também pode remover pastas. Uma pasta vazia será removida se o valor na coluna FileName da tabela RemoveFile for NULL.

Ao remover arquivos instalados anteriormente, a ação removidas consulta os mesmos campos nas mesmas tabelas que aqueles consultados pela ação [InstallFiles](installfiles-action.md) com a exceção de que a [tabela de mídia](media-table.md) não é usada pela ação removidas.

O nome do arquivo de destino pode ser especificado no texto localizado na coluna FileName da tabela RemoveFile.

 

 



