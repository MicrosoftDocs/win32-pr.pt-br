---
description: A ação InstallFiles copia os arquivos especificados na tabela de arquivos do diretório de origem para o diretório de destino.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Ação InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753444"
---
# <a name="installfiles-action"></a>Ação InstallFiles

A ação InstallFiles copia os arquivos especificados na tabela de arquivos do diretório de origem para o diretório de destino.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallFiles deve vir após a ação [InstallValidate](installvalidate-action.md) e antes de qualquer ação dependente de arquivo.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                      |
|-------|-------------------------------------------------|
| \[1\] | Identificador do arquivo instalado.                   |
| \[6\] | Tamanho do arquivo instalado em bytes.                |
| \[9\] | Identificador do diretório que contém o arquivo instalado. |



 

## <a name="remarks"></a>Comentários

A ação InstallFiles opera nos arquivos especificados na [tabela de arquivos](file-table.md). Cada arquivo é instalado com base no estado de instalação do componente associado do arquivo na [tabela de componentes](component-table.md). Somente os arquivos cujos componentes são resolvidos para o estado **msiInstallStatelocal** são elegíveis para cópia.

A ação InstallFiles implementa as colunas da tabela de arquivos a seguir.

-   A coluna FileName especifica o nome do arquivo de destino.
-   A coluna versão especifica a versão do arquivo.
-   A coluna atributos especifica os bits de sinalizador de atributo de arquivo e instalação.
-   A coluna arquivo especifica o token de arquivo exclusivo.
-   A coluna FileSize especifica o tamanho do arquivo descompactado em bytes.
-   A coluna idioma especifica o identificador de idioma do arquivo.
-   A coluna sequência especifica o número de sequência na mídia.

A ação InstallFiles implementa as colunas da tabela de componentes a seguir.

-   A \_ coluna Directory especifica uma referência a um item de [tabela de diretório](directory-table.md) .
-   A coluna componente especifica um nome exclusivo para o item de componente.

O arquivo especificado só será copiado se uma das seguintes opções for verdadeira:

-   O arquivo não está instalado no momento no computador local.
-   O arquivo está no computador local, mas tem um número de versão menor do que o arquivo na [tabela de arquivos](file-table.md).
-   O arquivo está no computador local, mas não há nenhum número de versão associado.

O diretório de origem para cada arquivo a ser copiado é determinado pelo sourcemode, que por sua vez depende do valor na coluna Cabinet da tabela de mídia. Para obter uma discussão completa sobre o modo de origem, consulte a [tabela de mídia](media-table.md).

Se o diretório de origem de um arquivo a ser copiado residir em mídia removível, como um disquete ou CD-ROM, a ação InstallFiles verificará se a mídia de origem adequada foi inserida antes de tentar copiar o arquivo. O InstallFiles pesquisa a mídia do mesmo tipo removível com um rótulo de [*volume*](v-gly.md) que corresponde ao valor fornecido na coluna VolumeLabel da tabela de mídia. Se um volume montado correspondente for encontrado, o processo de cópia de arquivo continuará. Se nenhuma correspondência for encontrada, uma caixa de diálogo solicitará que o usuário insira a mídia apropriada. Nesse caso, a caixa de diálogo usa o nome de mídia encontrado na coluna DiskPrompt da tabela de mídia como parte do prompt.

É preciso ter cuidado porque a ação InstallFiles pode excluir um arquivo original e não substituí-lo. Isso ocorre quando a ação InstallFiles passa por um erro ao substituir um arquivo mais antigo e o usuário escolhe ignorar o erro. O comportamento padrão do instalador é excluir um arquivo antigo antes de garantir que o novo arquivo seja copiado corretamente.

Para as regras de controle de versão de arquivo usadas pelo instalador, consulte [regras de controle de versão de arquivo](file-versioning-rules.md).

 

 



