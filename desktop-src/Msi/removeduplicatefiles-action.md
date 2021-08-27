---
description: A ação RemoveDuplicateFiles exclui os arquivos instalados pela ação DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Ação RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7527e7bd4dc66fe4d57f8c23654f1138e781a33064fc0a4a2694987c7ccdb66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074616"
---
# <a name="removeduplicatefiles-action"></a>Ação RemoveDuplicateFiles

A ação RemoveDuplicateFiles exclui os arquivos instalados pela [ação DuplicateFiles.](duplicatefiles-action.md)

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RemoveDuplicateFiles deve ocorrer após a [ação InstallValidate](installvalidate-action.md) e antes da [ação InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador do arquivo removido.                   |
| \[9\] | Identificador do diretório que mantém o arquivo removido. |



 

## <a name="remarks"></a>Comentários

Para excluir um arquivo duplicado com a ação [DuplicateFiles](duplicatefiles-action.md) usando a ação RemoveDuplicateFiles, o componente associado à entrada do arquivo na tabela DuplicateFile deve ser selecionado para remoção.

Use a coluna DestFolder da tabela [DuplicateFile](duplicatefile-table.md) para especificar o nome da propriedade cujo valor identifica a pasta de destino.

 

 



