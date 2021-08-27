---
description: Um módulo de mesclagem pode ser aplicado a um arquivo .msi para adicionar diretórios à instalação, mas não pode substituir nem remover diretórios existentes.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Como autorar tabelas de diretório do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90768dff191b729d482f8ddd58a821a6ed440e79fcd1453ff412aaf7b8a76fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086266"
---
# <a name="authoring-merge-module-directory-tables"></a>Como autorar tabelas de diretório do módulo de mesclagem

Um módulo de mesclagem pode ser aplicado a um arquivo .msi para adicionar diretórios à instalação, mas não pode substituir nem remover diretórios existentes. A [tabela Diretório](directory-table.md) especifica o layout dos diretórios que o módulo de mesclagem fornece para a instalação de destino. Uma tabela De diretório é necessária em cada módulo de mesclagem.

Use as diretrizes a seguir ao autorizar a Tabela de Diretórios em um módulo de mesclagem. Para obter mais informações, consulte [Tabela de diretório](directory-table.md) e Usando a tabela de [diretório](using-the-directory-table.md).

-   A estrutura de diretório adicionada pelo módulo de mesclagem deve ter um único diretório raiz. A raiz deve ser nomeada TARGETDIR. O usuário pode alterar o valor de TARGETDIR durante a mesclagem para especificar onde anexar a estrutura de diretório do módulo à árvore de diretório do destino.
-   Mesclar tabelas de módulo diferentes da tabela Diretório não deve referenciar diretamente os locais de diretório para TARGETDIR. O local dessa referência será alterado se o valor de TARGETDIR for alterado pelo usuário.
-   As tabelas no módulo de mesclagem devem referenciar o local de um diretório filho de TARGETDIR ou outro diretório na árvore do módulo de mesclagem. Faça o seguinte para especificar TARGETDIR como o pai de um diretório no módulo de mesclagem. Insira o diretório na coluna Diretório e insira TARGETDIR na coluna Pai \_ do Diretório. Use a notação "." na coluna DefaultDir para indicar que esse diretório está localizado em TARGETDIR sem um subdiretório. Para obter mais informações, consulte [Usando a tabela de diretórios](using-the-directory-table.md).
-   Os nomes dos diretórios adicionados pelo módulo de mesclagem devem usar as convenções de nomeação descritas em Nomeando chaves primárias em [bancos de dados de módulo de mesclagem.](naming-primary-keys-in-merge-module-databases.md) Isso inclui diretórios predefinidos por propriedades como a propriedade [**SystemFolder**](systemfolder.md) e [**a propriedade ProgramFilesFolder.**](programfilesfolder.md)
-   Anexar um [*GUID*](g-gly.md) a cada entrada na tabela Directory (exceto TARGETDIR.) Isso inclui entradas de tabela de diretório que especificam Windows propriedades [**systemFolder**](systemfolder.md) do instalador, por exemplo, SystemFolder.000000000 \_ 0000 \_ \_ 0000 \_ 0000 0000000000000. A biblioteca Mergemod.dll adiciona ações personalizadas para definir a **propriedade SystemFolder.**
-   Quando um diretório predefinido é incluído em um módulo de mesclagem, a ferramenta de mesclagem adiciona automaticamente um Tipo de Ação Personalizada [51](custom-action-type-51.md) ao banco de dados de destino. O autor do módulo de mesclagem deve garantir que uma [tabela CustomAction](customaction-table.md) também seja incluída. A tabela CustomAction pode estar vazia, mas essa tabela deve existir no banco de dados de destino e garante que os diretórios predefinidos modificados sejam gravados nos locais corretos. Por exemplo, quando um diretório do sistema é incluído em um módulo de mesclagem, o autor do módulo de mesclagem deve garantir que exista uma tabela ação personalizada.

    Observe que o algoritmo correspondente para a geração desses tipos 51 ações personalizadas verifica apenas se o nome do diretório começa com uma das propriedades predefinidos [**do SystemFolder.**](systemfolder.md) Ele não verifica se o nome do diretório é exatamente igual à propriedade de diretório. Qualquer diretório que começa com um desses nomes de pasta padrão obtém uma ação personalizada do tipo 51, mesmo que o restante do nome não seja um GUID. Os autores precisam tomar cuidado para que isso não gere resultados falsos positivos e geração de ações personalizadas não intencionais em chaves primárias derivadas que começam com uma das **propriedades systemFolder.**

A seguir está um exemplo de uma tabela Directory em um módulo de mesclagem e os diretórios resolvidos esperados.



| Diretório                                              | Pai do \_ Diretório                                | Defaultdir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| Targetdir                                              |                                                  | SourceDir   |
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Targetdir                                        | .:MMM \_ Prog |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | Targetdir                                        | MMM \_ Sys    |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848 \_ 006097ABDE17 | MFC \_ OCX    |



 

Espera-se que um módulo de mesclagem com a tabela Diretório acima resulte na estrutura de diretório a seguir.



| Diretório                                              | Destino                                     | Fonte                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[Ponto de instalação do módulo de mesclagem\]\\         | \[Merge Module's Source Point \] \\ MMM \_ Prog           |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | \[SystemFolder\]\\                         | \[MMM Sys do ponto de \] \\ \_ origem do módulo de mesclagem            |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[MFC \] \\ OCX do ponto de instalação do módulo de \_ mesclagem | \[OCX do mmm \] \\ \_ prog MFC do ponto de origem do módulo de \\ \_ mesclagem |



 

 

 



