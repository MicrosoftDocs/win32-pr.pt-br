---
description: A tabela de atalhos e as tabelas relacionadas do banco de dados de instalação armazenam as informações necessárias para instalar atalhos. Consulte o grupo tabelas de informações do programa e os atalhos do instalador de edição.
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Especificando atalhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29edf10a51827880a67826320d7f8415e70ea52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759372"
---
# <a name="specifying-shortcuts"></a>Especificando atalhos

A [tabela de atalhos](shortcut-table.md) e as tabelas relacionadas do banco de dados de instalação armazenam as informações necessárias para instalar atalhos. Consulte o [grupo tabelas de informações do programa](program-information-tables-group.md) e os [atalhos do instalador de edição](editing-installer-shortcuts.md).

Nesta seção, você adiciona informações que especificam atalhos anunciados e não anunciados para o exemplo do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela de atalho.

[Tabela de atalho](shortcut-table.md)



| Atalho  | Diretório\_ | Nome         | Componente\_ | Destino             | Argumentos | Descrição | Tecla de acesso | ícone\_         | IconIndex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Beisebol    | Beisebol           |           |             |        | \_icon.exe orca |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Concerto     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Dance       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Comemorar    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Ajuda        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | Janeiro     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Bloco de notas     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | Bloco de notas     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

A instalação de exemplo precisa habilitar a instalação de um atalho anunciado para o recurso de beisebol. Isso requer a especificação de uma chave para a tabela de ícones na \_ coluna ícone da tabela de atalho. Para os fins deste exemplo, você pode copiar o ícone do editor de banco de dados Orca fornecido com o SDK do Windows Installer. Exporte a [tabela de ícones](icon-table.md) de Orca.msi e mescle essa tabela no banco de dados de MNP2000.msi usando o Orca ou outra ferramenta de mesclagem. O Orca também cria um diretório chamado Icon no diretório que contém MNP2000.msi e adiciona o ícone arquivo de dados binários Orca \_icon.exe. IBD. Consulte a coluna de dados na tabela de ícones. A tabela de ícones concluídas deve ter a seguinte aparência quando exibida em orca.

[Tabela de ícones](icon-table.md)



| Nome           | Dados            |
|----------------|-----------------|
| \_icon.exe orca | \[Binary Data\] |



 

[Continuar](specifying-properties.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Editando atalhos do instalador](editing-installer-shortcuts.md)
</dt> </dl>

 

 



