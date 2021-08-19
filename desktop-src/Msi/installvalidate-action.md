---
description: A ação InstallValidate verifica se todos os volumes aos quais o custo foi atribuído têm espaço suficiente para a instalação. A ação InstallValidate encerra a instalação com um erro fatal se algum volume estiver com pouco espaço em disco.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: Ação InstallValidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8a5e2f69df5e588c2366f7cf9fff0fb3621889e9b725605a38acc14f39457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805634"
---
# <a name="installvalidate-action"></a>Ação InstallValidate

A ação InstallValidate verifica se todos os [*volumes*](v-gly.md) aos [*quais*](c-gly.md) o custo foi atribuído têm espaço suficiente para a instalação. A ação InstallValidate encerra a instalação com um erro fatal se algum volume estiver com pouco espaço em disco.

A ação InstallValidate também notifica o usuário se um ou mais arquivos a serem substituídos ou removidos estão atualmente em uso por um processo ativo. Para obter mais informações, consulte [Reinicializações do sistema.](system-reboots.md)

## <a name="sequence-restrictions"></a>Restrições de sequência

A [ação CostFinalize](costfinalize-action.md) e as sequências de caixa de diálogo da interface do usuário que permitem que o usuário modifique estados de seleção e/ou diretórios devem ser sequenciados antes da ação InstallValidate.

[Ações personalizadas](custom-actions.md) que alteram o estado de instalação de recursos ou componentes devem ser sequenciadas antes da ação InstallValidate.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

## <a name="remarks"></a>Comentários

Normalmente, uma sequência de caixa de diálogo da interface do usuário anterior deve executar a mesma verificação que a ação InstallValidate quando o usuário tenta iniciar a cópia de arquivos. Essa sequência de caixa de  diálogo da interface do usuário deverá apresentar uma caixa de diálogo Espaço Sem Disco se os volumes selecionados não têm espaço suficiente para a instalação. As caixas de diálogo da interface do usuário devem ser baseadas em uma maneira de impedir que o usuário prosseguir com a instalação se não houver espaço em disco suficiente. No caso de uma instalação silenciosa, não há nenhuma interface do usuário e a ação InstallValidate encerra a instalação se houver espaço em disco insuficiente. A causa da terminação prematura será registrada no arquivo de log se o registro em log estiver habilitado.

Uma entrada será adicionada a uma tabela FilesInUse interna se qualquer arquivo for substituído ou removido enquanto ele estiver aberto para execução ou modificação por qualquer processo durante o [*custo do arquivo*](c-gly.md). A tabela FilesInUse contém colunas para o nome e o caminho completo do arquivo. Quando a ação InstallValidate é executada, o instalador consulta a tabela FilesInUse para entradas e determina o nome do processo usando o arquivo. A ação InstallValidate adiciona um registro à tabela de interface do usuário [ListBox](listbox-table.md) para cada processo exclusivo identificado por essa consulta. O registro contém os seguintes valores em cada coluna:

**Propriedade**: FileInUseProcess

 

**Valor:** *nome do processo*

 

**Texto:** *texto contido na legenda da janela principal do processo*

A ação InstallValidate exibe a caixa **de diálogo Arquivos em** Uso. Essa caixa de diálogo exibe os processos que devem ser desligados para evitar a necessidade de reiniciar o sistema para substituir os arquivos em uso.

A ação InstallValidate [](dialog-table.md) consulta a tabela Dialog para uma caixa de diálogo autorada com o nome reservado [FilesInUse](filesinuse-dialog.md) diálogo e a exibe. Essa caixa de diálogo deve conter [um controle ListBox](listbox-control.md) que está vinculado a uma propriedade chamada FileInUseProcess. Por convenção, essa caixa de diálogo tem um botão **Sair,** Repetir ou **Ignorar,** mas isso é com o autor da interface do usuário. Cada botão deve ser vinculado a [um EndDialog](enddialog-controlevent.md) ControlEvent na [tabela ControlEvent.](controlevent-table.md) A ação InstallValidate responde da seguinte forma ao valor retornado pelo [DoAction](doaction-controlevent.md) ControlEvent, conforme ditado por um destes argumentos [EndDialog](enddialog-controlevent.md) associados ao botão pressionado pelo usuário:

**Repetição:** todos os valores adicionados à tabela [ListBox](listbox-table.md) [](c-gly.md) são limpos e todo o procedimento de custo do arquivo é repetido, remarcando os arquivos que ainda estão em uso. Se um ou mais processos ainda são identificados como usando arquivos a serem substituídos ou excluídos, o processo se repete; caso contrário, InstallValidate retorna o controle para o instalador com um status msiDoActionStatusSuccess.

**Sair:** a ação InstallValidate retorna imediatamente o controle para o instalador com um status de msiDoActionStatusUserExit. Isso encerra a instalação.

**Qualquer outro valor de** retorno: a ação InstallValidate retorna imediatamente o controle para o instalador com um status de msiDoActionStatusSuccess. Nesse caso, como um ou mais arquivos ainda estão em uso, as ações [InstallFiles](installfiles-action.md) e/ou [InstallAdminPackage](installadminpackage-action.md) subsequentes devem agendar os arquivos em uso para serem substituídos ou excluídos quando o sistema for reiniciado.

Se não houver nenhuma [tabela ListBox](listbox-table.md) no banco de dados, InstallValidate sairá silenciosamente sem um erro.

O ponto e vírgula é olimidor de lista para transformar, fontes e patches e não deve ser usado nesses nomes ou caminhos de arquivo.

Arquivos marcados como somente leitura em um local somente leitura nunca são considerados em uso pelo instalador.

Uma caixa **de diálogo** Fora do  Espaço em Disco padrão que contém os botões **Anular** e Repetir será apresentada ao usuário se o nível de interface do usuário for básico.

 

 



