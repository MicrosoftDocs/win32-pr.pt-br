---
description: A ação InstallFiles copia os arquivos especificados na tabela Arquivo do diretório de origem para o diretório de destino.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Ação InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df2a62deb253314e84e72cd84e88052f1175db7451807c3f266542e29c10c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629927"
---
# <a name="installfiles-action"></a>Ação InstallFiles

A ação InstallFiles copia os arquivos especificados na tabela Arquivo do diretório de origem para o diretório de destino.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallFiles deve vir após a [ação InstallValidate](installvalidate-action.md) e antes de qualquer ação dependente de arquivo.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                      |
|-------|-------------------------------------------------|
| \[1\] | Identificador do arquivo instalado.                   |
| \[6\] | Tamanho do arquivo instalado em bytes.                |
| \[9\] | Identificador do diretório que mantém o arquivo instalado. |



 

## <a name="remarks"></a>Comentários

A ação InstallFiles opera em arquivos especificados na [tabela Arquivo](file-table.md). Cada arquivo é instalado com base no estado de instalação do componente associado do arquivo na [tabela Componente](component-table.md). Somente os arquivos cujos componentes são resolvidos para o **estado msiInstallStatelocal** são qualificados para cópia.

A ação InstallFiles implementa as seguintes colunas da tabela Arquivo.

-   A coluna FileName especifica o nome do arquivo de destino.
-   A coluna Versão especifica a versão do arquivo.
-   A coluna Atributos especifica os bits do sinalizador de atributo de instalação e arquivo.
-   A coluna Arquivo especifica o token de arquivo exclusivo.
-   A coluna FileSize especifica o tamanho do arquivo descompactado em bytes.
-   A coluna Idioma especifica o identificador de idioma do arquivo.
-   A coluna Sequência especifica o número de sequência na mídia.

A ação InstallFiles implementa as seguintes colunas da tabela Componente.

-   A coluna \_ Diretório especifica uma referência a um item de tabela [directory.](directory-table.md)
-   A coluna Componente especifica um nome exclusivo para o item de componente.

O arquivo especificado será copiado somente se uma das seguintes condições for verdadeira:

-   No momento, o arquivo não está instalado no computador local.
-   O arquivo está no computador local, mas tem um número de versão inferior ao arquivo na [tabela Arquivo](file-table.md).
-   O arquivo está no computador local, mas não há nenhum número de versão associado.

O diretório de origem para cada arquivo a ser copiado é determinado pelo sourceMode, que, por sua vez, depende do valor na coluna Gabinete da tabela Mídia. Para uma discussão completa sobre o modo de origem, consulte a [tabela Mídia](media-table.md).

Se o diretório de origem de um arquivo a ser copiado residir em mídia removível, como um disquete ou CD-ROM, a ação InstallFiles verificará se a mídia de origem apropriada é inserida antes de tentar copiar o arquivo. O InstallFiles pesquisa mídia do mesmo tipo removível com um rótulo de [*volume*](v-gly.md) que corresponde ao valor determinado na coluna VolumeLabel da tabela Mídia. Se um volume montado correspondente for encontrado, o processo de cópia de arquivo prosseguirá. Se nenhuma combinação for encontrada, uma caixa de diálogo solicitará que o usuário insira a mídia adequada. Nesse caso, a caixa de diálogo usa o nome de mídia encontrado na coluna DiskPrompt da tabela Mídia como parte do prompt.

Tenha cuidado, pois a ação InstallFiles pode excluir um arquivo original e não substituí-lo. Isso ocorre quando a ação InstallFiles experimenta um erro ao substituir um arquivo mais antigo e o usuário opta por ignorar o erro. O comportamento padrão do instalador é excluir um arquivo antigo antes de garantir que o novo arquivo seja copiado corretamente.

Para as regras de versão de arquivo usadas pelo instalador, consulte [Regras de versão de arquivo](file-versioning-rules.md).

 

 



