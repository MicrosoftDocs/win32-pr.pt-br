---
description: O tipo de dados Formatado é uma cadeia de caracteres de texto processada para resolver nomes de propriedade inseridos, chaves de tabela, referências de variável de ambiente e outras substrings especiais.
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: Formatado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58cd21a53a3f77a646d6da0fac04480bd709ab8f1d7ddcb918d5362a0a366c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649636"
---
# <a name="formatted"></a>Formatado

O tipo de dados Formatado é uma cadeia de caracteres de texto processada para resolver nomes de propriedade inseridos, chaves de tabela, referências de variável de ambiente e outras substrings especiais. As convenções a seguir são reconhecidas para resolver a cadeia de caracteres:

-   Colchetes ( ) ou chaves ({ }) sem par \[ \] correspondente são deixados no texto.
-   Se uma substring do nome da propriedade do formulário for encontrada, ela será substituída \[  \] pelo valor da propriedade . Se *propertyname* não for um nome de propriedade válido, a substring será resolvida como em branco. Por exemplo, a coluna Descrição da [Tabela LaunchCondition](launchcondition-table.md) recebe uma cadeia de caracteres formatada. Se ERRORTXT tiver sido definido como "Entre em contato com sua equipe de suporte". em seguida, o texto exibido para falha na condição de lançamento incluiria essa cadeia de caracteres. Se ERRORTXT não estiver definido, o texto exibido para falhar na condição de lançamento será apenas "O sistema não atenderá aos requisitos de instalação".

    

    | Condição | Descrição                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9X | O sistema não atendem aos requisitos de instalação. \[ERRORTXT\] |

    

     

-   Os colchetes podem ser iterados e os nomes de propriedade são resolvidos de dentro para fora. Por exemplo, suponha que a substring \[ \[ PropertyA \] \] apareça no texto. Primeiro, o valor da propriedade PropertyA é recuperado. Se o valor for um nome de propriedade válido, como PropertyB, o valor de PropertyB será recuperado e toda a substring PropertyA será substituída pelo valor \[ \[ \] \] de PropertyB. Se PropertyA não for um nome de propriedade válido ou se o valor de PropertyA não for um nome de propriedade válido, a substring será em branco.
-   Se uma substring do formato environmentvariable for encontrada, o valor da variável de ambiente será substituído \[ %  \] pela substring.
-   Se uma substring do formato x for encontrada, ela será substituída pelo caractere x , em que x é um caractere, sem \[ \\  \] nenhum processamento posterior.   Somente o primeiro caractere após a faixa invertida é mantido; todo o resto é removido. Por exemplo, para incluir um colchete esquerdo literal ( \[ ), use \[ \\ \[ \] . O texto \[ \\ \[ \] Texto entre \[ \\ \] \] Colchetes é resolvido para \[ Texto entre Colchetes. \]
-   Se uma substring estiver entre chaves ({ }) e não contiver nomes de propriedade entre colchetes ( ), a substring será deixada inalterada, incluindo as \[ \] chaves.
-   Se uma substring estiver entre chaves ({ }) e contiver um ou mais nomes de propriedade entre colchetes ( ) , se todos os nomes de propriedade são válidos, o texto (com as substituições resolvidas) será exibido sem as \[ \] chaves.
-   Se uma substring do formulário \[ ~ \] for encontrada, ela será substituída pelo caractere nulo. Isso é usado para autor de cadeias de caracteres **REG \_ MULTI \_ SZ** na [tabela registro](registry-table.md). Observe que também \[ ~ \] é usado para anexar ou prefixar valores a variáveis de ambiente usando [a tabela Ambiente](environment-table.md).
-   Se uma substring da chave de arquivo de formulário for encontrada, ela será substituída pelo caminho completo do arquivo, pela chave de arquivo de valor usada como uma chave na \[ \#  \] [tabela Arquivo](file-table.md).  O valor de filekey permanece em branco e não é substituído por um caminho até que o instalador executa a ação \[ \#  \] [CostInitialize](costinitialize-action.md), a ação [FileCost](filecost-action.md)e a [ação CostFinalize](costfinalize-action.md). O valor de \[ \# *filekey* \] depende do estado de instalação do componente ao qual o arquivo pertence. Se o componente for executado da origem, o valor será o caminho para o local de origem do arquivo. Se o componente for executado localmente, o valor será o caminho para o local de destino do arquivo após a instalação. Se o componente tiver um estado de ação ausente, o estado instalado do componente será usado para determinar o \[ \) .
-   Se uma substring do formulário componentkey for encontrada, ela será substituída pelo diretório de instalação do componente, pela chave de componente de valor usada como uma chave na \[ $  \] [tabela Component](component-table.md).  O valor de componentkey permanece em branco e não é substituído por um diretório até que o instalador executa a ação \[ $  \] [CostInitialize](costinitialize-action.md), a ação [FileCost](filecost-action.md)e a [ação CostFinalize](costfinalize-action.md). O valor de \[ $ *componentkey* \] depende do estado de instalação do componente e de onde ele ocorre. Na coluna Valor da Tabela [do](registry-table.md)Registro , essa substring pode se referir ao estado da ação ou ao estado de ação solicitado do componente. Em todos os outros casos, essa substring refere-se ao estado de ação do componente. Por exemplo, se o componente for executado da origem, o valor será o diretório de origem do arquivo. Se o componente for executado localmente, o valor será o diretório de destino após a instalação. Se o componente estiver ausente, o valor será deixado em branco. Windows O instalador rastreia a ação e os estados de instalação solicitados dos componentes. Por exemplo, se um componente já estiver instalado, ele poderá ter um estado solicitado de local e um estado de ação nulo. Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte Verificando a [instalação de recursos, componentes, arquivos](checking-the-installation-of-features-components-files.md).
-   Observe que, se um componente já estiver instalado e não for reinstalado, removido ou movido durante a instalação atual, o estado de ação do componente será nulo e a chave de componente de cadeia de caracteres será avaliada como \[ $  \] Null.
-   Se uma substring do formulário \[ !*filekey* é encontrada, ela é substituída pelo caminho curto completo do arquivo, pela chave de arquivo de valor usada como uma chave na \] [tabela Arquivo](file-table.md). 

    Essa sintaxe é válida somente quando usada na coluna Valor do Registro ou nas tabelas IniFile. Quando usada em outras colunas, essa sintaxe é tratada da mesma forma que \[ \# *a chave de arquivo* \] .

 

 



