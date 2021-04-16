---
description: A ação DuplicateFiles duplica os arquivos instalados pela ação InstallFiles. Os arquivos duplicados podem ser copiados para o mesmo diretório com um nome diferente ou para um diretório diferente com o nome original.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Ação DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750616"
---
# <a name="duplicatefiles-action"></a>Ação DuplicateFiles

A ação DuplicateFiles duplica os arquivos instalados pela ação [InstallFiles](installfiles-action.md) . Os arquivos duplicados podem ser copiados para o mesmo diretório com um nome diferente ou para um diretório diferente com o nome original.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação DuplicateFiles deve vir após a [ação InstallFiles](installfiles-action.md). A ação DuplicateFiles também deve vir após a [ação PatchFiles](patchfiles-action.md) para evitar a duplicação da versão sem patch do arquivo.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                       |
|-------|--------------------------------------------------|
| \[1\] | Identificador de arquivo duplicado.                   |
| \[6\] | Tamanho do arquivo duplicado.                         |
| \[9\] | Identificador do diretório que contém o arquivo duplicado. |



 

## <a name="remarks"></a>Comentários

A ação DuplicateFiles processa uma entrada de [tabela replicafile](duplicatefile-table.md) somente se o componente vinculado a essa entrada estiver sendo instalado localmente. Para obter mais informações, consulte [tabela de componentes](component-table.md).

A cadeia de caracteres no campo DestFolder é um nome de propriedade cujo valor deve ser resolvido para um caminho totalmente qualificado. Essa propriedade pode ser qualquer uma das entradas de diretório na tabela de [diretório](directory-table.md) , qualquer propriedade de pasta predefinida ([**CommonFilesFolder**](commonfilesfolder.md), por exemplo) ou uma propriedade definida por qualquer entrada na tabela [AppSearch](appsearch-table.md) . Se a propriedade **DestFolder** não for avaliada como um caminho válido, a ação DuplicateFiles não fará nada para essa entrada.

Se o nome do arquivo de destino na coluna Destname da tabela Duplicatafile for deixado em branco, o nome do arquivo de destino será o mesmo que o nome do arquivo original.

Os arquivos instalados pela ação DuplicateFiles são removidos pela ação [RemoveDuplicateFiles](removeduplicatefiles-action.md) quando apropriado.

 

 



