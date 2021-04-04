---
description: A ação InstallValidate verifica se todos os volumes aos quais o custo foi atribuído têm espaço suficiente para a instalação. A ação InstallValidate finalizará a instalação com um erro fatal se qualquer volume tiver espaço em disco insuficiente.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: Ação InstallValidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650ce136ac3b1b62e41ce34f79f5d28540d1292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171290"
---
# <a name="installvalidate-action"></a>Ação InstallValidate

A ação InstallValidate verifica se todos os [*volumes*](v-gly.md) aos quais o [*custo*](c-gly.md) foi atribuído têm espaço suficiente para a instalação. A ação InstallValidate finalizará a instalação com um erro fatal se qualquer volume tiver espaço em disco insuficiente.

A ação InstallValidate também notificará o usuário se um ou mais arquivos a serem substituídos ou removidos estiverem em uso no momento por um processo ativo. Para obter mais informações, consulte [reinicializações do sistema](system-reboots.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [CostFinalize](costfinalize-action.md) e todas as sequências de caixa de diálogo da interface do usuário que permitem que os usuários modifiquem os Estados de seleção e/ou diretórios devem ser sequenciadas antes da ação InstallValidate.

[Ações personalizadas](custom-actions.md) que alteram o estado de instalação de recursos ou componentes devem ser sequenciadas antes da ação InstallValidate.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

Normalmente, uma sequência de caixas de diálogo da interface do usuário anterior deve executar a mesma verificação que a ação InstallValidate quando o usuário tenta iniciar a cópia dos arquivos. Essa sequência de caixa de diálogo da interface do usuário deverá apresentar uma caixa **de diálogo sem espaço em disco** se os volumes selecionados não tiverem espaço suficiente para a instalação. As caixas de diálogo da interface do usuário devem ser criadas de forma a impedir que o usuário continue com a instalação se não houver espaço em disco suficiente. No caso de uma instalação silenciosa, não há nenhuma interface do usuário e a ação InstallValidate terminará a instalação se não houver espaço em disco suficiente. A causa do encerramento prematuro será registrada no arquivo de log se o log estiver habilitado.

Uma entrada será adicionada a uma tabela interna do FilesInUse se algum arquivo for substituído ou removido enquanto estiver aberto para execução ou modificação por qualquer processo durante o [*custo*](c-gly.md)do arquivo. A tabela FilesInUse contém colunas para o nome e o caminho completo do arquivo. Quando a ação InstallValidate é executada, o instalador consulta a tabela FilesInUse em busca de entradas e determina o nome do processo usando o arquivo. A ação InstallValidate adiciona um registro à tabela de interface do usuário da caixa de [listagem](listbox-table.md) para cada processo exclusivo identificado por essa consulta. O registro contém os seguintes valores em cada coluna:

**Propriedade**: FileInUseProcess

 

**Valor**: *nome do processo*

 

**Texto**: *texto contido na legenda da janela principal do processo*

A ação InstallValidate exibe a caixa de diálogo **arquivos em uso** . Essa caixa de diálogo exibe os processos que devem ser desligados para evitar a necessidade de reiniciar o sistema para substituir os arquivos em uso.

A ação InstallValidate consulta a tabela de [diálogo](dialog-table.md) em busca de uma caixa de diálogo criada com o nome reservado [FilesInUse](filesinuse-dialog.md) diálogo e o exibe. Essa caixa de diálogo deve conter um controle [ListBox](listbox-control.md) que esteja vinculado a uma propriedade chamada FileInUseProcess. Por convenção, essa caixa de diálogo tem um botão **sair**, **repetir** ou **ignorar** , mas isso se aplica ao autor da interface do usuário. Cada botão deve ser vinculado a um ControlEvent, [EndDialog](enddialog-controlevent.md) na tabela [ControlEvent,](controlevent-table.md) . A ação InstallValidate responde da seguinte forma ao valor retornado pelo ControlEvent, [DoAction](doaction-controlevent.md) , conforme ditado por um desses argumentos [EndDialog](enddialog-controlevent.md) associados ao botão enviado pelo usuário:

**Repetir**: todos os valores adicionados à tabela [ListBox](listbox-table.md) são desmarcados e o procedimento de [*custo*](c-gly.md) de arquivo inteiro é repetido, verificando novamente se há arquivos que ainda estão em uso. Se um ou mais processos ainda forem identificados como usando arquivos a serem substituídos ou excluídos, o processo se repetirá; caso contrário, InstallValidate retornará o controle para o instalador com um status de msiDoActionStatusSuccess.

**Exit**: a ação InstallValidate retorna imediatamente o controle para o instalador com um status de msiDoActionStatusUserExit. Isso encerra a instalação.

**Qualquer outro valor de retorno**: a ação InstallValidate retorna imediatamente o controle para o instalador com um status de msiDoActionStatusSuccess. Nesse caso, como um ou mais arquivos ainda estão em uso, as ações subsequentes [InstallFiles](installfiles-action.md) e/ou [InstallAdminPackage](installadminpackage-action.md) devem agendar os arquivos em uso para serem substituídos ou excluídos quando o sistema for reiniciado.

Se não houver nenhuma tabela de caixa de [listagem](listbox-table.md) no banco de dados, o InstallValidate será fechado silenciosamente sem um erro.

O ponto-e-vírgula é o delimitador de lista para transformações, fontes e patches e não deve ser usado nesses nomes de arquivo ou caminhos.

Arquivos marcados como somente leitura em um local somente leitura nunca são considerados em uso pelo instalador.

Uma caixa **de diálogo padrão sem espaço em disco** que contém os botões **anular** e **repetir** será apresentada ao usuário se o nível da interface do usuário for básico.

 

 



