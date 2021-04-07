---
description: Um módulo de mesclagem pode ser aplicado a um arquivo. msi para adicionar diretórios à instalação, mas não pode substituir ou remover diretórios existentes.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Criando tabelas de diretório do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98332f2c0bda10a5cc076f0ec80df3bf4b2e05aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828058"
---
# <a name="authoring-merge-module-directory-tables"></a>Criando tabelas de diretório do módulo de mesclagem

Um módulo de mesclagem pode ser aplicado a um arquivo. msi para adicionar diretórios à instalação, mas não pode substituir ou remover diretórios existentes. A [tabela de diretórios](directory-table.md) especifica o layout dos diretórios que o módulo de mesclagem fornece à instalação de destino. Uma tabela de diretório é necessária em cada módulo de mesclagem.

Use as diretrizes a seguir ao criar a tabela de diretório em um módulo de mesclagem. Para obter mais informações, consulte [tabela de diretórios](directory-table.md) e [usando a tabela de diretórios](using-the-directory-table.md).

-   A estrutura de diretório adicionada pelo módulo de mesclagem deve ter um único diretório raiz. A raiz deve ser nomeada TARGETDIR. O usuário pode alterar o valor de TARGETDIR durante a mesclagem para especificar onde anexar a estrutura de diretório do módulo na árvore de diretórios do destino.
-   Mesclar tabelas de módulo diferentes da tabela de diretório não deve fazer referência direta a locais de diretório para TARGETDIR. O local dessa referência será alterado se o valor de TARGETDIR for alterado pelo usuário.
-   As tabelas no módulo mesclar devem referenciar o local de um diretório filho de TARGETDIR ou outro diretório na árvore do módulo de mesclagem. Faça o seguinte para especificar TARGETDIR como o pai de um diretório no módulo de mesclagem. Insira o diretório na coluna diretório e digite TARGETDIR na \_ coluna pai do diretório. Use a notação "." na coluna DefaultDir para indicar que esse diretório está localizado em TARGETDIR sem um subdiretório. Para obter mais informações, consulte [usando a tabela de diretórios](using-the-directory-table.md).
-   Os nomes dos diretórios adicionados pelo módulo de mesclagem devem usar as convenções de nomenclatura descritas em [nomear chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md). Isso inclui diretórios predefinidos por propriedades como a propriedade [**SystemFolder**](systemfolder.md) e a propriedade [**ProgramFilesFolder**](programfilesfolder.md) .
-   Acrescente um [*GUID*](g-gly.md) a cada entrada na tabela de diretórios (exceto TARGETDIR.) Isso inclui entradas de tabela de diretório que especificam Windows Installer propriedades [**SystemFolder**](systemfolder.md) , por exemplo, SystemFolder. 00000000 0000 0000 0000 \_ \_ \_ \_ 000000000000. A biblioteca Mergemod.dll adiciona ações personalizadas para definir a propriedade **SystemFolder** .
-   Quando um diretório predefinido é incluído em um módulo de mesclagem, a ferramenta de mesclagem adiciona automaticamente um [tipo de ação personalizada 51](custom-action-type-51.md) ao banco de dados de destino. O autor do módulo de mesclagem deve garantir que uma [tabela CustomAction](customaction-table.md) também esteja incluída. A tabela CustomAction pode estar vazia, mas essa tabela deve existir no banco de dados de destino e garantir que os diretórios predefinidos modificados sejam gravados nos locais corretos. Por exemplo, quando um diretório do sistema é incluído em um módulo de mesclagem, o autor do módulo de mesclagem deve garantir que exista uma tabela de ação personalizada.

    Observe que o algoritmo de correspondência para a geração dessas ações personalizadas do tipo 51 verifica apenas se o nome do diretório começa com uma das propriedades predefinidas de [**SystemFolder**](systemfolder.md) . Ele não verifica se o nome do diretório é exatamente igual à propriedade do diretório. Qualquer diretório que comece com um desses nomes de pastas padrão Obtém uma ação personalizada de tipo 51, mesmo que o restante do nome não seja um GUID. Os autores precisam cuidar de que isso não gera correspondências falsos positivos e a geração de ação personalizada não intencional, em chaves primárias derivadas que começam com uma das propriedades **SystemFolder** .

Veja a seguir um exemplo de uma tabela de diretório em um módulo de mesclagem e os diretórios resolvidos esperados.



| Diretório                                              | Pai do diretório \_                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| TARGETDIR                                              |                                                  | SourceDir   |
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | TARGETDIR                                        | .: \_ PROG Mmm |
| SystemFolder. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | TARGETDIR                                        | \_Sys Mmm    |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848 \_ 006097ABDE17 | OCX do MFC \_    |



 

Espera-se que um módulo de mesclagem com a tabela de diretórios acima resulte na seguinte estrutura de diretório.



| Diretório                                              | Destino                                     | Fonte                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[Ponto de instalação do módulo de mesclagem\]\\         | \[O ponto de origem do módulo de mesclagem \] \\ Mmm \_ PROG           |
| SystemFolder. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | \[SystemFolder\]\\                         | \[\] \\ Sys Mmm do ponto de origem do módulo de mesclagem \_            |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[\] \\ Ocx do MFC do ponto de instalação do módulo de mesclagem \_ | \[MFC do ponto de origem do módulo de mesclagem/ \] \\ \_ \\ \_ ocx |



 

 

 



