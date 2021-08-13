---
description: A ação DuplicateFiles duplica os arquivos instalados pela ação InstallFiles. Os arquivos duplicados podem ser copiados para o mesmo diretório com um nome diferente ou para um diretório diferente com o nome original.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Ação DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7969440aed4361ad264baa0d30a9c1d16f0ca673c72a2a7c3c1326e5d393ffc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637708"
---
# <a name="duplicatefiles-action"></a>Ação DuplicateFiles

A ação DuplicateFiles duplica os arquivos instalados pela [ação InstallFiles.](installfiles-action.md) Os arquivos duplicados podem ser copiados para o mesmo diretório com um nome diferente ou para um diretório diferente com o nome original.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação DuplicateFiles deve vir após a [ação InstallFiles](installfiles-action.md). A Ação DuplicateFiles também deve vir após a [ação PatchFiles](patchfiles-action.md) para impedir a duplicação da versão não corrigida do arquivo.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                       |
|-------|--------------------------------------------------|
| \[1\] | Identificador do arquivo duplicado.                   |
| \[6\] | Tamanho do arquivo duplicado.                         |
| \[9\] | Identificador do diretório que mantém o arquivo duplicado. |



 

## <a name="remarks"></a>Comentários

A ação DuplicateFiles processa uma entrada de tabela [DuplicateFile](duplicatefile-table.md) somente se o componente vinculado a essa entrada estiver sendo instalado localmente. Para obter mais informações, consulte [Tabela de componentes](component-table.md).

A cadeia de caracteres no campo DestFolder é um nome de propriedade cujo valor deve ser resolvido para um caminho totalmente qualificado. Essa propriedade pode ser qualquer uma das [](directory-table.md) entradas de diretório na tabela Directory, qualquer propriedade de pasta pré-definida ([**CommonFilesFolder**](commonfilesfolder.md), por exemplo) ou uma propriedade definida por qualquer entrada na tabela [AppSearch.](appsearch-table.md) Se a **propriedade DestFolder** não for avaliada como um caminho válido, a ação DuplicateFiles não faz nada para essa entrada.

Se o nome do arquivo de destino na coluna DestName da tabela DuplicateFile for deixado em branco, o nome do arquivo de destino será o mesmo que o nome do arquivo original.

Os arquivos instalados pela ação DuplicateFiles são removidos pela [ação RemoveDuplicateFiles](removeduplicatefiles-action.md) quando apropriado.

 

 



