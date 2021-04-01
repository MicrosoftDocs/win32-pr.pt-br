---
description: A ação RemoveDuplicateFiles exclui os arquivos instalados pela ação DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Ação RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647055"
---
# <a name="removeduplicatefiles-action"></a>Ação RemoveDuplicateFiles

A ação RemoveDuplicateFiles exclui os arquivos instalados pela ação [DuplicateFiles](duplicatefiles-action.md) .

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RemoveDuplicateFiles deve ocorrer após a ação [InstallValidate](installvalidate-action.md) e antes da ação [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador do arquivo removido.                   |
| \[9\] | Identificador do diretório que contém o arquivo removido. |



 

## <a name="remarks"></a>Comentários

Para excluir um arquivo duplicado com a [ação DuplicateFiles](duplicatefiles-action.md) usando a ação RemoveDuplicateFiles, o componente associado à entrada do arquivo na tabela duplicatafile deve ser selecionado para remoção.

Use a coluna DestFolder da [tabela duplicatefile](duplicatefile-table.md) para especificar o nome da propriedade cujo valor identifica a pasta de destino.

 

 



