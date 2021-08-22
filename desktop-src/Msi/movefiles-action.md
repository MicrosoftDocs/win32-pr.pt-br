---
description: A ação MoveFiles localiza arquivos existentes no computador do usuário e move ou copia esses arquivos para um novo local.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Ação MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8581cd19569109c0f7697b5dfebf33e91b33da9ba84d15caf424242e4e21ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945031"
---
# <a name="movefiles-action"></a>Ação MoveFiles

A ação MoveFiles localiza arquivos existentes no computador do usuário e move ou copia esses arquivos para um novo local. A ação MoveFiles consulta a tabela [MoveFile](movefile-table.md) e move os arquivos especificados lá se o componente vinculado às entradas for especificado para ser instalado localmente ou estiver sendo executado da origem.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação MoveFiles deve vir após a [ação InstallValidate](installvalidate-action.md) e antes [da ação InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                  |
|-------|---------------------------------------------|
| \[1\] | Identificador do arquivo movido.                   |
| \[6\] | Tamanho do arquivo instalado em bytes.            |
| \[9\] | Identificador do diretório que mantém o arquivo movido. |



 

## <a name="remarks"></a>Comentários

A tabela MoveFiles contém uma coluna chamada "options" que especifica os arquivos de origem a serem movidos ou copiados. Um arquivo de origem movido é excluído depois que ele é copiado para um novo local. Para ver a sintaxe exata, consulte a [tabela MoveFile](movefile-table.md).

As colunas SourceFolder e DestFolder da tabela MoveFile são nomes de propriedade cujos valores devem ser resolvidos para caminhos totalmente qualificados. Essas propriedades podem ser qualquer uma [](directory-table.md) das entradas de diretório na tabela Diretório, qualquer propriedade de pasta predefinida ([**FavoritesFolder**](favoritesfolder.md), por exemplo) ou uma propriedade definida por qualquer entrada na tabela [AppSearch.](appsearch-table.md) Essas propriedades podem conter um caminho completo que contém o nome do arquivo para um arquivo específico. Por exemplo, a tabela AppSearch pode ser criado para pesquisar um arquivo específico e definir uma propriedade como o caminho completo para esse arquivo. Neste exemplo, a coluna SourceName na tabela MoveFile pode ser deixada em branco para indicar que o valor na propriedade SourceFolder contém um caminho de arquivo completo. O ponto e vírgula é olimidor de lista para transformar, fontes e patches e não deve ser usado em nomes de arquivo ou caminhos.

A ação MoveFiles não atua em entradas na tabela MoveFile na qual a propriedade SourceFolder ou DestFolder não é avaliada como um caminho completo.

A ação MoveFiles tenta mover ou copiar todos os arquivos no diretório de origem que corresponderem ao nome dado na coluna SourceName da tabela MoveFiles. O nome na coluna SourceName pode incluir \* o ou o ? curingas que permitem que um grupo de arquivos seja movido ou copiado. Por exemplo, a coluna SourceName pode conter uma entrada de ".xls" e a ação MoveFiles move ou copia cada pasta de trabalho Microsoft Excel do diretório de origem para o \* destino.

O nome a ser dado ao arquivo de destino pode ser especificado na coluna DestName da tabela MoveFile. O nome do arquivo de destino reterá o nome do arquivo de origem se essa coluna for deixada em branco.

Se um curinga " " for inserido na coluna SourceName da tabela MoveFile e um nome de arquivo de destino for especificado na coluna DestName, todos os arquivos movidos ou copiados manterão os nomes nas \* fontes. [](movefile-table.md)

Os arquivos que são movidos ou copiados pela ação MoveFiles não são excluídos quando o produto é desinstalado.

 

 



