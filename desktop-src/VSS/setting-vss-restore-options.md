---
description: As opções de restauração permitem que os solicitantes comuniquem opções de restauração personalizadas para gravadores.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Definindo opções de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788830"
---
# <a name="setting-vss-restore-options"></a>Definindo opções de restauração do VSS

As opções de restauração permitem que os solicitantes comuniquem opções de restauração personalizadas para gravadores.

## <a name="restore-options"></a>Opções de restauração

Padronizar o formato das opções de restauração permite que gravadores e solicitantes manipulem solicitações personalizadas comuns. As opções de restauração são definidas pelo solicitante chamando o método [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) até uma vez por componente selecionado para backup antes de chamar o método [**IVssBackupComponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) . A cadeia de caracteres passada no parâmetro *wszRestoreOptions* para o método **setrestore** pode conter vários valores, conforme descrito abaixo.

## <a name="format"></a>Formatar

O formato das opções de restauração, é um ou mais pares de nome/valor separados por vírgula, e o nome é opcionalmente prefixado com o nome do subcomponente ao qual se aplica. Os nomes de componente e os nomes de opção não diferenciam maiúsculas de minúsculas. A diferenciação de maiúsculas e minúsculas dos valores é determinada pelo gravador. Por exemplo:

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

Neste exemplo, "opção 1" aplica-se apenas ao subcomponente "child1" e seus descendentes, "opção 2" aplica-se a todos os componentes e seus descendentes, e "Option3" aplica-se somente aos \\ Subcomponentes "child2 Grandchild3" e seus descendentes.

O método [**setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) só pode ser chamado em componentes que são selecionáveis para backup, enquanto os nós descendentes podem não ser selecionáveis para backup, podem ser selecionáveis para restauração.

## <a name="common-restore-options"></a>Opções comuns de restauração

Essas opções de restauração comuns foram definidas para aumentar a interoperabilidade entre gravadores e solicitantes.

-   Autoriza

    A opção "autoritativo" dá suporte a vários valores "item", mas apenas um valor "All".

    Todo o componente é autoritativo.

    ``` syntax
    "Authoritative"="All"
    ```

    Somente o item especificado é autoritativo. O formato do item nomeado é definido pelo gravador. Designações comuns são " \* " para indicar todos os arquivos, "..." para indicar todos os arquivos e subdiretórios do componente especificado.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Rolar para frente

    Depois que um banco de dados é restaurado, os gravadores geralmente passam pelos logs para atualizar o banco de dados. No caso de restaurações incrementais ou diferenciais, o solicitante usa o método [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) para controlar parcialmente o comportamento de manipulação de log – essa opção de restauração permite um controle mais granular.

    Não faça a distribuição de logs.

    ``` syntax
    "Roll Forward"="None"
    ```

    Faça o roll-through de todos os logs.

    ``` syntax
    "Roll Forward"="All"
    ```

    Faça o roll-through dos logs até o ponto especificado. O formato do ponto especificado é definido pelo gravador.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Novo nome do componente

    Um gravador pode querer restaurar um componente para um novo nome. Por exemplo, restaurar um banco de dados para um nome diferente para restaurar um item individual; a restauração para o mesmo nome faria todos os dados que recomendamos que os gravadores aceitem um caminho lógico e um nome de componente válidos como valor de opções. Isso geralmente será usado com um [*destino direcionado*](vssgloss-d.md).

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



