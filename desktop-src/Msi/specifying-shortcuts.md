---
description: A tabela Atalho e as tabelas relacionadas do banco de dados de instalação respetivas informações necessárias para instalar atalhos. Consulte o Grupo de Tabelas de Informações do Programa e Editando Atalhos do Instalador.
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Especificando atalhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67b43a104ee05b3711ac98395098acf9393faab8e046296e58d93df4d6b9218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624680"
---
# <a name="specifying-shortcuts"></a>Especificando atalhos

A [tabela Atalho e](shortcut-table.md) as tabelas relacionadas do banco de dados de instalação respetivas informações necessárias para instalar atalhos. Consulte o [Grupo de Tabelas de Informações do Programa](program-information-tables-group.md) e Editar [Atalhos do Instalador](editing-installer-shortcuts.md).

Nesta seção, você adiciona informações que especificam atalhos anunciados e não anunciados para o Bloco de notas exemplo.

Use o editor de banco de dados para MNP2000.msi e insira os dados a seguir na tabela Atalho.

[Tabela de atalho](shortcut-table.md)



| Atalho  | Diretório\_ | Name         | Componente\_ | Destino             | Argumentos | Descrição | Tecla de acesso | Ícone\_         | IconIndex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Beisebol    | Beisebol           |           |             |        | orca \_icon.exe |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Concerto     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Dança       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Futebol    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Ajuda        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | Janeiro     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Bloco de notas     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | Bloco de notas     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

A instalação de exemplo precisa habilitar a instalação de um atalho anunciado para o recurso De basebol. Isso requer a especificação de uma chave para a tabela Ícone na coluna \_ Ícone da tabela Atalho. Para os fins deste exemplo, você pode copiar o ícone para o editor de banco de dados Orca fornecido com o SDK do Windows Installer. Exporte [a tabela Ícone](icon-table.md) do Orca.msi e, em seguida, mesce essa tabela no banco de dados MNP2000.msi usando Orca ou outra ferramenta de mesclagem. O Orca também cria um diretório chamado Icon no diretório que contém MNP2000.msi e adiciona o arquivo de dados binários do ícone orca \_icon.exe.ibd. Consulte a coluna Dados na tabela Ícone. A tabela Ícone concluída deve ser a seguinte quando exibida no Orca.

[Tabela de ícones](icon-table.md)



| Name           | Dados            |
|----------------|-----------------|
| orca \_icon.exe | \[Binary Data\] |



 

[Continuar](specifying-properties.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Editando atalhos do instalador](editing-installer-shortcuts.md)
</dt> </dl>

 

 



