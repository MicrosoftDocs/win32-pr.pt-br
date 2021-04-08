---
description: O tipo de dados formatado é uma cadeia de caracteres de texto que é processada para resolver nomes de propriedades incorporadas, chaves de tabela, referências de variáveis de ambiente e outras subcadeias de caracteres especiais.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formatado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd15dca46839b25dbf186d8a741b7a5c37c05f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922034"
---
# <a name="formatted"></a>Formatado

O tipo de dados formatado é uma cadeia de caracteres de texto que é processada para resolver nomes de propriedades incorporadas, chaves de tabela, referências de variáveis de ambiente e outras subcadeias de caracteres especiais. As seguintes convenções são reconhecidas para resolver a cadeia de caracteres:

-   Colchetes ( \[ \] ) ou chaves ({}) sem par correspondente são deixados no texto.
-   Se uma subcadeia de caracteres do formulário \[ *PropertyName* \] for encontrada, ela será substituída pelo valor da propriedade. Se *PropertyName* não for um nome de propriedade válido, a subcadeia de caracteres será resolvida como em branco. Por exemplo, a coluna Descrição da [tabela LaunchCondition](launchcondition-table.md) usa uma cadeia de caracteres formatada. Se ERRORTXT tiver sido definido como ", entre em contato com a equipe de suporte". em seguida, o texto exibido para falha na condição de inicialização incluiria essa cadeia de caracteres. Se ERRORTXT não estiver definido, o texto exibido para falha na condição de inicialização seria apenas "o sistema não atende aos requisitos de instalação".

    

    | Condição | Descrição                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9X | O sistema não atende aos requisitos de instalação. \[ERRORTXT\] |

    

     

-   Os colchetes podem ser iterados e os nomes de propriedade são resolvidos de dentro para fora. Por exemplo, suponha que a propriedade de subcadeia de caracteres \[ \[ \] \] seja exibida no texto. Primeiro, o valor da propriedade propertya é recuperado. Se o valor for um nome de propriedade válido, como PropertyB, o valor de PropertyB será recuperado e a propriedade de subcadeia de caracteres inteira \[ \[ \] \] será substituída pelo valor de PropertyB. Se Propertya não for um nome de propriedade válido, ou se o valor de Propertya não for um nome de propriedade válido, a subcadeia de caracteres ficará em branco.
-   Se uma subcadeia de caracteres do formulário \[ % *environmentvariable* \] for encontrada, o valor da variável de ambiente será substituído pela subcadeia de caracteres.
-   Se uma subcadeia de caracteres do formulário \[ \\ *x* \] for encontrada, ela será substituída pelo caractere *x* , em que *x* é um caractere, sem nenhum processamento adicional. Somente o primeiro caractere após a barra invertida é mantido; Tudo o mais é removido. Por exemplo, para incluir um colchete esquerdo literal ( \[ ), use \[ \\ \[ \] . O texto do colchete de texto é \[ \\ \[ \] \[ \\ \] \] resolvido para o \[ texto de colchete \] .
-   Se uma subcadeia de caracteres estiver entre chaves ({}) e não contiver nenhum nome de propriedade entre colchetes ( \[ \] ), a subcadeia de caracteres permanecerá inalterada, incluindo as chaves.
-   Se uma subcadeia de caracteres estiver entre chaves ({}) e contiver um ou mais nomes de propriedade entre colchetes (), \[ \] se todos os nomes de propriedade forem válidos, o texto (com as substituições resolvidas) será exibido sem as chaves.
-   Se uma subcadeia de caracteres do formulário \[ ~ \] for encontrada, ela será substituída pelo caractere nulo. Isso é usado para criar cadeias de caracteres **reg com \_ vários \_ sz** na [tabela de registro](registry-table.md). Observe que \[ ~ \] também é usado para acrescentar ou prefixar valores a variáveis de ambiente usando a [tabela de ambiente](environment-table.md).
-   Se uma subcadeia de caracteres do formulário \[ \# *FileKey* \] for encontrada, ela será substituída pelo caminho completo do arquivo, com o valor *FileKey* usado como uma chave na [tabela de arquivos](file-table.md). O valor de \[ \# *FileKey* \] permanece em branco e não é substituído por um caminho até que o instalador execute a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md). O valor de \[ \# *FileKey* \] depende do estado da instalação do componente ao qual o arquivo pertence. Se o componente for executado da origem, o valor será o caminho para o local de origem do arquivo. Se o componente for executado localmente, o valor será o caminho para o local de destino do arquivo após a instalação. Se o componente tiver um estado de ação ausente, o estado instalado do componente será usado para determinar o \[ \) .
-   Se uma subcadeia de caracteres do formulário \[ $ *componentkey* \] for encontrada, ela será substituída pelo diretório de instalação do componente, com o valor *componentkey* usado como uma chave na [tabela de componentes](component-table.md). O valor de \[ $ *componentkey* \] permanece em branco e não é substituído por um diretório até que o instalador execute a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md). O valor de \[ $ *componentkey* \] depende do estado da instalação do componente e de onde ele ocorre. Na coluna valor da tabela de [registro](registry-table.md), essa subcadeia de caracteres pode se referir ao estado de ação ou ao estado de ação solicitado do componente. Em todos os outros casos, essa subcadeia de caracteres se refere ao estado de ação do componente. Por exemplo, se o componente for executado da origem, o valor será o diretório de origem do arquivo. Se o componente for executado localmente, o valor será o diretório de destino após a instalação. Se o componente estiver ausente, o valor será deixado em branco. Windows Installer rastreia a ação e os Estados de instalação solicitados dos componentes. Por exemplo, se um componente já estiver instalado, ele poderá ter um estado solicitado de local e um estado de ação nulo. Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte [verificando a instalação de recursos, componentes e arquivos](checking-the-installation-of-features-components-files.md).
-   Observe que, se um componente já estiver instalado e não for reinstalado, removido ou movido durante a instalação atual, o estado de ação do componente será nulo e a cadeia de caracteres \[ $ *componentkey* \] avaliará como NULL.
-   Se for uma subcadeia de caracteres do formulário \[ !*FileKey* \] for encontrado, ele será substituído pelo caminho curto completo do arquivo, com o valor *FileKey* usado como uma chave na [tabela de arquivos](file-table.md).

    Essa sintaxe é válida somente quando usada na coluna Value do registro ou nas tabelas IniFile. Quando usado em outras colunas, essa sintaxe é tratada da mesma forma que \[ \# *FileKey* \] .

 

 



